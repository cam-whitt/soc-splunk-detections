# Detection: Repeated Failed Logins

## Purpose
Identify repeated failed authentication attempts that may indicate password spraying or brute force behavior.

## Data Source
Windows authentication/security events ingested into Splunk.

## Splunk Search (Example)
(Insert your actual query here)

## Triage Notes
- Identify target account(s)
- Check source IP / host
- Look for follow-on success logon
- Validate if this is expected behavior (VPN, service accounts, etc.)

## Recommended Response
- Confirm user activity
- Investigate source system
- Consider lockout / password reset if suspicious
