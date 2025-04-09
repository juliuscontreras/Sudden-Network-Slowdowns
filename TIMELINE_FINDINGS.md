# Timeline Summary and Findings

## Initial Suspicion
- The IT team reported slow performance on older servers.
- Investigation revealed excessive failed network connections.

## Network Indicators
- Host: `julius-mde-test`
- IP: `10.0.0.5`
- Unusual pattern of failed connection attempts to multiple hosts.

## Suspicious Activity
- DeviceProcessEvents revealed a PowerShell script `portscan.ps1` executed by `labtestuser`.

## Action Taken
- Host isolated.
- Script manually verified.
- No malware detected, host sent for reimaging.

## Conclusion
Unauthorized PowerShell usage was the root cause of the port scanning activity. Account misuse or potential lateral movement was suspected.
