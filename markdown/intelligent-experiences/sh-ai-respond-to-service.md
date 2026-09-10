---
title: Triage a detected AI service
description: Triage a detected AI service according to its traffic, usage, or potential risk.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/sh-ai-respond-to-service.html
release: australia
topic_type: task
last_updated: "2026-08-25"
reading_time_minutes: 2
keywords: [Shadow AI, respond, escalate, snooze, dismiss, block]
breadcrumb: [Investigate a detected AI service, Detecting shadow AI, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Triage a detected AI service

Triage a detected AI service according to its traffic, usage, or potential risk.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

After reviewing a detected AI service's usage and exposure, decide how to respond.

For worked examples of choosing between options, see [Shadow AI triage examples](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-triage-scenarios.md).

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Inventory** &gt; **Shadow AI**.

2.  Select the detected AI service you want to respond to.

3.  Triage the detected AI service by choosing the action that you want to take.

<table><thead><tr><th align="left" id="d186450e127">

Action

</th><th align="left" id="d186450e130">

Steps

</th></tr></thead><tbody><tr><td id="d186450e136">

**__Snooze for 7 days__**

</td><td>

1.  Select **Actions**.
2.  Allow more time or context to surface by selecting **Snooze for 7 days**.
 The status changes to **Snoozed** and the service is deprioritized for 7 days, then returns to **New** once new traffic is detected.

</td></tr><tr><td id="d186450e170">

**__Dismiss__**

</td><td>

1.  Select **Actions**.
2.  Address a known, low-risk pattern that might come back by selecting **Dismiss**.
 The status changes to **Dismissed**. However, the **Dismiss** action leaves the registry entry active, so a dismissed service returns as a new detection the next time it sees traffic.

</td></tr><tr><td id="d186450e204">

**__Block__**

</td><td>

1.  Select **Actions**.
2.  Block a service that presents risk or has no legitimate business use by selecting **Block**.
3.  In the dialog box that appears, select the scope for the block.
    -   **AI service** blocks the service for all users in your organization with Agent Client Collector \(ACC\) installed. The service status changes to **Blocked**.
    -   **Users** blocks the service for specific users. The service status changes to **Partially blocked**.
4.  If you selected **Users**, select each person to block in the **Who is blocked** field.
5.  Enter why you're blocking the service in **Reason \(logged\)**.
6.  Review the policy details, and then select **Block**.
 Blocking creates a policy in AI Control Tower and is enforced only on devices running the ACC agent. To extend a block's reach, deploy the agent to more devices. See [Connect Agent Client Collector to detect AI use](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-connect-acc.md).

</td></tr><tr><td id="d186450e285">

**__This is not Shadow AI__**

</td><td>

1.  Select **Actions**.
2.  Flag a misclassified detection that isn't actually an AI service by selecting **This is not Shadow AI**.
3.  Select **Remove** to confirm.
 This option marks the matching domain as **Not Shadow AI** in the registry.

 Shadow AI continues collecting traffic for this service for 30 days before removing it, then stops reporting it. To reverse this before or after that window, mark the domain active again. See [Manage the AI services registry](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-manage-registry.md).

</td></tr></tbody>
</table>
**Parent Topic:**[Investigating a detected AI service in Shadow AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/sh-ai-investigating-detected-services.md)

