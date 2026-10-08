---
title: Delete a policy
description: Remove a policy you no longer need.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/intelligent-experiences/gov-pol-delete-policy.html
release: australia
topic_type: task
last_updated: "2026-08-27"
reading_time_minutes: 1
keywords: [ServiceNow Otto, AI Agents, generative AI, agentic AI, Policies, Explicit Block, Threat Response, delete]
breadcrumb: [Manage policies, Controlling AI asset usage, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Delete a policy

Remove a policy you no longer need.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## About this task

A policy has no pause or disable state. You must delete the policy to end enforcement.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Govern** &gt; **Policies**.

2.  Find the policy you want to remove.

3.  In the More actions menu, select **Delete**.

4.  In the confirmation dialog box, select **Delete policy**.

    Deleting a policy can't be undone. Activity from the deleted policy stays available in the **Enforcement activity** tab.


## Result

What happens next depends on the policy type.

-   **Threat Response**

    The policy stops responding to new detections. An agent it already took offline stays offline; reinstate it separately from Security. For details, see [Contain AI agents manually using kill switch protocol](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/intelligent-experiences/gov-sec-manage-ai-agents-using-kill-switch-protocol.md).

-   **Explicit Block**

    Access is restored at every enforcement point the policy applied to.


