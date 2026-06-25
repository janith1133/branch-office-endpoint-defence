Lab Design

Scenario

The lab represents a small branch office environment. The organisation needs visibility over endpoint activity and a safe way to contain suspicious endpoint communication.

Network Design

The lab used a private internal network with the 10.10.80.0/24 address range.

BRANCH-SIEM used 10.10.80.30.

FINANCE-ENDPOINT used 10.10.80.20.

SUPPORT-ENDPOINT used 10.10.80.10.

Monitoring Flow

FINANCE-ENDPOINT sent Linux security telemetry to BRANCH-SIEM.

SUPPORT-ENDPOINT was used as the Windows endpoint and containment target.

BRANCH-SIEM provided the Wazuh dashboard and agent monitoring view.

Docker on FINANCE-ENDPOINT provided automation evidence.

Why This Design Was Used

This design separates monitoring, endpoint activity and response evidence. The SIEM is used for visibility. The endpoints are used for telemetry and containment evidence. Docker is used to show how automation logic could support response decisions.

Evidence Mapping

Agent visibility was shown through the Wazuh Agents page.

Authentication and security telemetry was shown through Wazuh security events.

Containment was shown through the UFW deny rule.

Automation was shown through the Docker evidence log.
