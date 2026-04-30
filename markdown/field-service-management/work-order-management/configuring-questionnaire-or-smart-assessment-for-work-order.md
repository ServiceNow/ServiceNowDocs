---
title: Configuring work order questionnaires
description: As part of completing some work orders and tasks, Field Service agents fill out questionnaires or complete check lists.
locale: en-US
release: yokohama
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring work order tasks, Setting up work orders and tasks, Configuring Field Service Management, Field Service Management]
---

# Configuring work order questionnaires

As part of completing some work orders and tasks, Field Service agents fill out questionnaires or complete check lists.

Questionnaires gathers different types of information from Field Service agents, such as verifying their compliance with the generic Field Service process while working on the task.

Administrators can create questionnaire records and associate those records with work orders or work order tasks. For example, an agent might need to complete a safety check list before starting work on a task or fill out an inspection questionnaire before completing a work order. The administrator can also make filling out the questionnaire mandatory before an agent closes a task.

Questionnaire records include some configuration information, such as the condition or event that triggers the questionnaire, as well as the list of questions included in the questionnaire.

**Note:** Configuring questionnaires is optional.

Questionnaire for a work order or work order task can be either a survey-based questionnaire or a smart assessment.

## Survey-based questionnaire

A survey-based questionnaire uses the **Survey Designer** tool to create a questionnaire with a list of questions.

For more information, see [Configuring survey-based work order questionnaires](work-order-questionnaire.md).

## Smart Assessment questionnaire

A Smart Assessment questionnaire for Now Mobile uses **Template designer** in the Smart Assessment Engine application.

For more information, see [Configuring Smart Assessment questionnaires for Now Mobile Agent](configuring-smart-assessment-questionnaire.md).

**Note:**

-   Smart Assessment allows migration of survey-based questionnaires to Smart Assessment questionnaires.

-   Usage of Smart Assessment questionnaire can't be disabled once enabled.


