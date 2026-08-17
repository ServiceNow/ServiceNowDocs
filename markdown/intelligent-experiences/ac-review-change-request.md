---
title: Review and approve a change request
description: Evaluate a change request submitted by an asset owner and either approve the change so AI Control Tower can apply it, or reject the change so the asset remains unchanged.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/ac-review-change-request.html
release: australia
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Change and offboarding requests, Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Review and approve a change request

Evaluate a change request submitted by an asset owner and either approve the change so AI Control Tower can apply it, or reject the change so the asset remains unchanged.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Activity Center** &gt; **Work** &gt; **Assigned to you**.

2.  Select the **Requests** sub-tab.

3.  Select the change request that you want to review.

    The change request opens in a side panel with three tabs: **Details**, **Change tasks**, and **Impacted assets**.

4.  Review the proposed changes on the **Details** tab.

    For example, compare the asset's current configuration with the values the requester has proposed for fields such as Asset type, Version, Updated AI Asset, Sub AI systems, and AI models. You can review the justification to understand the business context for the change.

5.  Review the work that the request will generate on the **Change tasks** tab.

    For example, view the tasks that will be created if the request is approved, along with their assignees and current state. A change request that switches an AI model might generate a "Review change request" task for the AI steward and a "Validate model performance" task for the asset owner.

6.  Assess the impact on related assets on the **Impacted assets** tab.

    For example, you might review impacted assets to determine whether the change might break a downstream dependency or require coordinated updates.

7.  Approve or reject the change request.

<table><thead><tr><th align="left" id="d182697e155">

Option

</th><th align="left" id="d182697e158">

Description

</th></tr></thead><tbody><tr><td id="d182697e164">

**Approve the request**

</td><td>

1.  Select **Approve**.
2.  If prompted, record the rationale for the approval.
3.  Confirm the approval. AI Control Tower applies the change to the asset and updates the asset record with the new values.


</td></tr><tr><td id="d182697e188">

**Reject the request**

</td><td>

1.  Select **Reject**.
2.  Record the rationale for the rejection so the requester understands why the change cannot proceed.
3.  Confirm the rejection. AI Control Tower closes the change request and the asset remains unchanged.


</td></tr></tbody>
</table>
## Result

If you approved the request, AI Control Tower applies the change to the asset and the request is marked **Completed**. If you rejected the request, the asset is unchanged and the request is closed. The asset owner receives a notification with the outcome and your rationale.

