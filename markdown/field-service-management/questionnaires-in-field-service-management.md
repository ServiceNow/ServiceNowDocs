---
title: Questionnaires in Field Service Management
description: Field Service Management supports questionnaires as a structured mechanism for collecting information from field service agents during the execution of work orders and work order tasks. Questionnaires can be used at any stage of a task—before work begins, while work is in progress, or as a condition for closing a task—and can be made mandatory to enforce compliance and completeness.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/questionnaires-in-field-service-management.html
release: australia
topic_type: concept
last_updated: "2026-06-04"
reading_time_minutes: 2
breadcrumb: [Explore, Field Service Management]
---

# Questionnaires in Field Service Management

Field Service Management supports questionnaires as a structured mechanism for collecting information from field service agents during the execution of work orders and work order tasks. Questionnaires can be used at any stage of a task—before work begins, while work is in progress, or as a condition for closing a task—and can be made mandatory to enforce compliance and completeness.

Questionnaires serve several operational purposes across the field service lifecycle.

-   Agents can be required to complete a compliance checklist or safety check before starting work on a task, ensuring they have taken proper precautions and met regulatory requirements.
-   Inspection questionnaires can be triggered before a work order is completed, allowing reviewers and agents to verify that all required steps have been executed to the expected standard.
-   Checklist-style questionnaires confirm that all necessary actions have been performed before a task is closed.
-   Structured questions capture task-specific information—such as equipment condition, compliance confirmations, or part usage details—directly in the field, reducing manual follow-up and data entry errors.

Structured questions capture task-specific information—such as equipment condition, compliance confirmations, or part usage details—directly in the field, reducing manual follow-up and data entry errors.

## Questionnaire types

Field Service Management supports the following two types of questionnaires.

|Type|Description|Authoring tool|
|----|-----------|--------------|
|Survey-based questionnaire|Uses the Survey Designer to create a list of questions associated with a work order or task.|Survey Designer|
|Smart Assessment questionnaire|Uses the Smart Assessment Engine template designer, with support for conditional questions, offline execution, and enhanced mobile integration via Now Mobile Agent.|Smart Assessment Engine \(Template Designer\)|

Both types are triggered from the same work order and work order task forms. Smart Assessment allows migration from existing survey-based questionnaires, and once Smart Assessment is enabled, it cannot be disabled.

## Where questionnaires are used

Questionnaires are available across both the web interface and the ServiceNow Agent mobile application. On mobile, agents can view, answer, and submit questionnaires while offline; responses are stored in the device's local cache and synchronized when connectivity is restored. Agents cannot view each other's completed questionnaire responses.

**Related topics**  


[Survey-based questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/survey-based-questionnaires.md)

[Smart Assessment Questionnaires](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/field-service-management/smart-assessment-questionnaire.md)

