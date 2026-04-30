---
title: Propose a standard change template
description: Propose a new standard change template when you identify a need while creating a change request.
locale: en-US
release: xanadu
product: Change Management
classification: change-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Create a standard change task template, Standard change catalog, Configure, Change Management, IT Service Management]
---

# Propose a standard change template

Propose a new standard change template when you identify a need while creating a change request.

## Before you begin

Role required: itil, admin

## About this task

As an IT technician, you can propose a new change template for a change request that you frequently create. This new template is later sent for approval to the change management team, which reviews the request and approves the template as part of the approval process.

## Procedure

1.  You can propose a standard change template by navigating to **Change** &gt; **Standard Change** &gt; **Standard Change Catalog** &gt; **Template Management** &gt; **Propose a new Standard Change Template** and filling in the fields on the form.

    |Field|Description|
    |-----|-----------|
    |Short description|Short description of the standard change proposal template.|
    |Category|Category under which the template is published. For example, Server Standard Changes.|
    |Sample Change Requests|Change requests that are available as samples for the change that you propose. The Change Management team reviews the requests as a part of the approval process.|
    |Change Request values|Text which appears as default text in the standard change proposal template.|

2.  Click **Save**.

    The proposal is created with the status **New**.

3.  Click **Request Approval**.

    The proposal is created with the status **In Progress**.

4.  Create a standard change template from a change that exists by completing the following steps.

    1.  Navigate to **Change** &gt; **Open** and click the change whose information you want to use in the standard change template.

    2.  Open the form context menu and click **Propose a Standard Change Template**.

    **Note:**

    -   Any change tasks that are included with the change also get copied to the new standard change proposal. The fields copied from both the change and change tasks are defined in the [Standard Change Properties](t_ConfigureTheStandardChangeCatalog.md).
    -   By default, approval records are created for members of the Change Management group.
    Alternatively, as a change manager, create and submit a standard change proposal that can be utilized as a template to draft a standard change request that occurs frequently and is of low risk. By default, the basic standard change proposal workflow sends approval records to members of the change management group where the members verify and modify the records, as appropriate. Navigate to **Change** &gt; **Standard Change** &gt; **My Proposals**. Click **New**, fill the form, and then click **Submit**.


## Result

A new template record is created for use.

**Parent Topic:**[Create a standard change task template](create-a-standard-change-task-template.md)

