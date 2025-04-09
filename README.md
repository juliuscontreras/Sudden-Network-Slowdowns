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
- Investigation revealed PowerShell-based port scanning from a VM.
- Unauthorized use of the `labtestuser` account was noted.
- Device was isolated, investigated, and reimaged as a precaution.
