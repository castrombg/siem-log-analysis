# SIEM Log Analysis (Splunk)

SIEM-based analysis of authentication and network activity to identify brute-force attempts and suspicious login behavior.

## Scenario
Authentication logs were reviewed after SIEM alerts indicated repeated failed login attempts followed by successful authentication from unfamiliar IP addresses.

## What Was Analyzed
- Authentication logs
- Source IP addresses
- Login success and failure patterns

## Findings
- Multiple failed login attempts from a single IP address
- Successful login shortly after repeated failures
- Activity consistent with brute-force or credential stuffing behavior

## Skills Demonstrated
- SIEM alert triage
- SPL query writing
- Log correlation
- Threat identification
