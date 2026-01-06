# Incident Writeup 001 – Authentication Anomaly

## Alert Summary
An alert was generated for repeated failed authentication attempts associated with a single user account.

## Evidence Reviewed
- Authentication failure events
- Source IP address
- Time window of activity
- User account history

## Investigation Findings
The account experienced multiple failed login attempts over a short period. No immediate successful login was observed following the failures. Activity did not align with typical user behavior.

## Impact Assessment
Potential risk of account compromise if activity were to continue or succeed.

## Recommended Actions
- Notify the user of suspicious activity
- Monitor the account for follow-on authentication attempts
- Enforce password reset if activity persists
- Document the incident for tracking and trend analysis

## Lessons Learned
Early detection of authentication anomalies helps reduce the likelihood of successful account compromise and supports proactive security monitoring.
