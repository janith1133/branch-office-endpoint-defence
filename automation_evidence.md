automation_evidence.md

Automation Evidence

Purpose

This file explains the Docker automation evidence used in the lab.

Docker Role

Docker was used on FINANCE-ENDPOINT to show that a simple automation evidence layer was available.

Automation Log

The automation log recorded the following response decision:

Wazuh alert classified SUPPORT-ENDPOINT activity as high risk and linked it to an allowlisted remediation action.

Interpretation

The Docker evidence shows how an alert decision can be recorded and linked to a safe response action.

Scope

This was not a full production SOAR platform. It was a lab-based automation evidence layer.

Safety Control

The automation evidence did not allow unrestricted command execution. The remediation action was predefined, allowlisted and auditable.

Future Improvement

In a production setting, the automation layer should use Docker Compose, secure secrets, SIEM log forwarding and approval gates for high-impact actions.
