---
title: Add questions from a question bank to a template
description: Add one or more published questions from a question bank to an assessment template instead of creating the same questions again.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-add-questions-from-question-bank.html
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 2
breadcrumb: [Question bank, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Add questions from a question bank to a template

Add one or more published questions from a question bank to an assessment template instead of creating the same questions again.

## Before you begin

Role required: sn\_smart\_asmt.template\_manager or sn\_smart\_asmt.assessment\_admin

To view and select questions from a question bank, you also need the sn\_smart\_asmt.question\_bank\_reader role together with one of the roles configured in the question bank's category. For more information, see [Roles in Smart Assessment Engine](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-roles-defined.md).

## About this task

Only published questions in question banks whose purposes match the template's purpose are available to add.

## Procedure

1.  Open an assessment template for updates.

    For more information, see [Add instructions and questions to an assessment template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-populate.md).

2.  Select a section, subsection, or question in the content tree and then select **Add question from question bank**.

    The system opens a full-screen window that lists the question banks that are applicable to the template. Use the keyword search field in this window to narrow the list of questions.

3.  Select the checkbox for each question that you want to add.

    You can select questions across multiple question banks. For each question, the window shows the question label, type, and type-specific configuration. For example, a choice-type question shows response options, and a number-type question shows the number range.

    A question that you already added elsewhere in the template shows an indicator so that you don't add a duplicate.

4.  Select **View selected questions** to review the selected questions, and then select or clear questions as needed.

5.  Select **Add question to template**.

    The questions that you add are inserted directly after the item that you selected, the same way as when you manually add a question. If you select a section or subsection instead of a question, the new questions are added at the end of that section or subsection.


## Result

The imported questions keep their question bank configuration, such as response options and justification settings.

**Related topics**  


[Publish questions in a question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-publish.md)

[Question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/question-bank.md)

