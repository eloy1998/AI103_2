# Unit 2 reproduction

## Issue and account

- Path Review issue: **Pending issue URL**
- GitHub username: **Pending username**

## Claim comment

Link: **Pending: post claim after live-mode grading**

Comment text:

> Pending the issue URL. The claim must name the issue's concrete
> behavior, promise investigation and a later report, and avoid promising
> a fix, deadline, or reproduction result.

## Reproduction comment

Link: **Pending: reproduce the issue and post the live-mode-approved report**

Comment text:

> Pending reproduction. The report must include the relevant environment,
> complete setup and trigger steps, observed artifacts, expected versus
> actual behavior, and any honest cannot-reproduce limitations.

## Eval iteration fields

### Run history

1. Ran the calibration package `calib-02` with the completed rubric and
   evidence guide. It correctly returned `reject`.
2. Ran the first complete 20-package evaluation. It returned 19/20:
   `pkg-20` was incorrectly accepted, and the disclosure category floor
   was unmet.
3. Tightened the conventions/disclosure pass condition to require an
   explicit AI-assistance disclosure whenever the repository policy
   requires one.
4. Re-ran `pkg-20` and `calib-02` as canaries; both returned `reject`.
5. Ran the confirming complete evaluation with `--save-run
   eval-run.txt`; it returned 20/20 and passed every category floor.

### Package analysis

The scored disagreement was `pkg-20` (`ghostty-org/ghostty#13604`). The
first run said `accept` while the gold label said `reject`. The
reproduction evidence itself was strong, but the repository policy
required disclosure of AI assistance and neither comment disclosed it.
The original conventions check did not make that conditional policy
failure explicit enough. After revising the check, the package returned
`reject`, matching the gold label.

### Check rationale

The final check reads:

> Pass only when the comments follow the stated reporting/comment
> conventions and include an explicit AI-assistance disclosure if the
> policy requires one. If the policy requires disclosure and neither
> comment discloses it, fail even when the reproduction evidence is
> otherwise excellent; if the policy does not require disclosure, do not
> penalize its absence.

This check is required because a complete and faithful reproduction can
still violate a repository's stated contribution policy.

### Trade-offs

The rubric uses several required checks rather than one broad quality
check so that no-evidence, wrong-target, unfollowable, and disclosure
failures remain distinguishable. This is stricter than accepting a
well-written report based only on its artifact, but it can reject a
technically useful report when the repository's required conventions are
not followed. The explicit cannot-reproduce allowance preserves honest
reports while still requiring an environment and evidence record.
