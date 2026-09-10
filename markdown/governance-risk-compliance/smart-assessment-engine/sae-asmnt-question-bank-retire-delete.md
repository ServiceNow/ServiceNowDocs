---
title: Retire or delete a question bank
description: Retire all the published questions in a question bank at once, or delete an entire question bank when it's no longer needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-retire-delete.html
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [Question bank, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Retire or delete a question bank

Retire all the published questions in a question bank at once, or delete an entire question bank when it's no longer needed.

## Before you begin

Role required: sn\_smart\_asmt.question\_bank\_manager or sn\_smart\_asmt.assessment\_admin

## About this task

Use these bulk options when an entire question bank, rather than individual questions, needs to be retired or removed. For example, a regulatory change might make every question in a question bank obsolete. A question bank might also have been created for a category that no longer needs one.

**Important:** Deleting a question bank permanently removes the question bank and all of its sections and questions. Assessment templates that already added questions from the question bank keep those questions; deleting or retiring the question bank doesn't affect them.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  Select \[Omitted image "question-bank.png"\] Alt text:.

    The question bank hub lists every question bank that you have access to.

3.  Open the question bank that you want to retire or delete.

4.  Select the **Other bulk options** menu.

5.  Choose one of the following options.

    |Option|Description|
    |------|-----------|
    |**__Retire all published questions__**|Moves every published question in the question bank to the **Retired** state in a single action. This option is available only when the question bank contains at least one published question.|
    |**__Delete question bank__**|Permanently deletes the question bank along with its sections and questions.|

6.  Confirm the action in the dialog that appears.


## Result

Retired questions are no longer available for template managers to add to new assessment templates, but assessment templates that already added them keep the questions unchanged. Deleting a question bank removes it from the question bank hub entirely.

**Related topics**  


[Question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/question-bank.md)

[Publish questions in a question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-publish.md)

