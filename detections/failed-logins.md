# Detection: Repeated Failed Login Attempts

## Purpose
Identify repeated failed authentication attempts that may indicate password spraying, brute-force activity, or unauthorized access attempts.

## Data Source
Windows authentication and security event logs ingested into Splunk.

## Detection Logic
This detection looks for multiple failed login events associated with the same account or source within a defined time window.

## Example Splunk Search
(Note: Query structure may vary based on log source and field names.)

index=security EventCode=4625
| stats count by user, src_ip
| where count > 5

## Triage Steps
- Identify the affected user account(s)
- Review source IP addresses and hostnames
- Check for subsequent successful login events
- Validate whether activity aligns with normal user behavior (VPN usage, service accounts, etc.)

## Severity Assessment
- Medium: Single account with repeated failures
- High: Multiple accounts targeted from a single source

## Recommended Response
- Notify user if activity appears suspicious
- Investigate source system or IP
- Reset credentials if compromise is suspected
- Escalate according to SOC incident handling procedures

## Why This Matters
Repeated failed authentication attempts are a common early indicator of account compromise and are routinely monitored by SOC teams to prevent unauthorized access.
