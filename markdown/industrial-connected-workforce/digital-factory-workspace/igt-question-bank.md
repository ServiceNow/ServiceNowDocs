---
title: Question bank in Industrial Guided Tasks
description: Use the question bank to store assessment questions once and reuse them across multiple Industrial Guided Task standards, so that you maintain consistency across standards without recreating questions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/igt-question-bank.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [question bank, reuse questions, Industrial Guided Task Manager, IGT standard]
breadcrumb: [Industrial Guided Tasks, Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Question bank in Industrial Guided Tasks

Use the question bank to store assessment questions once and reuse them across multiple Industrial Guided Task standards, so that you maintain consistency across standards without recreating questions.

## Question bank overview

Industrial Guided Tasks uses the question bank capability of the Smart Assessment Engine. A question bank is a shared repository of assessment questions. Instead of creating the same question in each standard, you create and publish it in a question bank. Standard authors add it to any IGT standard that requires it.

When you add a question from a question bank to an IGT standard, the system adds an independent copy of the question to the standard. The copy keeps its question bank configuration, such as response options. Later changes to the question in the question bank don't affect standards that already use it. Also, changes to the copy in a standard don't affect the question bank.

For more information about question banks, see [Question bank](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/question-bank.md).

## Roles

Access to the question bank is controlled by role. The following roles are relevant:

-   **Industrial Guided Task Manager \[sn\_icw\_igt.manager\]**

    Can create question banks and create and publish questions in them from the question bank hub in the Assessment Workspace. This role contains the sn\_icw\_igt.standard\_author and sn\_smart\_asmt.question\_bank\_manager roles, so an Industrial Guided Task Manager can also do everything that a standard author can do.

-   **Standard author \[sn\_icw\_igt.standard\_author\]**

    Can search for published questions in the question bank and add them to sections in an IGT standard during task authoring. Can't create question banks or add, modify, or delete questions in a question bank.


## Question bank purposes

Each question bank has one or more purposes. Only published questions in question banks with the Industrial Guided Task purpose are available to add to IGT standards.

## Question states

A question in a question bank moves from Draft to Published when an Industrial Guided Task Manager publishes it. Only published questions are available to add to an IGT standard. A retired question is no longer available to add, but continues to work in the standards that already use it.

## Adding questions during task authoring

Standard authors add questions from the question bank on the **Task authoring** tab of an IGT standard. For more information, see [Add a question bank question to an IGT standard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/add-question-bank-question-to-igt-standard.md).

**Note:**

After questions from the question bank are added, a message asks you to refresh the page. The questions appear in the standard after you refresh the page.

**Parent Topic:**[Exploring Industrial Guided Tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/exploring-industrial-guided-tasks.md)

