# Log Triage Engine (still working on this)

### Simulates a SOC alert queue using real and synthetic security telemetry, supporting alert triage, correlation, deduplication, escalation workflows, and false-positive reduction - ingests telemetry, generates detections, and models analyst triage, escalation, and incident response workflows.

 ---
 <br> 
 
# Project Roadmap

## Phase 1 - Detection Ingestion
- Connect to Splunk via the REST API.
- Execute predefined SPL detection queries against Sysmon and Windows Event telemetry.
- Convert detection results into structured alert objects.

## Phase 2 - Alert Queue
- Implement a persistent alert queue using SQLite.
- Track alert lifecycle states:
  - New
  - In Progress
  - Escalated
  - Closed

## Phase 3 - Triage Engine
- Apply severity scoring based on alert context.
- Implement alert deduplication to reduce noise.
- Correlate related alerts into single incidents.

## Phase 4 - Threat Intelligence Enrichment
- Integrate VirusTotal API enrichment for IP addresses and domains.
- Attach reputation, ASN, and malicious scoring data to alerts.

## Phase 5 - Analyst Dashboard
- Build a Streamlit-based SOC dashboard.
- Display alert queue, severity, status, and investigation context.
- Support analyst actions such as escalation, closure, and false-positive classification.

## Phase 6 - Metrics & Reporting
- Track alert volume, triage decisions, false positives, and deduplication effectiveness.
- Generate operational metrics to measure alert quality and workflow efficiency.

## Phase 7 - CI/CD
- Implement GitLab CI/CD pipelines.
- Automate testing of detection logic and alert processing workflows.
- Validate code changes prior to deployment.
