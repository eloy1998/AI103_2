# Evidence guide: where proof lives in a reproduction package

## Environment

Where it lives: the repro report's environment section or explicit
environment lines before its commands. Compare these with the issue body,
maintainer comments, and repository documentation. Good evidence names
relevant versions and platform details, including driver, shell, build
profile, or release channel when material, and calls out differences.

## Steps

Where it lives: the repro report's setup, commands, inputs, and trigger
sequence, plus any repo-facts bug-report template. Good steps start from a
stated state, include complete commands or inputs, identify required files
or configuration, and use the issue's trigger. A private prerequisite must
be named rather than presented as a public rerun.

## Behavior shown

Where it lives: output excerpts, logs, screenshots, measurements, or other
artifacts, compared directly with the issue's symptom and expected result.
Good evidence shows the observable failure or an evidenced
cannot-reproduce result. Healthy startup output, a nearby validation error,
or a claim without the target artifact is not proof. Controls provide
contrast but cannot replace the target artifact.

## Honesty

Where it lives: the report's observed-versus-expected comparison and the
claim/repro conclusions, checked against artifacts and environment
differences. Good writing separates observation from hypothesis,
acknowledges version or platform deviations, and says cannot reproduce
when appropriate. Diagnoses and broad generalizations need evidence.

## Comms

Where it lives: the claim comment against the issue title/body/thread,
and both comments against repo-facts contribution policy and templates.
Good claim language identifies the specific behavior, says what
investigation will happen next, and makes no unsupported fix or date
promise. Comments follow required templates and disclose AI assistance
whenever repository policy requires it. Bare "+1", generic assign-me
boilerplate, or omitted required disclosure fails.
