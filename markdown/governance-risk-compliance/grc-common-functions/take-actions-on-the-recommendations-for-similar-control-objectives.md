---
title: Act on the recommendations for similar control objectives
description: Act on the recommendations by identifying, deduplicating, and rationalizing similar control objectives within the compliance library.
locale: en-US
release: australia
product: GRC Common Functions
classification: grc-common-functions
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Generate recommendation for similar control objective, Use generative AI skills, Now Assist, Common GRC features, Governance, Risk, and Compliance]
---

# Act on the recommendations for similar control objectives

Act on the recommendations by identifying, deduplicating, and rationalizing similar control objectives within the compliance library.

## Before you begin

Role required: sn\_reco\_template.rationalization\_process\_writer and sn\_grc\_shared\_genai.compliance\_gen\_ai\_user

For more information on related roles, see [Roles installed with GRC: Policy and Compliance Management](../reference/r_InstallWPolAndCompl.md#).

## About this task

Now Assist for Integrated Risk Management \(IRM\) introduces an AI-powered rationalization workflow that enables compliance managers and analysts to act on recommendations for similar control objectives. This process identifies duplicates, consolidates associations, and creates unified control objectives that are easier to support management and audit.

**Important:** Be sure to check AI-generated recommendations for accuracy.

## Procedure

1.  Navigate to **Workspaces** &gt; **Compliance Workspace**.

2.  Select ![](../../assessment-engine/image/list-icon.png).

3.  Navigate to **Rationalization process** &gt; **Control objectives**.

4.  Select the control objective that you want to review recommendations for and navigate to the **Rationalize** tab.

5.  Review the recommendation cards.

    Each recommendation card consists of the following information:

<table id="table_bmt_mj2_3hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the control objective.

</td></tr><tr><td>

Description

</td><td>

Description of the control objective.

</td></tr><tr><td>

Active

</td><td>

Whether the control objective is active or inactive

</td></tr><tr><td>

Comments

</td><td>

The field enables users \(owners and reviewers\) to provide feedback or contextual notes explaining decisions for actions taken.

 The comment count is dynamically updated on the card and in the Feedback trail \(Summary\) panel.

 Comments are sorted in descending order by latest activity, making it easy for users \(owners and reviewers\) to reply to existing comments.

</td></tr><tr><td>

View Summary

</td><td>

Provides a view of activities related to the recommendation card. In the Analyze State, it displays the recommendations summary. In the Consolidated State, it includes both the recommendation summary and the association summary.

</td></tr></tbody>
</table>6.  Select the control objective recommendation card and review the following sections:

    |Field|Description|
    |-----|-----------|
    |Name|Name of the control objective.|
    |Source|The origin or reference from which a control objective is derived.|
    |Description|Description and summary of the control objective.|
    |Supplemental guidance|Additional guidance about the control objective.|
    |**Evaluate Related Associations**|
    |Impacted items|Related lists that contain the items that are directly affected by the consolidation of the control objectives.|
    |Associated items|Related lists that contain all the associations from accepted control objectives in a consolidated view.|

7.  View the full record for a control objective by selecting the details icon \(![Details icon.](../../grc-privacy-management/image/details-icon.jpg)\).

8.  In the Analyze state, act on recommendations through a two-step process: Identify duplicates and Finalize.

    1.  In the Identify duplicates step, take one of the following actions on all the recommendations:

        -   Select **Accept as duplicate** to accept a recommendation as a duplicate.
        -   Select **Dismiss** to dismiss the recommendation.
        -   \(Optional\) In Comments, type a reason for the action taken on the recommendation.
        **Note:**

        A guidance message is shown for UCF recommendations indicating that the UCF control objective must be retained, and that unretained UCF recommendations will be automatically dismissed at the request review step because they cannot be deactivated. \(No such message is shown for non-UCF recommendations.\)

    2.  After taking actions on all the recommendations, select **Continue** and then select **Yes** in the confirmation dialog box.

    3.  In the Finalize step, select one accepted recommendation as **Retain as primary** to retain it as the primary control objective.

        A guidance message is shown for UCF recommendations indicating two things:

        -   Changing your selection for a UCF control objective automatically dismisses the previously retained UCF recommendation.
        -   Unretained UCF recommendations will be automatically dismissed when you request review, as they cannot be deactivated.
        Any UCF recommendations that were accepted but not retained are automatically dismissed at this point.

    4.  Alternatively, select **Create** to use generative AI to create a common control objective.

        **Note:** This AI-driven approach eliminates the need to retain a primary control objective manually. Generative AI automatically populates the name, description, and supplemental guidance fields and displays the consolidated objective on the form. It combines details from all the accepted control objectives into a single, new common control objective.

    5.  After the common control objective is created, do the following actions:

        -   Review the name, description, and supplemental guidance and select **Save**.
        -   To re-generate the name, description, and supplemental guidance fields, select **Generate**.
        -   To update the new common control objective after making any changes, select **Update**.
    **Note:**

    -   Only one control objective can be retained as primary. The information from all duplicate control objectives is combined into the primary objective.
    -   At least one retained control objective must be active for the rationalization process to move to the next state.
    -   When the retained primary control objective is deleted, the rationalization process doesn’t transition to the next state.
    -   When a control objective is deleted, its associations remain visible but are removed after the user initiates a transition to the next state.
    -   Any recommendations that are linked to a deleted control objective are also deleted.
    -   When an accepted control objective is deactivated, all impacted items are automatically moved to inactive state.
9.  Select **Request review**.

    -   For more information on review request, see [Review actions taken on rationalization process](review-actions-taken-on-rationalization-process.md).
    -   The actions you take on the recommendations are sent for review to the configured reviewers. The reviewer can accept or reject your actions and provide their justifications.
10. Select **Summary**.

    Analyze the reviewer feedback and act on it as necessary.

11. After the **Analyze** state is approved, select **Consolidate**.

    This action consolidates the details of all the accepted control objectives.

12. Review all the impacted items and associations and take one of the following actions on the associations:

    -   Accept the association by selecting **Accept** and then selecting **Confirm**.
    -   Remove an association by selecting **Dismiss** and then selecting **Confirm**.
    **Note:**

    -   By default, all associations are in the Accepted state. You can select an association and choose to dismiss or accept the association as is.
    -   The related items are impacted items and associations that are affected by consolidating the accepted control objectives.
    -   Impacted and associated items display pre-calculated data, updated daily. Since recommendations can change this data, select **Sync Related Items** to sync in real-time and view the latest data on impacted items and associations.
13. To approve the Consolidated step, initiate the review process by selecting **Request review**.

    The reviewer can review the action taken by the owner on all the impacted items. The reviewer can accept or reject your actions and provide their justifications. They can also act on the associations that are captured in the summary. For more information, see [Review actions taken on rationalization process](review-actions-taken-on-rationalization-process.md).

14. Select the bulb icon on the right to access the Feedback trail section.

    The Feedback trail section provides a chronological overview of all user actions taken on the recommendations. The following details are captured for each action:

    -   **User Identity**: The user who performed the action.
    -   **Action Type**: Whether the control objective was Accepted, Retained, or Dismissed.
    -   **Justification**: The reason provided for the action taken.
    -   **Control Objective**: The specific control objective associated with the action.
    -   **Last Update**: The most recent status or change related to the action.
    This structured format allows for clear tracking and understanding of the actions taken by users.

15. Reset the rationalization process to the Analyze state by selecting **Restart Analyze**.

    The **Restart Analyze** option allows you to re-evaluate identified recommendations by returning to the **Identify Duplicates** step. While previous actions on the recommendations are retained, you have the opportunity to re-decide whether to accept or dismiss them.

16. After the **Consolidate** state is approved, select **Confirm** and then **Confirm** to complete the rationalization process.

    The Consolidated state page now displays the retained and accepted control objectives with their associated items. This change provides you with an improved context for the rationalization process.

    After the confirmation, the following changes happen:

    -   The state of the rationalization process is moved to closed.
    -   The accepted control objectives are retired and all their details and associations are merged into the retained control objective.
    -   The impacted items are retired.

