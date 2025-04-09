# Threat Hunt Process

## 1. Preparation
- **Goal:** Investigate internal network performance degradation.
- **Hypothesis:** Lateral movement or internal scanning could be degrading network speed.
- **Assumptions:** All internal traffic is permitted, PowerShell is unrestricted.

## 2. Data Collection
- Gathered data from:
  - DeviceNetworkEvents
  - DeviceProcessEvents
  - DeviceFileEvents

## 3. Data Analysis
- Counted failed connections from devices.
- Observed excessive outbound failed connection attempts from `10.0.0.5`.

## 4. Investigation
- Used KQL to pivot into DeviceProcessEvents.
- Found `portscan.ps1` launched via PowerShell by user `labtestuser`.
- Matched patterns with MITRE ATT&CK techniques.

## 5. Response
- Isolated the VM `julius-mde-test`.
- Conducted a malware scan (result: clean).
- Submitted the system for re-imaging.

## 6. Documentation
- All queries, observations, and outcomes were documented in this repository.

## 7. Improvement
- Recommendation to restrict PowerShell access.
- Suggest implementing internal east-west traffic monitoring.
