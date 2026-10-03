# packshield alert log

An append-only record of when the packshield detector raised an alert on an npm
publish, written by the detector itself within minutes of scoring.

Each line of `alerts.jsonl` names a package version, the scoring pass (`early`,
a few minutes after publish; `final`, after the release tag has had time to
appear), the alert tier, the ids of the rules that fired, the ruleset version,
the publish time, the scoring time, and the SHA-256 of the full scoring record.

The full record is not published here. An entry is not an accusation: the
detector works from publish metadata alone and most alerts turn out to be
ordinary releases. What this log establishes is only *when* the detector
flagged a version, independent of anything written about it afterwards.

The detection approach is described at https://github.com/JakeShulman/dependency_detection.
