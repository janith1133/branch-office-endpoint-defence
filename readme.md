Branch Office Endpoint Defence Lab

Project Overview

This repository contains the supporting artefacts for an endpoint security monitoring and response lab. The lab was designed for a small branch office environment where endpoint activity must be monitored through a central SIEM.

The project uses Wazuh as the SIEM platform, FINANCE-ENDPOINT as the Ubuntu endpoint, SUPPORT-ENDPOINT as the Windows endpoint and Docker as the automation evidence layer.

Lab Components

BRANCH-SIEM

Role: Wazuh SIEM server

IP address: 10.10.80.30

FINANCE-ENDPOINT

Role: Ubuntu endpoint used for monitoring, security event evidence and remediation

IP address: 10.10.80.20

SUPPORT-ENDPOINT

Role: Windows endpoint and containment target

IP address: 10.10.80.10

Docker automation layer

Role: Simple automation evidence hosted on FINANCE-ENDPOINT

Architecture Summary

The lab follows a branch office endpoint defence design. FINANCE-ENDPOINT sends endpoint activity to BRANCH-SIEM. SUPPORT-ENDPOINT is included as the Windows endpoint and containment target. BRANCH-SIEM provides the Wazuh dashboard and agent monitoring view. Docker on FINANCE-ENDPOINT records alert classification and response evidence.

Evidence Collected

VirtualBox VM list showing the lab systems.

BRANCH-SIEM IP configuration.

FINANCE-ENDPOINT IP configuration and connectivity to BRANCH-SIEM.

SUPPORT-ENDPOINT IP configuration.

Wazuh Agents page showing FINANCE-ENDPOINT active.

Wazuh security events from FINANCE-ENDPOINT.

UFW containment rule blocking SUPPORT-ENDPOINT.

Docker automation evidence.

Containment Logic

The lab used SUPPORT-ENDPOINT as the containment target. The IP address 10.10.80.10 was blocked using UFW from FINANCE-ENDPOINT. The rule was verified using the numbered UFW status output. A rollback command was also included to show that the action was reversible.

Safety Statement

The lab was completed in an isolated virtual network. No real malware was used. No public systems were targeted. The response action was limited to a safe UFW rule and could be rolled back.

Limitation

The strongest SIEM evidence came from FINANCE-ENDPOINT because it was actively connected to Wazuh and produced visible security events. SUPPORT-ENDPOINT was used as the Windows endpoint and containment target, but Windows telemetry evidence was limited and recorded as a lab limitation.
