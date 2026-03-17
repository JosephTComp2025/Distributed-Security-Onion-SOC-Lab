
# Distributed Security Onion SOC Lab

## Overview
- **Goal:** Build a distributed Security Onion deployment that mirrors a small SOC environment which includes a Windows Server domain controller and a Windows 10 workstation joined to the domain.

- **Role:** Architect, implementer, and analyst.
- **Focus:** Detection, visibility, and repeatable workflows.

## Architecture

- **ManagerSearch:** [securityonion], [20GB Ram], [network role]
- **Sensor:** [sensor), [10GB Ram], [2 wired nics via usb adapters]
- **Network:** Utilziing a managed switch, one wired nic connected via manager switch, one wired nic connected from the sensor to the mirror port and one wired nic connected to a gneral port on the switch)


## Deployment Highlights

- Clean hostname and Salt key alignment between manager and sensor.
- Documented install steps for:
  - Manager (`deployment-notes/manager-setup.md`)
  - Sensor (`deployment-notes/sensor-setup.md`)
- Troubleshooting log:
  - Salt state errors
  - Hostname mismatches
  - Key re-registration
  -  Windows Server 2019
- Active Directory Domain Services
- Centralized authentication and Kerberos ticketing
- Logs forwarded to Security Onion via Winlogbeat
- Sysmon installed for process-level visibility
- - Windows 10 Enterprise
- Joined to the domain
- Configured as the primary victim host for attack simulations
- Sysmon + Winlogbeat forwarding to Security Onion
- Used for phishing, malware execution, credential harvesting, and lateral movement tests

## Detection Scenarios

Each scenario has:
- **Attack simulation**
- **What Security Onion saw**
- **How an analyst would respond**



## SOC Playbooks

- Short, actionable playbooks for each scenario:
  - Where to look in Security Onion
  - Key pivots and fields
  - Decision points


## Lessons Learned

- Design decisions
- What broke and how it was fixed
- How this lab maps to a real SOC environment



