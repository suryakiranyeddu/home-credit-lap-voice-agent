# Known Limitations and Submission Notes

1. **Hindi language handling — FAIL in a recorded test.** The agent repeatedly insisted on English and did not complete the Hindi screening. This is documented in the test CSV and should not be hidden.
2. **Market-value capture — PARTIAL in a recorded test.** In one out-of-order conversation, the caller did not provide market value; the agent moved to tenure and later qualified the caller. The market-value field should be enforced before eligibility is concluded.
3. **Public agent link — unconfirmed.** The Share option displayed `https://bolna.ai/a/f6a7e211-8d08-4bb5-9d12-6a24c655e4d9`, but Incognito access reportedly requested login. Do not call it publicly accessible unless access is verified without authentication.
4. **Web-call deployment.** Bolna documentation describes a Web Call SDK that is embedded in an application; it is not the same as a guaranteed public agent page. Building a web-call page/backend may be outside the current scope.
5. **Prompt provenance.** The prompt files in this starter package are reconstructed drafts based on assignment requirements and conversation notes. They must be compared with the exact deployed prompt in Bolna and replaced if different.
6. **Data protection.** Do not publish API keys, credentials, private customer details, phone numbers, or raw logs containing sensitive information.
