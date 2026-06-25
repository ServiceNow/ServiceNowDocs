---
title: Create incident template
description: Create an incident template to confirm consistency in the way information about the incident request is captured. A template also helps you to create incident easily and accurately.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/incident-management/t\_CreateAnIncidentTemplate.html
release: australia
product: Incident Management
classification: incident-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Incident templates and record producers, Configuring Incident Management, Incident Management, IT Service Management]
---

# Create incident template

Create an incident template to confirm consistency in the way information about the incident request is captured. A template also helps you to create incident easily and accurately.

## Before you begin

Role required: admin

## About this task

Let us consider an example where you want to create a template to log an incident when you are denied access to the Bond Trading application.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Templates**.

    You can also [Create a template from the incident form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/create-template-inci-form.md).

2.  Complete the steps in [Create a template using the Template form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_CreateATemplateUsingTheTmplForm.md) using the following information:

    -   **Name**: `Bond Trading Access Denied`
    -   **Table**: Incident \[incident\]
    -   **Global**: Select the check box. The **Global** option allows any user to use the template, not just the template creator.
        -   **User:** The user who can configure and apply this template. If specified, only that user can see the templates unless **Global** is also selected.
        -   **Group:** The group whose members can use this template. If specified, only members of that group can see the template unless **Global** is also selected.

            **Note:** If you leave **User** and **Group** empty and clear the **Global** check box, only you can see the template. To share the template with a team or user, specify a **Group** or **User**, or select the **Global** check box.

    -   **Short Description**: `Bond Trading Access Denied`
    -   **Template**: Add the following values to define the fields that are filled in when the template is used:
        -   **\[Category\]: \[Inquiry / Help\]**
        -   **\[Configuration Item\]: \[Bond Trading\]**
        -   **\[Description\]: \[The user was denied access to the Bond Trading application\]**
        -   **\[Impact\]: \[2 - Medium\]**
        -   **\[Urgency\]: \[3 - Low\]**
    \[Omitted image "incident-template.png"\] Alt text: Incident template to log incident when access is denied to the Bond Trading application

    **Note:** Template fields only support static values. For dynamic references to other field values, you can use a client script or UI action. For example, a resolution can't automatically include the caller's name.

3.  Select **Submit**.


**Parent Topic:**[Incident templates and record producers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/incident-management/incident-templates-record-producers.md)

**Related topics**  


[Create a module that uses incident template]()

[Create a record producer to log incidents]()

[Create a record producer using a template]()

