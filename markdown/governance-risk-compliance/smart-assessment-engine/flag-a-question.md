---
title: Flag or resolve a question
description: Flag a question on an assessment to indicate that it needs attention. After the response is updated, mark the question as resolved or remove the flag.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/flag-a-question.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 2
breadcrumb: [Respond to assessments, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Flag or resolve a question

Flag a question on an assessment to indicate that it needs attention. After the response is updated, mark the question as resolved or remove the flag.

## Before you begin

Flagging is enabled for all roles by default. If the assessment administrator has configured the **Question flag roles** field on the template category, your user account must have one of the configured roles to change a question's flag state. For more information, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

Role required: none.

## About this task

A question's flag has one of three states:

-   **Unflagged**

    No flag is set on the question. This is the default state for every question.

-   **Flagged**

    The question is marked as needing attention. The flag icon on the question card is highlighted.

-   **Resolved**

    The question was previously flagged and has been addressed. The flag icon shows the resolved state.


For more information, see [Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md).

## Procedure

1.  Navigate to your workspace and then to your list of assessments.

    Here’s an example of how to navigate to this list in the Compliance Workspace.

    1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.
    2.  Select the tasks icon \[Omitted image "list-icon.png"\] Alt text:.
    3.  Select the **Control attestations** &gt; **Smart Assessments** on the left panel.
    4.  The smart assessments list is displayed.
2.  Select the assessment in which you want to flag or resolve a question.

3.  Open the question that you want to flag, resolve, or unflag.

4.  Select the flag icon at the bottom of the question card.

    The flag icon cycles the question through three states each time you select it: **Unflagged**, **Flagged**, and **Resolved**. The icon and tooltip update to reflect the current state.

    -   From **Unflagged**, the icon appears as an outline flag \[Omitted image "question-flag.png"\] Alt text:. Selecting it sets the question to **Flagged**.
    -   From **Flagged**, the icon appears as a filled flag \[Omitted image "question-flagged.png"\] Alt text:. Selecting it sets the question to **Resolved**.
    -   From **Resolved**, the icon appears as a check mark \[Omitted image "question-flag-resolved.png"\] Alt text:. Selecting it returns the question to **Unflagged**.

## What to do next

To focus your review on flagged questions, use the **Flagged** filter from the filter list. You can combine this filter with other filters, such as **Unanswered** or **With comments**, to narrow your view further. For details on the available filters and how to combine them, see [Filtering questions in an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/filtering-questions-in-an-assessment.md).

**Related topics**  


[Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md)

[Add a comment or work note to a question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/add-comment-to-question.md)

[Filtering questions in an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/filtering-questions-in-an-assessment.md)

