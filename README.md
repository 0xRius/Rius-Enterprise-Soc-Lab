<p align="center">
  <img src="assets/Rius%20Enterprise%20lab%20image.png" alt="RIUS Enterprise headquarters" width="100%">
</p>

# Operation Ghost Account: The RIUS Enterprise Insider Incident

> A full-scale SOC attack, detection, and incident response case study built inside the fictional RIUS Enterprise environment.

![Status](https://img.shields.io/badge/Status-Active%20Development-blue)
<!-- progress-start -->
![Progress](https://img.shields.io/badge/Progress-10%25-red)
![Target Completion](https://img.shields.io/badge/Target-Sep%2012%2C%202026-green)

`██░░░░░░░░░░░░░░░░░░` **10%**
<!-- progress-end -->

## Project Overview

Operation Ghost Account follows a simulated insider threat incident at RIUS Enterprise, a fictional technology services company. The project covers the full incident lifecycle, including the security failures that made the attack possible, attack simulation, log collection, Splunk detection engineering, SOC investigation, containment, and reporting.

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

- Build a realistic small enterprise environment with centralized identity.
- Generate controlled attack activity inside an isolated virtual lab.
- Collect Windows, Sysmon, authentication, process, and network telemetry.
- Develop and tune Splunk searches, alerts, detections, and dashboards.
- Investigate the incident from a SOC analyst perspective.
- Map the observed activity to MITRE ATT&CK.
- Identify the root cause and failed security controls.
- Produce an incident report, executive summary, and remediation plan.

## Planned Environment

| System | Purpose |
|---|---|
| `RIUS-DC01` | Windows Server domain controller and Active Directory |
| `RIUS-WKS01` | Windows 11 employee workstation |
| `RIUS-KALI01` | Authorized attacker workstation |
| Splunk SIEM | Centralized logging, detection, alerting, and investigation |
| Sysmon | Detailed Windows process and endpoint telemetry |
| VirtualBox Network | Isolated RIUS Enterprise lab network |

Due to host memory limitations, the virtual machines will be operated in stages when necessary.

## Project Roadmap

<!-- roadmap-start -->
- [x] Install and configure VirtualBox
- [x] Create the `RIUS-WKS01` virtual machine
- [ ] Complete the Windows workstation baseline and clean snapshot
- [ ] Create the RIUS Enterprise company profile and incident charter
- [ ] Build the asset inventory and network architecture diagram
- [ ] Configure the isolated VirtualBox lab network
- [ ] Deploy the `RIUS-DC01` domain controller
- [ ] Configure Active Directory users, groups, and the former employee identity
- [ ] Document the failed offboarding controls and exposed access paths
- [ ] Deploy Sysmon and Windows audit policies
- [ ] Forward workstation and domain controller telemetry to Splunk
- [ ] Deploy the `RIUS-KALI01` authorized attacker system
- [ ] Write the rules of engagement and attack simulation plan
- [ ] Simulate retained account access and internal reconnaissance
- [ ] Simulate PowerShell, persistence, lateral movement, and data staging
- [ ] Develop Splunk detections, searches, and alerts
- [ ] Build SOC dashboards and tune false positives
- [ ] Investigate the incident and document the timeline, indicators, and MITRE ATT&CK mapping
- [ ] Write the incident report, root cause analysis, executive summary, and remediation plan
- [ ] Publish the final documentation and interview walkthrough
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
- Interview ready project walkthrough

## Current Phase

Building and configuring the `RIUS-WKS01` employee workstation while establishing the RIUS Enterprise incident scenario and project foundation.

## Safety and Authorization

All activity is performed inside an isolated personal lab using fictional identities and fictional company data. No testing is performed against systems without explicit authorization.
