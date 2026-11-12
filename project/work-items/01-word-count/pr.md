# spec 01: word-count

## Summary

This change adds `count_words` to the `textstats` package and a command `python3 -m textstats FILE` that prints the word count of a file. It lets a writer keep to a word limit from Python or from the shell.

## Spec

- [requirements.md](requirements.md)
- [design.md](design.md)
- [tasks.md](tasks.md)

## Gates

| Gate | Status | Report |
|---|---|---|
| Design review | APPROVED WITH ISSUES | [design-review-summary.md](design-review-summary.md) |
| Task review | APPROVED | [task-review-summary.md](task-review-summary.md) |
| Implementation audit | PASSED | [implementation-audit.md](implementation-audit.md) |
| Test plan | PASSED | [test-plan.md](test-plan.md) |
| Spec maintenance | skipped, no peer | none |

## Evidence

- Tests: `Ran 6 tests`, `OK`, on commit 755df30.
- Implementation audit findings: 0 CRITICAL, 0 MAJOR, 1 MINOR.

## Review first

- Design review MAJOR finding 1: a file that is not valid UTF-8 raises `UnicodeDecodeError` with a traceback. The design does not decide the behaviour.
- Test plan gap 1 (open): no test for a file that is not valid UTF-8.
