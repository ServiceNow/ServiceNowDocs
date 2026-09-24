---
title: Review the agent containment list
description: The agent containment list shows agents that were deactivated and reinstated for the instance manually with kill switch protocol or automatically by policy enforcement. You can view audit log information for each AI agent which can help you stay compliant with regulatory guidance and your business rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI]
breadcrumb: [Contain AI agents manually using kill switch protocol, Managing AI asset security, Govern AI assets, AI Control Tower, Establishing AI governance, Enable AI Experiences]
---

# Review the agent containment list

The agent containment list shows agents that were deactivated and reinstated for the instance manually with kill switch protocol or automatically by policy enforcement. You can view audit log information for each AI agent which can help you stay compliant with regulatory guidance and your business rules.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

## Procedure

1.  Navigate to **Security** &gt; **Overview** &gt; **Contained AI Agents**.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

The current state of the operation. Possible values are:-   Completed — The operation succeeded on every configured enforcement point. If the agent was deactivated, it was deactivated on its runtime platform. Also, if an identity provider is configured, its session tokens were revoked and no new access tokens are issued. If the agent was reinstated, access was restored on every configured enforcement point.
-   Failed — The containment or reinstatement operation didn't take effect on any configured enforcement point. Failed to deactivate or reinstate agent on all configured enforcement points or skipped them \(for example, agent not found, subflow error, or an unhandled exception\).
-   In progress — The operation is actively executing. Control enforcement point \(CEP\) subflows \(for example, AWS Bedrock\) are running, with audit log information being captured.
-   Partial — The operation succeeded on at least one control enforcement point and failed on at least one point. For example, the AWS Bedrock AI agent deactivation succeeded, but the Okta token revocation failed.


</td></tr><tr><td>

AI agent name

</td><td>

The name of the contained AI agent. Select the name to go to the AI asset in Inventory.

</td></tr><tr><td>

Start time

</td><td>

The date and time when the operation was initiated, shown in Coordinated Universal Time \(UTC\).

</td></tr><tr><td>

End time

</td><td>

The date and time when the operation ended, regardless of status, shown in Coordinated Universal Time \(UTC\).

</td></tr><tr><td>

Domain

</td><td>

The domain the AI agent belongs to. If global or null is shown, the instance isn't domain-separated.

</td></tr><tr><td>

Operation

</td><td>

The operation that was attempted. Possible values are:-   Deactivate
-   Reinstate


</td></tr><tr><td>

Actions

</td><td>

Select one of the following:-   **View details** — Opens a side panel with two subtabs: **Overview** and **Audit log**. The Overview subtab shows containment context \(including trigger type of Manual or Automated\) and identity and enforcement information.
-   **Reinstate agent** — Make the AI agent active again.


</td></tr></tbody>
</table>2.  Select **All**, **In progress**, or **Contained** to filter the list.


**Parent Topic:**[Contain AI agents manually using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md)

