---
title: Review the kill switch protocol log
description: The kill switch protocol log shows agents that you deactivated and reinstated for the instance. You can view audit log information for each AI agent which can help you stay compliant with regulatory guidance and your business rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Manage AI agents using kill switch protocol, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Review the kill switch protocol log

The kill switch protocol log shows agents that you deactivated and reinstated for the instance. You can view audit log information for each AI agent which can help you stay compliant with regulatory guidance and your business rules.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

## Procedure

1.  Navigate to **Security** &gt; **Overview** &gt; **Contained AI agents**.

    All contained AI agents are shown for the last 30 days.

    \[Omitted image "gov-sec-view-kill-switch-protocol-log.png"\] Alt text: Kill switch protocol log showing multiple deactivated AI agents and one AI agent reinstatement in progress.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Status

</td><td>

The current state of the operation. Possible values are:-   Completed — The operation was successful. If the agent was deactivated, all AI agent credentials were revoked across all providers, the session was ended, and no new access tokens will be provisioned. If the agent was reinstated, all AI agent credentials were restored across all providers.
-   Failed — The containment or reinstatement operation didn't take effect on any provider. Failed to deactivate or reinstate agent on all configured providers or skipped providers \(for example, agent not found, subflow error, or an unhandled exception\).
-   In progress — The operation is actively executing. Policy enforcement point \(PEP\) subflows \(for example, AWS Bedrock\) are running, with audit log information being captured.
-   Partial — The operation succeeded on at least one provider and failed on at least one provider. For example, the AWS Bedrock AI agent deactivation succeeded, but the Okta deactivation failed.


</td></tr><tr><td>

AI agent name

</td><td>

The name of the contained AI agent. Select the name to go to the AI asset in Inventory.

</td></tr><tr><td>

Start time

</td><td>

The date and time when the operation was initiated.

</td></tr><tr><td>

End time

</td><td>

The date and time when the operation ended, regardless of status.

</td></tr><tr><td>

Operation

</td><td>

The operation that was attempted. Possible values are:-   Deactivate
-   Reinstate


</td></tr></tbody>
</table>2.  To show contained AI agents for all time, select **Show all**.

3.  In an AI agent row, under **More actions**, select **View details**.

    Context, identity, enforcement, and audit log information is shown.


**Parent Topic:**[Manage AI agents using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md)

