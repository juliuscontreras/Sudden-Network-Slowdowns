# Threat Hunt: Internal Network Performance Degradation (Port Scan via PowerShell)

## Overview

This repository contains documentation and artifacts from a threat hunt that investigated internal network slowdowns in the 10.0.0.0/16 range. The issue was ultimately traced back to unauthorized PowerShell-based port scanning.

## 📁 Contents

- [Threat Hunt Steps](./THREAT_HUNT_STEPS.md)
- [Timeline and Findings](./TIMELINE_FINDINGS.md)
- [MITRE ATT&CK Mapping](./MITRE_MAPPING.md)
- [KQL Queries](./QUERIES)

## 🔍 Summary

- A suspected internal scanning activity was causing network degradation.

![image](https://github.com/user-attachments/assets/993b1a34-83bc-47e3-b4e0-f21515775322)

- Investigation revealed PowerShell-based port scanning from a VM.

![image](https://github.com/user-attachments/assets/8d5658a2-c3ca-4680-8eba-62c912752538)

![image](https://github.com/user-attachments/assets/5bb02af4-16ad-4a85-bf18-6a4fd51fc7a6)


- Unauthorized use of the `labtestuser` account was noted.

![image](https://github.com/user-attachments/assets/8e87862e-5802-41b6-9ac4-8e2307d7fb44)

- Logged into the suspect computer and observed the powershell script that was used to conduct the port scan.

![image](https://github.com/user-attachments/assets/1a66d92c-cf8d-4a03-a616-f1182ce5290e)

- Device was isolated, investigated, and reimaged as a precaution.

![image](https://github.com/user-attachments/assets/ad3e0821-118f-4320-aa49-9e7f63cb91ae)
