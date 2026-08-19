# Operation Ghost Account: The RIUS Enterprise Insider Incident

> A full-scale SOC attack, detection, and incident response case study built inside the fictional RIUS Enterprise environment.

![Status](https://img.shields.io/badge/Status-Active%20Development-blue)
<!-- progress-start -->
![Progress](https://img.shields.io/badge/Progress-38%25-orange)
![Target Completion](https://img.shields.io/badge/Target-Sep%2012%2C%202026-green)

`████████░░░░░░░░░░░░` **38%**
<!-- progress-end -->

## Project Overview

Operation Ghost Account follows a simulated insider threat incident at RIUS Enterprise, a fictional technology services company. The project covers the full incident lifecycle, including the security failures that made the attack possible, attack simulation, log collection, Splunk detection engineering, SOC investigation, containment, and reporting.

The lab is now being built in Microsoft Azure to provide a stable cloud-hosted environment for Windows endpoint telemetry, attack simulation, and SOC analysis.

## Incident Scenario

A former RIUS Enterprise IT support employee was terminated following repeated workplace and security policy violations. During a rushed offboarding process, several important security controls were missed:

- The former employee's account was not disabled immediately.
- Existing remote access and authenticated sessions were not fully revoked.
- A shared administrator credential was not rotated.
- MFA was not enforced on a legacy access path.
- Logs were collected, but alert coverage and active monitoring were limited.

The former employee later uses retained access to re-enter the RIUS Enterprise environment. The simulated intrusion will progress through unauthorized access, internal reconnaissance, suspicious PowerShell activity, persistence, lateral movement, data staging, and simulated exfiltration of fictional company data.

The RIUS Enterprise SOC must detect the activity, determine what happened, contain the incident, identify the failed controls, and recommend improvements.

## Project Objectives

- Build a realistic small enterprise security lab in Microsoft Azure.
- Generate controlled attack activity inside an authorized lab environment.
- Collect Windows, Sysmon, authentication, process, and network telemetry.
- Develop and tune Splunk searches, alerts, detections, and dashboards.
- Investigate the incident from a SOC analyst perspective.
- Map the observed activity to MITRE ATT&CK.
- Identify the root cause and failed security controls.
- Produce an incident report, executive summary, and remediation plan.

## Environment

| System | Purpose |
|---|---|
| `RIUS-WKS01` | Azure-hosted Windows 11 employee workstation and primary monitored endpoint |
| `RIUS-DC01` | Planned Windows Server domain controller and Active Directory environment |
| `RIUS-KALI01` | Planned authorized attacker workstation |
| Microsoft Azure | Cloud infrastructure, virtual networking, NSG controls, and remote lab access |
| Splunk SIEM | Centralized logging, detection, alerting, and investigation |
| Sysmon | Detailed Windows process, network, file, registry, and DNS telemetry |

## Current Telemetry Configuration

`RIUS-WKS01` is now deployed and instrumented for endpoint monitoring.

- Sysmon installed and running.
- Custom Sysmon configuration loaded using schema version `4.91`.
- SHA256 hashing enabled.
- Process, network, file, registry, and DNS telemetry configured.
- Sysmon Event ID `3` network telemetry generated and validated in Event Viewer.
- Windows Logon auditing configured for both success and failure events.
- Simulated former employee account `ghost.user` created for the incident scenario.

## Project Roadmap

<!-- roadmap-start -->
- [x] Define the Operation Ghost Account insider-threat scenario
- [x] Create the `RIUS-WKS01` Windows 11 workstation
- [x] Move the workstation lab environment to Microsoft Azure
- [x] Configure Azure virtual networking and Network Security Group controls
- [x] Restrict and validate administrative RDP access
- [x] Install and configure Sysmon on `RIUS-WKS01`
- [x] Validate Sysmon network telemetry using Event ID 3
- [x] Enable Windows success and failure logon auditing
- [x] Create the simulated former employee account `ghost.user`
- [ ] Build the asset inventory and network architecture diagram
- [ ] Deploy the `RIUS-DC01` domain controller
- [ ] Configure Active Directory users, groups, and enterprise identities
- [ ] Document the failed offboarding controls and exposed access paths
- [ ] Forward Windows and Sysmon telemetry to Splunk
- [ ] Deploy the `RIUS-KALI01` authorized attacker system
- [ ] Write the rules of engagement and attack simulation plan
- [ ] Generate failed and successful Ghost Account authentication activity
- [ ] Simulate internal reconnaissance and suspicious PowerShell activity
- [ ] Simulate persistence, lateral movement, and data staging
- [ ] Develop Splunk detections, searches, and alerts
- [ ] Build SOC dashboards and tune false positives
- [ ] Investigate the incident and document the timeline, indicators, and MITRE ATT&CK mapping
- [ ] Write the incident report, root cause analysis, executive summary, and remediation plan
- [ ] Publish the final documentation, selected evidence, and interview walkthrough
<!-- roadmap-end -->

## Planned Attack Lifecycle

1. Retained account access
2. Internal reconnaissance
3. Suspicious authentication activity
4. PowerShell execution
5. Persistence
6. Credential and access discovery
7. Lateral movement
8. Data staging
9. Simulated exfiltration
10. SOC detection, containment, and recovery

## Planned Deliverables

- RIUS Enterprise company profile and incident charter
- Rules of engagement
- Asset inventory and network architecture diagram
- Attack simulation plan
- Splunk detection and SPL library
- SOC dashboards and alert documentation
- Investigation timeline and triage notes
- Indicators of compromise
- MITRE ATT&CK mapping
- Root cause and control gap analysis
- Incident report and executive summary
- Containment, recovery, and remediation plan
- Selected screenshots and supporting evidence
- Interview-ready project walkthrough

## Current Phase

`RIUS-WKS01` is live in Microsoft Azure with Sysmon and Windows authentication auditing enabled. The next phase is forwarding endpoint telemetry to Splunk and generating the controlled Ghost Account authentication and endpoint activity that will drive the SOC investigation.

## Safety and Authorization

All activity is performed inside an authorized personal lab using fictional identities and fictional company data. No testing is performed against systems without explicit authorization.
