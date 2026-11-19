---
title: Publish questions in a question bank
description: Move a question through the draft, ready to publish, and published lifecycle stages so that it becomes available for template managers to add to assessment templates.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-question-bank-publish.html
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: task
last_updated: "2026-09-03"
reading_time_minutes: 1
breadcrumb: [Question bank, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Publish questions in a question bank

Move a question through the draft, ready to publish, and published lifecycle stages so that it becomes available for template managers to add to assessment templates.

## Before you begin

Role required: sn\_smart\_asmt.question\_bank\_manager or sn\_smart\_asmt.assessment\_admin

## About this task

A question bank question moves through four lifecycle stages: draft, ready to publish, published, and retired. Each question card includes a state menu that you use to change the question's state. A published question is set to read-only except for its state menu and **Delete** control.

You can select **Draft** from a published question's state menu to move it back to draft and edit it further. Moving a question back to draft doesn't affect assessment templates that already added it.

## Procedure

1.  Navigate to **Workspaces** &gt; **Assessment Workspace**.

2.  Select \[Omitted image "question-bank.png"\] Alt text:.

    The question bank hub lists every question bank that you have access to.

3.  Open the question bank that contains the questions that you want to publish.

4.  Select a question and change its state to **Ready to publish** from the state menu.

    Repeat this step for each question that you want to publish.

5.  Select **Publish questions** button to publish every ready-to-publish question in the question bank at the same time.

    The system marks the selected questions as published and refreshes the question labels in the content tree to show the updated state.

6.  To publish a single question instead, select **Publish** from that question's state menu.

7.  To remove a question from the question bank, select \[Omitted image "delete-question.png"\] Alt text:.

    Deleting a published question doesn't affect the assessment templates that already added it.


## Result

Published questions are available for template managers to add to assessment templates. See [Add questions from a question bank to a template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/smart-assessment-engine/sae-asmnt-template-add-questions-from-question-bank.md).

