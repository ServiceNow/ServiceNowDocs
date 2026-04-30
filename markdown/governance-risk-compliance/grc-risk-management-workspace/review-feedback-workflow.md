---
title: Parallel Review and Feedback workflow
description: The Parallel Review and Feedback workflow outlines the systematic process by which the solution facilitates the submission of feedback on a record or specific fields within a record. Feedback could be related to any improvement or recommendation at a record level, such as data integrity, compliance, and operational procedures.
locale: en-US
release: yokohama
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Parallel Review and Feedback in Advanced Risk, Use Risk Workspace, Risk Management, Governance, Risk, and Compliance]
---

# Parallel Review and Feedback workflow

The Parallel Review and Feedback workflow outlines the systematic process by which the solution facilitates the submission of feedback on a record or specific fields within a record. Feedback could be related to any improvement or recommendation at a record level, such as data integrity, compliance, and operational procedures.

## Exploring the user journey for Parallel Review and Feedback

The following diagram shows the workflow of Review and Feedback.

![Parallel Review and Feedback workflow.](../image/review-feedback-workflow.jpg "Parallel Review and Feedback workflow")

The steps for how each user uses the Review and Feedback application according to their organization's requirements are explained as follows.

-   **Configure a feedback integration**

    Configure a feedback integration setup in the Advanced Risk application to define the table on which you want to use Parallel Review and Feedback. This setup enables you to define the workspace, reviewer, and respondent for creating feedback on the table records. A user with the sn\_rvw\_feedback.admin role can configure a feedback integration. For more details, see [Configure a feedback integration](../task/configure-feedback-integration.md).

-   **Create the feedback**

    A user with the sn\_rvw\_feedback.reviewer role can create feedback on a record they're reviewing, suggesting overall improvements, or changes to specific fields in the record. You can create feedback on both ServiceNow® and external records. For more information, see [Create feedback in the Risk Workspace](../task/create-feedback.md) and [Create Feedback from the record side panel](../task/create-feedback-from-record-side-panel.md).

-   **Respond to the feedback**

    A user with the sn\_rvw\_feedback.respondent role can take necessary actions and provide comments or explanations regarding the submitted feedback. The respondent can either remediate or reject the feedback, provided that there’s proper justification. After closing all the open items, the respondent can send the feedback to the reviewer. For more information, see [Respond to the feedback](../task/respond-to-feedback.md).

-   **Collaborate through sidebar chat feature**

    The Sidebar chat feature enabling the first and second line risk users to discuss feedback in real-time. The chat feature enables better collaboration among different stakeholders to brainstorm solutions, clarify details, or coordinate actions regarding the feedback received. For more information, see [Initiate a chat from Sidebar in Parallel Review and Feedback](../task/initiate-chat-sidebar-review-and-feedback.md).

-   **Review and close the feedback**

    When the reviewer is content with the respondent's comments, they have a couple of options. They can choose to close the feedback either with or without an action. If an action is selected, they can take further actions based on the feedback received. It involves initiating new actions or tasks, such as creating an issue or linking it to an existing record, to facilitate follow-up and resolution. For example, an organization conducted an RCSA \(Risk and control self-assessment\) concerning fraud-related risks and suggested they have 3 controls in place. Subsequently, the second line of defense reviewed the assessment and raised a feedback, recommending the addition of a new control as it aligns with global best practices to mitigate that risk. Implementing this new control requires budget allocation and an estimated timeline of 1-2 years. The organization may decide to close the feedback by creating an issue to track and manage the progress.

    When the reviewer isn’t satisfied with the respondent comments, the reviewer can move the feedback to the Draft state and reinitiate the workflow. For more information, see [Review and close the feedback](../task/review-and-close-feedback.md).


**Parent Topic:**[Parallel Review and Feedback in Advanced Risk](integrate-advanced-risk-with-parallel-review-feedback.md)

