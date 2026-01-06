# Incident Writeup 002 – Unauthorized Privilege Escalation

## Alert Summary
An alert was triggered indicating a user account was added to a privileged security group outside of normal onboarding or change management processes.

## Evidence Reviewed
- Security event logs showing group membership changes
- Account receiving elevated privileges
- Initiating user or system performing the change
- Timestamp and affected security group

## Investigation Findings
The user account was added to a privileged group granting elevated access. Initial review did not identify a corresponding change request or documented business justification. The change was performed outside of standard access provisioning workflows.

No additional suspicious activity was immediately observed, but the access level granted increased risk exposure.

## Impact Assessment
Unauthorized privilege escalation increases the risk of:
- Lateral movement
- Data exposure
- Abuse of administrative permissions

If left unaddressed, elevated access could enable further compromise or policy violations.

## Recommended Actions
- Validate access change with management or IAM team
- Revoke elevated privileges if unauthorized
- Review recent activity for the affected account
- Document the incident for audit and compliance purposes
- Recommend access review of similar privileged groups

## Lessons Learned
Monitoring privilege changes is critical to detecting misuse of access. Strong coordination between SOC and IAM teams helps ensure access changes follow least-privilege and approval requirements.
