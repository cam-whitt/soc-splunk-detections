# SOC Splunk Detections (Windows Auth + Privilege Changes)

## Objective
Build SOC-style detections in Splunk focused on authentication anomalies and privilege-related activity.

## What I Built
- Searches for repeated failed logons
- Detection logic for suspicious authentication patterns
- Alerts for privilege/role changes (where applicable)
- Short incident-style writeups documenting:
  - What happened
  - What evidence was found
  - Recommended response steps

## Tools
Splunk, Windows event logs (auth/security), basic SOC triage methodology

## Why It Matters
These detections map to common SOC monitoring responsibilities and help identify account misuse and access-risk activity.
