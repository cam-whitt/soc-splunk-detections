# SOC Log Detection & Incident Analysis (Splunk)

## Objective
Demonstrate SOC-style monitoring, detection, and investigation using log analysis focused on authentication activity and access-related events.

## Scenario
Security logs were ingested into Splunk to simulate a SOC monitoring environment. The goal was to identify suspicious authentication behavior and privilege-related activity that could indicate account misuse or access risk.

## Detections Implemented
- Repeated failed login attempts
- Abnormal authentication patterns across time windows
- Privilege or role change activity (where applicable)

## Investigation Approach
For each detection:
- Reviewed authentication events and timestamps
- Identified affected accounts and source systems
- Checked for follow-on successful logins
- Assessed whether activity was expected or suspicious

## Incident Writeups
Each alert includes a short incident-style writeup documenting:
- Alert summary
- Evidence reviewed
- Findings
- Recommended response actions

## Tools Used
Splunk, Windows authentication/security logs, SOC triage methodology

## Why This Matters
Authentication abuse and privilege misuse are common attack vectors. SOC teams rely on log-based detections like these to identify account compromise early and reduce access-related risk.
