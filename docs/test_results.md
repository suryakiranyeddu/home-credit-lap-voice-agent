# Test Results Summary

## Execution overview
Project notes recorded 52 executions in Bolna, 50 marked Completed at the time of review. This number describes execution status, not the number of successful eligibility tests.

## Summary of documented scenarios
- PASS: 18
- FAIL: 1
- PARTIAL: 1

These counts are for the 20 scenarios in `tests/test_scenarios.csv`, not for all 52 executions. Verify against the live Bolna history before final submission if the dashboard has changed.

## Key observations
- Eligibility checks were exercised for property type, original documents, ownership, income source, loan amount cap, tenure boundaries, callback, identity refusal, rate questions, and loan-transfer routing.
- The corrected mixed bank/cash income retest was documented as PASS in the project notes, but a working recording link has not been verified. The related income-question recording below is a different scenario and is not evidence of the mixed-income retest.
- Hindi conversation handling failed: the agent repeatedly insisted on English rather than proceeding in Hindi.
- Market value was not reliably enforced in one out-of-order conversation: the agent proceeded to tenure and qualified even though market value was not supplied. This is a PARTIAL result and should be disclosed.

## Recording links
Happy-path recording:
https://api.bolna.ai/recordings/call/e8e61eac-591b-42a8-8f30-648dcbcc0ebc

Mixed bank/cash income retest: PASS was documented in the project notes, but its recording link is unavailable/unverified. The broken recording URLs have been removed.

Related income-question test (caller refuses mandatory income-source question; not the mixed-income retest):
https://api.bolna.ai/recordings/call/1916baa5-4b7f-4493-af30-3a61f5c9bae9

Hindi test:
https://api.bolna.ai/recordings/call/b6779c01-adb8-44e9-8d32-caa1d84aaef3

Market value partial test:
https://api.bolna.ai/recordings/call/8decf433-2299-4d38-b1fc-e1d5b2757fc7

## Important note
Recording IDs are included as evidence references. Open each recording in Bolna to verify its content before making claims beyond the observations above.


## Raw Bolna execution history

`tests/call_execution_history.csv` contains the supplied raw execution-history export (54 records). A completed execution is not automatically a passed eligibility test. The export includes missing recording URLs for some calls; evaluate scenario outcomes against the transcript and recording where available. Known issues documented in this project remain: Hindi test failed and market-value flow was partial.
