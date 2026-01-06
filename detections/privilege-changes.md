# Detection: Privilege or Role Changes

## Purpose
Monitor changes to user privileges or group memberships that could indicate unauthorized elevation of access.

## Data Source
Windows security logs and directory service audit events ingested into Splunk.

## Detection Logic
This detection identifies events where user accounts are added to privileged groups or roles.

## Example Splunk Search
(Note: Query structure may vary.)

index=security (EventCode=4728 OR EventCode=4732 OR EventCode=4756)
| stats count by user, target_group

## Triage Steps
- Identify the account receiving elevated access
- Confirm who initiated the change
- Validate business justification or approval
- Check for additional suspicious activity involving the account

## Severity Assessment
- Medium: Approved or expected role change
- High: Unauthorized or unexplained privilege escalation

## Recommended Response
- Confirm access change with management or IAM team
- Revoke access if unauthorized
- Document findings for audit and compliance tracking
- Escalate according to incident response procedures

## Why This Matters
Unauthorized privilege changes increase the risk of lateral movement and data exposure. SOC teams monitor these events to detect misuse of access and insider threats.
