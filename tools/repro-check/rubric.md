# Rubric: is this reproduction package ready to post?

<!--
THIS IS THE PART YOU WRITE. The skill in SKILL.md executes whatever
checks you define here. It ships empty on purpose: the judgment is your
work.

A filled rubric must contain:

1. At least one row in the checks table. Each row needs all four
   columns:
   - Check: a short name (used in the output JSON).
   - Evidence: exactly what to look at, and where in the package. Name
     the part (the claim comment, the repro report's environment
     record, the artifacts read against the issue's description, the
     repo-facts block) or a location from your
     references/evidence-guide.md. "The report" is not a source; "the
     output excerpt read against the error the issue describes" is.
   - Pass condition: a decision rule about the OUTCOME that someone
     else could apply and get your answer. Judge the thing itself (does
     the artifact show the issue's behavior?), never the write-up's
     shape (how many steps it has, how long it is, whether it uses a
     template's headings). Structure-shaped checks are what make
     graders disagree with themselves.
   - Weight: `required` (a fail here holds the package) or `preferred`
     (never changes the verdict).

2. A verdict rule below the table: how the check grades combine into
   accept (ready) or reject (hold), including how `unclear` is
   treated. The verdict space is binary. If you write no rule for
   `unclear`, the skill treats it as fail.

Cover what actually gets bad packages posted. The lecture named the
proof families: the environment is recorded, the steps are complete
and followable, the behavior shown matches the issue (not an adjacent
one), the outcome is stated honestly (an evidenced cannot-reproduce is
a pass, a confident wrong-target is not), and the words respect the
repo's conventions. A rubric that ignores a family will fail eval
packages designed around that family.
-->

## Checks

| Check | Evidence | Pass condition | Weight |
|---|---|---|---|
| environment-recorded | The repro report's environment record, read against the issue's target versions, platforms, drivers, shells, build profiles, or other stated conditions. | Pass when the report records the material environment details needed to interpret or repeat the result, including any meaningful deviation from the issue's target. A truthful cannot-reproduce report may pass when it records enough environment to explain the attempt and difference. | required |
| steps-followable | The repro report's commands and setup steps, starting state, inputs, and trigger sequence, read against the issue description and repo-facts instructions. | Pass when a stranger can carry out the setup and trigger from the report, or when the report explicitly identifies an unavailable private dependency and therefore honestly limits what can be rerun. Skipped trigger details, a different input, or an unshared required config fails. | required |
| behavior-matches | The repro report's output excerpts, logs, screenshots, measurements, or other artifacts, read against the exact behavior described by the issue. | Pass when the artifact directly shows the reported behavior, or clearly shows that the behavior did not reproduce. A control run is useful but does not replace an artifact of the target behavior. An adjacent error, healthy run, or assertion without evidence fails. | required |
| outcome-honest | The report's observed-versus-expected statement and the claim comment's wording, read against the artifacts and any environment or version deviations. | Pass when conclusions are no stronger than the evidence: reproduction is claimed only when the target artifact is shown, and cannot-reproduce or uncertainty is stated when appropriate. A confident diagnosis, certainty, or generalization contradicted by the evidence fails. | required |
| claim-specific | The claim comment, read against the issue title/body/thread and the repo-facts contribution policy. | Pass when the claim names the issue's concrete behavior or scope, states what the commenter will investigate next, and does not promise an unsupported fix, deadline, or result. A bare +1, assign-me boilerplate, or vague ownership claim fails. | required |
| conventions-disclosure | The claim and repro comments read against the repo-facts contribution policy, including its AI-use rule. | Pass only when the comments follow the stated reporting/comment conventions and include an explicit AI-assistance disclosure if the policy requires one. If the policy requires disclosure and neither comment discloses it, fail even when the reproduction evidence is otherwise excellent; if the policy does not require disclosure, do not penalize its absence. | required |

## Verdict rule

Accept only when every required check passes. Treat unclear as fail.
Preferred checks, if added later, never change the verdict.
