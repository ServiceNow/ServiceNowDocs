---
title: Manage AI agents using kill switch protocol
description: Deactivate or reinstate AI agents using kill switch protocol to eliminate malicious activity and improve your security posture.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.html
release: zurich
topic_type: task
last_updated: "2026-07-21"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Manage AI agents using kill switch protocol

Deactivate or reinstate AI agents using kill switch protocol to eliminate malicious activity and improve your security posture.

## Before you begin

Role required: AI steward \[sn\_ai\_governance\_ai\_steward\]

Make sure that you have configured connectors and optional identity providers for AI agent containment. For more information, see [Configure AI agent containment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-ai-agent-containment.md).

## About this task

## Procedure

1.  In AI Control Tower, navigate to **Govern** &gt; **Security** &gt; **Overview** &gt; **Your top recommendations**.

    Alternatively, you can navigate to **Activity Center** &gt; **Recommendations**.

2.  Open Critical AI asset events.

3.  Select and view the AI asset associated with the critical event.

    A banner appears informing you that there is malicious activity detected for this AI asset.

4.  On the banner, select **View details**.

    \[Omitted image "gov-sec-malicious-activity-banner.png"\] Alt text: Banner indicating that malicious activity was detected for the AI agent.

    A pane appears with information about the activity detected for this AI asset, and the next best action to take.

5.  Select **Deactivate**.

    \[Omitted image "gov-sec-malicious-activity.png"\] Alt text: Malicious activity evidence shown for an agent.

6.  Provide the reason for the deactivation and select **Deactivate**.

    \[Omitted image "gov-sec-deactivate-agent-confirmation.png"\] Alt text: Deactivation confirmation with a prompt to enter the reason for deactivating the AI agent.

    The banner on the AI asset changes to reflect the progress of deactivation.

7.  Select **View kill switch protocol log** to track the progress of the deactivation.

    \[Omitted image "gov-sec-view-kill-switch-protocol-log-banner.png"\] Alt text: In progress banner message with a View kill switch protocol log button.

    For more information, see [Review the kill switch protocol log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.md).

8.  After deactivation is complete, you can reinstate the AI agent by resolving the critical security task for the AI agent first.

9.  Navigate to **Security** &gt; **Overview** &gt; **Contained AI agents**.

10. In the AI agent row, under **More actions**, select **Reinstate**.

11. Enter a reason for reinstating the AI agent and select **Reinstate**.


-   **[Review the kill switch protocol log](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-review-kill-switch-protocol-log.md)**  
The kill switch protocol log shows agents that you deactivated and reinstated for the instance. You can view audit log information for each AI agent which can help you stay compliant with regulatory guidance and your business rules.

**Parent Topic:**[Managing AI asset security with AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-landing.md)

