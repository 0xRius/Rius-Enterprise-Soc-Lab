# RIUS Enterprise SOC Attack & Detection Lab

![Status](https://img.shields.io/badge/Status-Active%20Development-blue)
<!-- progress-start -->
![Progress](https://img.shields.io/badge/Progress-20%25-red)
![Target Completion](https://img.shields.io/badge/Target-Sep%2012%2C%202026-green)

`████░░░░░░░░░░░░░░░░` **20%**
<!-- progress-end -->

## Project Overview

This project documents the development of a simulated enterprise security environment for RIUS Enterprise. The lab will generate realistic attack activity, collect endpoint telemetry, develop Splunk detections, and investigate the activity from a SOC analyst perspective.

## Planned Environment

- Windows 11 employee workstation
- Kali Linux attacker system
- Sysmon and Windows Security logging
- Splunk SIEM
- Isolated VirtualBox network
- Detection rules, dashboards, and alerts
- Incident investigation and reporting

## Project Roadmap

<!-- roadmap-start -->
- [x] Install and configure VirtualBox
- [x] Create RIUS-WKS01 virtual machine
- [ ] Complete workstation baseline and snapshot
- [ ] Deploy Sysmon and forward telemetry to Splunk
- [ ] Build the isolated RIUS Enterprise network
- [ ] Deploy the attacker virtual machine
- [ ] Execute and document the attack chain
- [ ] Develop and tune Splunk detections and dashboards
- [ ] Conduct the SOC investigation and MITRE ATT&CK mapping
- [ ] Publish the incident report and final documentation
<!-- roadmap-end -->

## Attack and Detection Workflow

Attacker activity → Windows endpoint → Sysmon and Windows logs → Splunk detections → SOC investigation → Incident report → MITRE ATT&CK

## Current Phase

Configuring the `RIUS-WKS01` employee workstation and establishing the initial Windows baseline.

## Disclaimer

All activity is performed inside an isolated personal lab environment for authorized educational purposes.
