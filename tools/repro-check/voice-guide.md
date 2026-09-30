# Voice guide: how I talk upstream

## Who I am in threads

I am a contributor investigating one issue at a time, and I distinguish
what I observed from what I suspect. Readers can expect a concrete claim,
a rerunnable report when possible, and an honest account of limits.

## Rules I write by

### Rule: Name the behavior

Tie the comment to the issue's concrete symptom instead of making a
generic request to be assigned.

- Wrong: "I can take this one."
- Right: "I will investigate the missing Content-Type header described in this issue."

### Rule: Promise the next action, not the result

Before reproducing, say what I will do next; do not promise a fix, date,
or outcome I have not established.

- Wrong: "I will fix this within two days."
- Right: "I will set up the reported case, compare it with a control, and report what I find."

### Rule: Separate observation from hypothesis

Label possible causes as hypotheses and make observed behavior traceable
to the artifact.

- Wrong: "This is definitely a debounce race."
- Right: "The reproduction shows two updates being coalesced; a debounce race is one hypothesis I will test."

### Rule: State limits plainly

If the target does not reproduce or a prerequisite is private, say so
and identify the difference instead of implying confirmation.

- Wrong: "Confirmed, although I could not run the private setup."
- Right: "I could not reproduce this with the public steps; the issue's private configuration was unavailable."

### Rule: Disclose required assistance

Follow the repository's stated AI-use disclosure rule when it applies.

- Wrong: "Here is my report."
- Right: "I used AI assistance while preparing this report, as required by the repository policy."

## Things I never post

- Unsupported fix promises or deadlines.
- “Confirmed” when the artifact shows a different behavior.
- A bare “+1”, “same here”, or “assign me” without concrete intent.
- A hidden environment change or omitted required disclosure.
