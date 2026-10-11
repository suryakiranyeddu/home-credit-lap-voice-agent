# Home Credit LAP Voice Agent — Nani

## Project overview
This project documents a Bolna voice agent named **Nani** designed to conduct an initial qualification conversation for a Home Credit Loan Against Property (LAP) enquiry.

## Objectives
- Verify the caller's identity before discussing the enquiry.
- Offer a callback when the caller is busy.
- Collect the required property, ownership, documentation, income, amount, market-value, and tenure information.
- Route existing-loan transfer / EMI-reduction enquiries to a specialist.
- Route eligible prospects to a senior expert without promising approval or an interest rate.

## Eligibility logic documented for this project
1. Property type: residential, commercial, and industrial are accepted; agricultural property is rejected.
2. Ownership: sole and joint ownership are accepted.
3. Documents: original property documents are required.
4. Requested amount: up to ₹75 lakh; if the requested amount is higher, ask whether the caller agrees to consider a maximum of ₹75 lakh.
5. Income: salaried and self-employed callers may qualify only when income is received through bank/non-cash channels. Any cash component makes the case ineligible under the supplied rules.
6. Market value: collect the customer's estimate; no minimum market value was specified in the supplied assignment context.
7. Tenure: 3–15 years inclusive.
8. Existing property loan / EMI reduction: route to a loan-transfer specialist and end the qualification flow.
9. Eligible prospects: hand off to a senior expert. Do not guarantee approval, disbursal, or a rate.

## Technology
- Bolna Agent Studio for agent configuration and call executions.
- Voice conversation recordings and transcripts from Bolna.
- GitHub for versioned project documentation and test evidence.

## Screenshot evidence

**All 24 screenshot image files are included in `screenshots/` in this ZIP.** The filenames below reflect the actual files included in this archive:

1. `01_Agent_Dashboard.png`
2. `01_Agent_Configuration_2.png`
3. `03_system_prompt_part1.png`
4. `03_system_prompt_part2.png`
5. `05_hangup_prompt1.png`
6. `05_hangup_prompt2.png`
7. `05_hangup_prompt3.png`
8. `06_execution_history.jpg`
9. `01_HappyPath_01_Identity_Verification.png`
10. `01_HappyPath_02_Offer_Disclosure_and_Time_Check_2.png`
11. `01_HappyPath_03_Fresh_Loan_Selection_2.png`
12. `01_HappyPath_04_Property_Type_Check_2.png`
13. `01_HappyPath_05_Ownership_Check_2.png`
14. `01_HappyPath_06_Original_Documents_Check_2.png`
15. `01_HappyPath_07_Loan_Amount_Check_2.png`
16. `01_HappyPath_08_Income_and_Bank_Source_Check_2.png`
17. `01_HappyPath_09_Property_Value_Unknown_2.png`
18. `01_HappyPath_10_Loan_Tenure_Check_2.png`
19. `01_HappyPath_11_Senior_Expert_Handoff_and_Disclaimer_2.png`
20. `01_HappyPath_12_Call_Audio_Waveform_and_Hangup_2.png`
21. `08_ineligible_case_recording_transcript.png`
22. `09_income_retest_recording_transcript1.png`
23. `09_income_retest_recording_transcript2.png`
24. `10_drive_sharing_evidence.png`

See [`docs/screenshot_index.md`](docs/screenshot_index.md) for the evidence purpose of each included image. Do not add fabricated screenshots or publish API keys, credentials, or private customer details.

## Sample public recording
Happy-path recording (tested in Incognito according to project notes):
https://api.bolna.ai/recordings/call/e8e61eac-591b-42a8-8f30-648dcbcc0ebc

## Screen recording
Google Drive screen recording:
https://drive.google.com/file/d/1hRDS8NlgXvlPff7c_06dlBWRoe6_KrXt/view?usp=sharing

## Limitations / known issues
See [`docs/limitations.md`](docs/limitations.md). The agent's public browser-call URL has not been confirmed to work without login. Do not describe a login-protected URL as public.

## Important verification note
The system prompt file contains the detailed prompt supplied for this project, formatted as a clean Markdown document. Before submission, compare it with the active Bolna Canvas prompt to ensure it matches the deployed configuration exactly. The Hangup prompt is kept separately in `prompts/hangup_prompt.md`.

## Screenshot files
All 24 screenshot images are already included. The `screenshots/README.txt` file is only an informational note; no screenshot upload is needed unless you want to replace an image with a newer version.

## Raw call log
The supplied Bolna execution export is at `tests/call_execution_history.csv` (54 records). Completed execution status does not mean the eligibility test passed.
