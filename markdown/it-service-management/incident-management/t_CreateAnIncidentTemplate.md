---
title: Create incident template
description: Create an incident template to ensure consistency in the way information about the incident request is captured. A template also helps you to create incident easily and accurately.
locale: en-US
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Incident templates and record producers, Configuring Incident Management, Incident Management, IT Service Management]
---

# Create incident template

Create an incident template to ensure consistency in the way information about the incident request is captured. A template also helps you to create incident easily and accurately.

## Before you begin

Role required: admin

## About this task

Let us consider an example where you want to create a template to log an incident when you are denied access to the Bond Trading application.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Templates**.

    You can also [Create a template from the incident form](create-template-inci-form.md).

2.  Complete the steps in [Create a template using the Template form](https://www.servicenow.com/docs/access?context=t_CreateATemplateUsingTheTmplForm&version=australia&pubname=australia-platform-administration&ft:locale=en-US) using the following information:

    -   **Name**: `Bond Trading Access Denied`
    -   **Table**: Incident \[incident\]
    -   **Global**: Select the check box. The **Global** option allows any user to use the template, not just the template creator.
    -   **Short Description**: `Bond Trading Access Denied`
    -   **Template**: Add the following values to define the fields that are filled in when the template is used:
        -   **\[Category\]: \[Inquiry / Help\]**
        -   **\[Configuration Item\]: \[Bond Trading\]**
        -   **\[Description\]: \[The user was denied access to the Bond Trading application\]**
        -   **\[Impact\]: \[2 - Medium\]**
        -   **\[Urgency\]: \[3 - Low\]**
    ![Incident template to log incident when access is denied to the Bond Trading application](../image/incident-template.png)

3.  Select **Submit**.


**Parent Topic:**[Incident templates and record producers](../concept/incident-templates-record-producers.md)

**Related topics**  


[Create a module that uses incident template](t_UseATemplateFromAModule.md)

[Create a record producer to log incidents](t_CreateARecordProducer.md)

[Create a record producer using a template](t_CreateRecProducWithTempl.md)

