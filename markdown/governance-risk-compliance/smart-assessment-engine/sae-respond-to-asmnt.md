---
title: Responding to assessments
description: Use the Smart Assessment Engine application to help assessors complete survey requests. Track your progress and let the system automatically save your information. Administrators and template managers manage the assessment process.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/smart-assessment-engine/sae-respond-to-asmnt.html
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Responding to assessments

Use the Smart Assessment Engine application to help assessors complete survey requests. Track your progress and let the system automatically save your information. Administrators and template managers manage the assessment process.

If you have the Assessment actor \[sn\_smart\_asmt.actor\] role, you can submit responses to an assigned assessment. Here are some more key functionalities:

-   A progress indicator displays how much of the assessment you have completed.
-   Questions are paginated, making it easier to navigate through the assessment.
-   Your work is automatically saved, eliminating the risk of potential data loss.
-   An assessment administrator \[sn\_smart\_asmt.assessment\_admin\] can cancel assessments that are no longer needed.

If you have the assessment reassign \[sn\_smart\_asmt.reassign\] role, you can reassign in-progress assessments to another user. If your template manager or administrator has added reference information, such as scope-related information, you can view it in the Details section of your assessment. If relevant to the state of the assessment, the scope, requester, assignee, the requested and due dates are listed in the Details section by default.

The following example shows how your progress, save status, assessment status, reference information, actions, and more are indicated in the assessment view.

\[Omitted image "sae-asmnt-respond.png"\] Alt text: In-progress assessment that shows the previously described features and their indicators.

## Assessment response features

-   **Navigating assessments**

    Assessment actors can navigate through an assessment by selecting the section of questions they’re ready to answer.

-   **Saving assessments**

    Your assessment progress is automatically saved and your save status is indicated by the saved badge \[Omitted image "save-indicator.png"\] Alt text: Saved badge..

-   **Progress tracking in assessments**

    The progress bar indicates how many questions remain in the assessment including required and optional questions.

-   **Default focus when opening or reopening an assessment**

    When you open or reopen an assessment, the view defaults to the assessment instructions if configured. Otherwise, the view defaults to the first question of the first section or subsection. This default focus applies even if you or a contributor already answered later questions, or a response was set by response automation.

    **Note:** This feature is available starting with Zurich Patch 10.

-   **Searching reference-type question responses**

    For single-select and multi-select reference-type questions, if the specified table returns more than 10 records, you see only the first 10 by default. Select the search icon to open a list of all matching records and choose from the full set.

    **Note:** This feature is available starting with Zurich Patch 10.

-   **Question-level change history**

    Review a log of every response, justification, and flag-state change made to a question, including who made the change and when. For details, see [Question change history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-question-change-history.md).


