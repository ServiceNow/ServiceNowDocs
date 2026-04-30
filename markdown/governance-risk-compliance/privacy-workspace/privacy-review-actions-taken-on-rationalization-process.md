---
title: Review actions taken on rationalization process
description: After acting on the recommendations, the owner sends it for review to the configured reviewers. The reviewers then analyze the actions taken and either approve or reject them, providing proper justification for their decisions.
locale: en-US
release: zurich
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use Recommendation of similar control objectives skill to generate suggestions, Now Assist for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# Review actions taken on rationalization process

After acting on the recommendations, the owner sends it for review to the configured reviewers. The reviewers then analyze the actions taken and either approve or reject them, providing proper justification for their decisions.

## Before you begin

Role required: sn\_reco\_template.rationalization\_process\_writer and sn\_grc\_shared\_genai.compliance\_gen\_ai\_user

## About this task

During the review process, the reviewer has several options to manage the actions taken by the owner on the recommended control objectives:

-   The reviewer can approve or reject the recommendations based on their assessment of the actions taken by the owner.
-   If the owner of a control objective is also listed as a reviewer in the approval configuration, their approval is skipped automatically and the rationalization process moves to the next state.
-   The reviewer can change the actions taken by the owner. For example, if the owner dismissed a control objective as not duplicate, the reviewer can mark it as a duplicate instead and provide their justification for it.
-   The reviewer can view all impacts and associated items related to the control objectives and make necessary adjustments.
-   The reviewer can provide feedback on the recommendations, which will be visible to the owner for further action.

**Note:** Changes made by the reviewer aren’t immediately reflected in the recommendations, instead, they’re captured in the summary, and the owner can then accept or reject these changes.

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the List icon.

3.  Navigate to **Library** &gt; **Control Objectives**.

4.  Select the control objective that you want to approve.

5.  In the control objective page, navigate to the **Rationalize** tab.

6.  Review the recommendations and take appropriate actions.

    For example, if you believe a recommendation should be accepted as a duplicate, even if the owner has dismissed it, you can still accept it as a duplicate. Your justification will appear as a comment on the recommendation card, visible to the owner for their review and action. it will also appear in the Feedback trail \(Summary\) panel.

7.  After reviewing the recommendations, take the following actions:

    -   1.  Select **Reject**.
2.  In the **Justification for rejection** dialog box, provide your reason for rejection in the **Justification** field.
3.  Select **Rejection**.
    -   1.  Select **Approve**.
2.  In the **Justification for approval** dialog box, provide your reason for approval in the **Justification** field and select **Submit**.

## What to do next

The owner can refer to the summary to view the reviewer's updates and feedback.

-   If the review is approved, the owner can move to the consolidated state.
-   If the review is rejected, the owner can take the necessary actions and send for review again.

