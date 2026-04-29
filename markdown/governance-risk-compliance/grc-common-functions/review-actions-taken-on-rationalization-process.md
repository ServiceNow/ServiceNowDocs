---
title: Review actions taken on rationalization process
description: After acting on the recommendations, such as accepting as duplicate, retaining as primary, or dismissing during the rationalization process, the owner sends them for review to the configured reviewers. The reviewers then analyze the actions taken and either approve or reject them, providing proper justification for their decisions.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Generate recommendation for similar control objective, Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Review actions taken on rationalization process

After acting on the recommendations, such as accepting as duplicate, retaining as primary, or dismissing during the rationalization process, the owner sends them for review to the configured reviewers. The reviewers then analyze the actions taken and either approve or reject them, providing proper justification for their decisions.

## Before you begin

Role required: sn\_reco\_template.rationalization\_process\_writer and sn\_grc\_shared\_genai.compliance\_gen\_ai\_user

For more information on related roles, see [Roles installed with GRC: Policy and Compliance Management](../reference/r_InstallWPolAndCompl.md#).

## About this task

During the review process, the reviewer has several options to manage the actions taken by the owner on the recommended control objectives:

-   The reviewer can approve or reject the rationalization process based on their assessment of the actions taken by the owner.
-   The reviewer can change the actions taken by the owner. For example, if the owner dismissed a control objective, the reviewer can mark it as a duplicate instead and provide their justification for it.
-   The reviewer can view all impacts and associated items related to the control objectives and make necessary adjustments.
-   The reviewer can provide feedback on the rationalization process, which will be visible to the owner for further action.

**Note:** Changes made by the reviewer aren’t immediately reflected in the recommendations, instead, they’re captured in the summary, and the owner can then accept or reject these changes.

## Procedure

1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Control objectives** &gt; **All Control objectives**.

2.  Select ![](../../assessment-engine/image/list-icon.png).

3.  On the list, select the control objective under **Rationalize Process**.

4.  Review the recommendations and take the following actions:

    -   1.  Select **Approve**.
2.  In the **Justification for approval** dialog box, provide your reason for approval in the **Justification** field.
3.  Select **Approve**.
    -   1.  Select **Reject**.
2.  In the **Justification for rejection** dialog box, provide your reason for rejection in the **Justification** field.
3.  Select **Rejection**.

## What to do next

The owner can refer to the summary to view the reviewer's updates and feedback.

-   If the review is approved the owner can move to the consolidated state.
-   If the review is rejected, the owner can take the necessary actions and send for review again.

