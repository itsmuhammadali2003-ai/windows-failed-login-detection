Failed-Login Detection Logic

Objective

Identify repeated failed login attempts that may indicate password guessing.

Detection Rule

Flag an account when it records 5 or more failed logon events (Windows Event ID 4625) within a rolling 3-minute window.

Test Result

The synthetic dataset contains 12 failed events for the account "ali" from the example source IP "192.0.2.10" between 09:00:00 and 09:02:45.

The test data meets the illustrative threshold and should generate an alert for investigation.

Analyst Follow-up

- Check whether the activity is expected.
- Review the source address and account context.
- Look for related successful logons and other suspicious events.
- Escalate according to the organisation's incident-response procedures if corroborating evidence supports it.

Limitations

This is a manual analysis of synthetic CSV data, not a live Windows detection system. A threshold match does not prove an attack. Production detection requires a reliable event source, correct time handling, and testing for false positives.
