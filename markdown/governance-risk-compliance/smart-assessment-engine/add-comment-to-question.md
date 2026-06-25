---
title: Add a comment or work note to a question
description: Post a comment or a private work note on a specific question in an assessment so that reviewers and contributors can discuss the question.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/smart-assessment-engine/add-comment-to-question.html
release: australia
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-06-01"
reading_time_minutes: 3
breadcrumb: [Respond to assessments, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Add a comment or work note to a question

Post a comment or a private work note on a specific question in an assessment so that reviewers and contributors can discuss the question.

## Before you begin

Role required:

-   For comments: sn\_smart\_asmt.actor, sn\_smart\_asmt.assessment\_admin, or sn\_smart\_asmt.assessment\_reader.
-   For worknote: sn\_smart\_asmt.assessment\_admin or role configured in the **Worknote roles** field on the template category

**Note:** To post a work note, your user account must have one of the roles configured in the **Worknotes roles** field on the template category. Work notes are inactive by default; if no roles are configured, the Work notes tab is hidden for all users except the assessment administrator. For more information, see [Create an assessment template category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-category-create.md).

## About this task

Use question-level comments to discuss a specific question with other collaborators. Use work notes for internal conversations that should not be visible to all participants, for more details on question-level communication, see [Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md).

## Procedure

1.  Navigate to your workspace and then to your list of assessments.

    Here’s an example of how to navigate to this list in the Compliance Workspace.

    1.  Navigate to **All** &gt; **Policy and Compliance** &gt; **Compliance Workspace**.
    2.  Select the tasks icon \[Omitted image "list-icon.png"\] Alt text:.
    3.  Select the **Control attestations** &gt; **Smart Assessments** on the left panel.
    4.  The smart assessments list is displayed.
2.  Select the assessment in which you want to comment the questions.

3.  Open the question that you want to comment on.

4.  Select the comment \[Omitted image "question-comment.png"\] Alt text: icon at the bottom of the question card.

    The comment icon is visible when the question already has one or more comments. If the question has no comments, the icon appears when the question card is focused.

5.  If you want to post a work note instead of a comment, select the **Work notes** tab in the dynamic panel.

    If the **Work notes** tab is not visible, your user account does not have one of the roles configured in the **Worknotes roles** field on the template category.

6.  Enter your comment in the input field.

7.  Select post comment \[Omitted image "post-comments.png"\] Alt text: icon for a comment, or post work notes \[Omitted image "post-comments.png"\] Alt text: icon for a work note.

    The entry appears in the thread for that question, and the comment count on the question card updates to reflect the total number of comments and work notes on the question.


## What to do next

To find all questions on the assessment that have comments, use the **With comments** filter from the filter list. For details on the available filters and how to combine them, see [Filtering questions in an assessment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/filtering-questions-in-an-assessment.md).

**Related topics**  


[Collaboration in assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/collaboration-in-assessments.md)

[Flag or resolve a question](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/flag-a-question.md)

[Adding comments to assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/smart-assessment-engine/adding-comments-to-assessments.md)

