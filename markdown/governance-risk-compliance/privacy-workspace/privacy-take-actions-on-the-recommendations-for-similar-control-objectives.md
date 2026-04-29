---
title: Act on the recommendations for similar control objectives
description: Act on the recommendations, like accept as duplicate, retain as primary, or dismiss, to enable your compliance managers and analysts to streamline their processes by identifying, deduplicating, and rationalizing similar control objectives within the compliance library.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Use Recommendation of similar control objectives skill to generate suggestions, Now Assist for Privacy Management, Privacy Management, Governance, Risk, and Compliance]
---

# Act on the recommendations for similar control objectives

Act on the recommendations, like accept as duplicate, retain as primary, or dismiss, to enable your compliance managers and analysts to streamline their processes by identifying, deduplicating, and rationalizing similar control objectives within the compliance library.

## Before you begin

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=australia&pubname=australia-intelligent-experiences&ft:locale=en-US).

Role required: sn\_reco\_template.rationalization\_process\_writer and sn\_grc\_shared\_genai.compliance\_gen\_ai\_user

For more information on related roles, see [Roles installed with GRC: Policy and Compliance Management](../../grc-policy-and-compliance/reference/r_InstallWPolAndCompl.md#).

## About this task

Now Assist for Integrated Risk Management \(IRM\) introduces an AI-powered rationalization workflow that enables privacy managers and analysts to act on recommendations for similar control objectives. This process identifies duplicates, consolidates associations, and creates unified control objectives that are easier to support management and audit.

**Important:** Be sure to check AI-generated recommendations for accuracy.

## Procedure

1.  Navigate to **Workspaces** &gt; **Privacy Workspace**.

2.  Select the List icon.

3.  Navigate to **Library** &gt; **Control Objectives**.

4.  Select the control objective that you want to review recommendations for.

5.  In the control objective page, navigate to the **Rationalize** tab.

6.  Select the control objective recommendation card and review the following sections:

    |Field|Description|
    |-----|-----------|
    |Name|Name of the control objective.|
    |Source|The origin or reference from which a control objective is derived.|
    |Description|Description and summary of the control objective.|
    |Supplemental guidance|Additional guidance about the control objective.|
    |**Evaluate Affected Associations**|
    |Impacted items|Related lists that contain the items that are directly affected by the consolidation of the control objectives.|
    |Associated items|Related lists that contain all the associations from accepted control objectives in a consolidated view.|

7.  View the full record for a control objective by selecting the details icon \(\).

8.  For all recommendations, take one of the following actions on it:

    -   Select **Accept as duplicate** and then **Confirm** to accept a recommendation as a duplicate.
    -   Select **Dismiss** and then **Confirm** to avoid a recommendation from being shown again as it isn’t a duplicate.
    -   Select **Retain as primary** and then **Confirm** to mark the control objective as the primary, retaining it as the main objective.
    **Note:**

    -   Only one control objective can be retained as primary. The information from all duplicate control objectives is combined into the primary objective.
    -   At least one retained control objective must be active for the rationalization process to move to the next state.
    -   When the retained primary control objective is deleted, the rationalization process doesn’t transition to the next state.
    -   When a control objective is deleted, its associations remain visible but are removed after the user initiates a transition to the next state.
    -   Any recommendations that are linked to a deleted control objective are also deleted.
    -   When an accepted control objective is deactivated, all impacted items are automatically moved to inactive state.
9.  In the **Justification** field, provide a justification for the action taken on the recommendation.

10. After accepting the control objectives as duplicates, scroll to the bottom of the page, and select **Create** to use generative AI to create a common control objective.

    This AI-driven approach eliminates the need to manually retain a primary control objective.

    Generative AI automatically populates the name, description, and guidance fields and displays the consolidated objective on the form. It combines details from all the accepted control objectives into a single, new common control objective.

11. Regenerate the common control objective fields by selecting **Generate** on the form and then selecting **Update**.

12. Select **Request review**.

    -   After you act on all recommendations, the **Request review** button is enabled.
    -   The actions you take on the recommendations are sent for review to the configured reviewers. The reviewer can accept or reject your actions and provide their justifications.
13. Select **Summary**.

    Analyze the reviewer feedback and act on it as necessary.

14. After the **Analyze** state is approved, select **Consolidate**.

    This action consolidates the details of all the accepted control objectives into the primary control objective.

15. Review all the impacted items and associations and take one of the following actions on the associations:

    -   Accept the association by selecting **Accept** and then selecting **Confirm**.
    -   Remove an association by selecting **Dismiss** and then selecting **Confirm**.
    **Note:**

    -   By default, all associations are in the Accepted state. You can select an association and choose to dismiss or accept the association as is.
    -   The impacted items are items that are affected by consolidating the accepted control objectives into the primary control objective. These items are retired and can’t be associated. Select **Sync Impacted Items** to update the impacted items list across various states.
16. Initiate the review process by selecting **Request review**.

    The reviewer can review the action taken by you on all the impacted items and associations. The reviewer can accept or reject your actions and provide their justifications. They can also act on the associations that are captured in the summary.

17. Select the bulb icon on the right to access the **Reviewer Feedback** section.

    The Reviewer Feedback section provides a chronological overview of all user actions taken on the recommendations that provides a chronological overview of all user actions taken on the recommendations. The following details are captured for each action:

    -   **User Identity**: The user who performed the action
    -   **Action Type**: Whether the control objective was Accepted, Retained, or Dismissed
    -   **Justification**: The reason provided for the action taken
    -   **Control Objective**: The specific control objective associated with the action
    -   **Latest Update**: The most recent status or change related to the action
    This structured format allows for clear tracking and understanding of the actions taken by users.

18. Reset the rationalization process to the Analyze state by selecting **Restart Analyze**.

    The **Restart Analyze** option enables you to reevaluate the recommendations by accepting, dismissing, or retaining them.

19. After the **Consolidate** state is approved, select **Confirm** and then **Confirm** to complete the rationalization process.

    The Consolidated state page now displays the retained and accepted control objectives with their associated items. This change provides you with an improved context for the rationalization process.

    After the confirmation, the following changes happen:

    -   The state of the rationalization process is moved to closed.
    -   The accepted control objectives are retired and all their details and associations are merged into the retained control objective.
    -   The impacted items are retired.

