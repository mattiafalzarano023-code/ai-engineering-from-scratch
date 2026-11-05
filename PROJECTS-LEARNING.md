# My Projects
<!-- Managed by the build-project tutor. -->

## prompt-regression-tester
- Started: 2026-11-05
- Workspace: C:\Users\MattiaFalzarano\AI Stuff\ai-engineering-from-scratch\learning-artifacts\prompt-regression-tester
- Mode: Executable (Python 3.14.5 on Windows; WSL Ubuntu is available if a later stage needs POSIX locks)
- Current stage: 2 of 4

| Stage | Status | Grader result | Date | Note |
|---|---|---|---|---|
| 01-validate-cases | Done | Stage 1 pass (5 tests) | 2026-11-05 | First code written by the learner. A dict silently overwrites a duplicate key, so duplicate ids must be rejected before results are collected; a set of seen ids does it. Fixed along the way: `is in`, a missing `+`, `case(["checks"])` (call) vs `case["checks"]` (key), `or` chains that are always true, adding the id (not the whole dict) to the set, returning `cases`. Reflection: a changed prompt changes the case hash (avalanche effect), and stopping avoids comparing recordings made for different cases, which would give false results with no runtime error. |
| 02-score-recordings | Grader pass, reflection pending | Stages 1-2 pass (11 tests) | 2026-11-05 | UPDATE: at the learner's request I added the missing `import json` to their `main.py` and the grader now passes (stage 1: 5 tests, stage 2: 6 tests); the "next time" instructions below about the missing import no longer apply. Only the reflection question remains. |
| 02-score-recordings (history) | | | |  Learner was mentally tired and asked to see the solution before any attempt at `score_response`; I wrote a reference for that one function (not copied from `solution/`) and checked it passes stages 1-2 in a scratch workspace. Understood before that: the dict return (tests read `["passed"]`, details tell which promise failed), `checks` is one case's list of check dicts, case-sensitive `contains`, `all([])` is True so empty checks must fail explicitly, `.append`, dict assignment. End of session 2026-11-05: the learner copied the function into their `main.py` but forgot the `import json` line at the top of the file; the grader shows stage 1 pass, stage 2 FAIL with 2 errors (`NameError: name 'json' is not defined`, in the `json` check tests). Next time: let them find the cause from the traceback (hint: where does Python learn what `json` is?), add the import, rerun the stage 2 grader. Still to do after that: the grader pass, then answer "Investigate next" (does lowercasing change the API_KEY contract?). |
| 03-pair-revisions | | | | |
| 04-gate-releases | | | | |
