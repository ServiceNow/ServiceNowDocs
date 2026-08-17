---
title: Review and approve an offboarding request
description: Evaluate an offboarding request submitted by an asset owner and either approve the request to move the asset into the offboarding lifecycle, or reject the request so the asset remains active.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/ac-review-offboarding-request.html
release: zurich
topic_type: task
last_updated: "2026-07-16"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Change and offboarding requests, Manage tasks and approvals, Address action items, AI Control Tower, Enable AI experiences]
---

# Review and approve an offboarding request

Evaluate an offboarding request submitted by an asset owner and either approve the request to move the asset into the offboarding lifecycle, or reject the request so the asset remains active.

## Before you begin

Role required: sn\_ai\_governance.ai\_steward

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Activity Center** &gt; **Work** &gt; **Assigned to you**.

2.  Select the **Requests** sub-tab.

3.  Select the offboarding request that you want to review.

    The offboarding request opens in a side panel with the asset details, the requester's justification, and the dependencies that the asset has.

4.  Review the offboarding rationale and the asset's current state.

    For example, evaluate whether the asset has had recent activity, whether the requester has identified a replacement asset, and whether retiring the asset will affect users or downstream systems.

5.  Assess the impact of retiring the asset by reviewing related sub-AI systems, AI models, and other dependencies in the request.

    For example, identify any downstream assets that depend on the one being retired so you can confirm whether they have been migrated to a replacement or whether additional planning is needed before approval.

6.  Approve or reject the offboarding request.

<table><thead><tr><th align="left" id="d38846e128">

Option

</th><th align="left" id="d38846e131">

Description

</th></tr></thead><tbody><tr><td id="d38846e137">

**Approve the request.**

</td><td>

1.  Select **Approve**.
2.  If prompted, record the rationale for the approval.
3.  Confirm the approval. AI Control Tower moves the asset into the offboarding lifecycle stage and generates the offboarding tasks defined by the offboarding playbook.


</td></tr><tr><td id="d38846e161">

**Reject the request.**

</td><td>

1.  Select **Reject**.
2.  Record the rationale for the rejection so the requester understands why the asset cannot be retired at this time.
3.  Confirm the rejection. AI Control Tower closes the offboarding request and the asset remains active.


</td></tr></tbody>
</table>
## Result

If you approved the request, the asset moves into offboarding and lifecycle tasks are generated to complete the retirement. If you rejected the request, the asset remains active. The asset owner receives a notification with the outcome and your rationale.

