---
title: Contain AI agents manually using kill switch protocol
description: Deactivate or reinstate AI agents using kill switch protocol to eliminate malicious activity and improve your security posture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.html
release: australia
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Contain AI agents manually using kill switch protocol

Deactivate or reinstate AI agents using kill switch protocol to eliminate malicious activity and improve your security posture.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

Make sure that you have configured connectors and optional identity providers for AI agent containment. For more information, see [Configure AI agent containment using kill switch protocol manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-configure-ai-agent-containment.md).

## About this task

You can manually deactivate an AI agent two ways. If a security event is detected for the agent, a banner appears indicating that malicious activity was detected for the AI asset, offering deactivation, as described in the following steps.

You can also manually deactivate any managed AI agent directly, whether or not it has an associated security event, by opening the AI asset record and, from the **Actions** menu, selecting **Deactivate Agent**. This option is available only for managed AI agents. For details, see [Deactivate a managed AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/disc-contain-managed-asset.md).

**Note:** To contain AI agents automatically through policy enforcement, see [Controlling AI asset usage in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-pol-landing.md).

## Procedure

1.  In AI Control Tower, navigate to one of the following:

    -   **Govern** &gt; **Security** &gt; **Overview** &gt; **Your top recommendations**
    -   **Activity Center** &gt; **Recommendations**
    -   The AI asset record's **Overview** tab or **Security** tab, for AI agents in the Agentic AI category.
2.  Open an AI asset event of any severity \(Critical, High, Medium, or Low\).

3.  Select and view the AI asset associated with the critical event.

    A banner appears informing you that there is malicious activity detected for this AI asset.

4.  On the banner, select **View containment options**.

    \[Omitted image "gov-sec-malicious-activity-banner.png"\] Alt text: Banner indicating that malicious activity was detected for the AI agent.

    A pane appears with information about the activity detected for this AI asset, and the next best action to take.

5.  Select **Deactivate**.

    \[Omitted image "gov-sec-malicious-activity.png"\] Alt text: Malicious activity evidence shown for an agent.

6.  Provide the reason for the deactivation and select **Deactivate**.

    \[Omitted image "gov-sec-deactivate-agent-confirmation.png"\] Alt text: Deactivation confirmation with a prompt to enter the reason for deactivating the AI agent.

    The banner on the AI asset changes to reflect the progress of deactivation.

7.  If the deactivation status shows as Failed or Partial, select **Retry** on the banner.

8.  Select **View agent containment list** to track the progress of the deactivation.

    \[Omitted image "gov-sec-view-kill-switch-protocol-log-banner.png"\] Alt text: In progress banner message with a View agent containment list button.

    For more information, see [Review the agent containment list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.md).

9.  After deactivation is complete, you can reinstate the AI agent by resolving the critical security task for the AI agent first.

10. Navigate to **Security** &gt; **Overview** &gt; **Contained AI Agents**.

11. In the AI agent row, under **Actions**, select **Reinstate**.

12. Enter a reason for reinstating the AI agent and select **Reinstate**.


-   **[Review the agent containment list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.md)**  
The agent containment list shows agents that were deactivated and reinstated for the instance manually with kill switch protocol or automatically by policy enforcement. You can view audit log information for each AI agent which can help you stay compliant with regulatory guidance and your business rules.

**Parent Topic:**[Managing AI asset security with AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/gov-sec-landing.md)

