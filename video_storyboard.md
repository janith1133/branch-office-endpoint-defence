

Video Storyboard

Video Title

Branch Office Endpoint Defence Lab

Opening

Introduce the project as an endpoint security monitoring and response lab for a branch office environment.

Mention that Wazuh was used as the SIEM platform, FINANCE-ENDPOINT was used as the Ubuntu endpoint, SUPPORT-ENDPOINT was used as the Windows endpoint and Docker was used as the automation evidence layer.

Part 1: GitHub Repository

Show the GitHub repository named branch-office-endpoint-defence.

Briefly show the README, lab design, alert catalogue, containment runbook, automation evidence and proof index.

Part 2: Architecture

Show the architecture diagram.

Explain that BRANCH-SIEM receives endpoint evidence, FINANCE-ENDPOINT provides Linux security telemetry, SUPPORT-ENDPOINT is the containment target and Docker records the response decision.

Part 3: IP Plan

Show BRANCH-SIEM with IP address 10.10.80.30.

Show FINANCE-ENDPOINT with IP address 10.10.80.20.

Show SUPPORT-ENDPOINT with IP address 10.10.80.10.

Part 4: Wazuh Agent Visibility

Show the Wazuh Agents page.

Explain that FINANCE-ENDPOINT is active and visible in Wazuh.

Part 5: Security Events

Show FINANCE-ENDPOINT security events in Wazuh.

Explain that the events support the detection evidence for authentication and privileged activity.

Part 6: Remediation

Show the UFW deny rule blocking 10.10.80.10.

Explain that SUPPORT-ENDPOINT was used as the containment target.

Show that the action is reversible using the rollback command.

Part 7: Docker Automation Evidence

Show the Docker automation evidence.

Explain that the alert was classified as high risk and linked to an allowlisted response action.

Part 8: Limitations

Explain that the strongest SIEM evidence came from FINANCE-ENDPOINT.

Mention that Windows telemetry evidence was limited and recorded as a lab limitation.

Part 9: Conclusion

Summarise that the lab demonstrated endpoint visibility, Wazuh monitoring, security event review, UFW containment, Docker automation evidence and rollback planning.
