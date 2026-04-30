---
title: Configure an activity configuration for a lifecycle event
description: Create or modify an activity configuration to define the fulfillment process and conditions for closure for a lifecycle event activity.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure the supporting components for a lifecycle event, Building a lifecycle event, Use, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Configure an activity configuration for a lifecycle event

Create or modify an activity configuration to define the fulfillment process and conditions for closure for a lifecycle event activity.

## Before you begin

Role required: sn\_hr\_le.admin or sn\_hr\_le.activity\_set\_manager

A key benefit of the Enterprise Onboarding and Transitions application is that you can leverage existing fulfillment processes from different departments to fulfill lifecycle event activities that are assigned to them. For example, you can use a fulfillment process set up by the IT department to fulfill lifecycle event activities assigned to IT. Preconfigured activity types are available to use. You can also configure your own custom activity types.

## Procedure

1.  Navigate to **All** &gt; **Lifecycle Events** &gt; **Administration** &gt; **Manage Activity Configuration**.

2.  Click **New** or open a record.

3.  Fill in the fields on the form.

<table id="table_wr5_stm_tgb"><thead><tr><th>

Field

</th><th colspan="2">

Description

</th></tr></thead><tbody><tr><td>

Fulfiller activity

</td><td colspan="2">

Name of the fulfiller activity type.

</td></tr><tr><td rowspan="9">

Configuration type

</td><td colspan="2">

Configuration type. Select one of the following:

</td></tr><tr><td>

Catalog item

</td><td>

Creates a task, request, or case based on an existing catalog item. In the **Catalog** field, select a catalog.

</td></tr><tr><td>

Content

</td><td>

 

</td></tr><tr><td>

Flow

</td><td>

Creates a flow on the parent lifecycle event case.**Note:** A flow automates a process with a sequence of reusable actions. See [Flow designer](https://www.servicenow.com/docs/access?context=flow-designer&version=zurich&pubname=zurich-application-development&ft:locale=en-US) for more information.

</td></tr><tr><td>

HR service

</td><td>

Creates a case based on an HR service.

</td></tr><tr><td>

HR task template

</td><td>

Creates a task based on an HR task template.

</td></tr><tr><td>

Order guide

</td><td>

Creates an IT request based on an order guide. In the **Catalog** field, select a catalog.

</td></tr><tr><td>

Template

</td><td>

Creates a record on a task table that supports templates.

</td></tr><tr><td>

Workflow

</td><td>

Creates a workflow on the parent lifecycle event case. In the following fields, provide the following:-   **Workflow**: A workflow that runs on the parent lifecycle event case.
-   **Workflow required fields**: Fields on the activity form that are required to be populated for the workflow.
-   **Workflow optional fields**: Fields on the activity form that are optional and populated for the workflow.


</td></tr><tr><td>

Activity closure

</td><td colspan="2">

Conditions that must be met for the fulfiller activity to close and for the State value to change to Completed.**Note:** Once all of the activities in an activity set are completed, then the State value of the activity set will change to Finished.

</td></tr><tr><td>

Active

</td><td colspan="2">

Option to activate the fulfiller activity type for use.

</td></tr><tr><td>

Task table

</td><td colspan="2">

Table that the fulfiller activity type is associated with. Depending on the **Configuration type** selected, you can select a table or the field is automatically set to a table.

</td></tr><tr><td>

Badge

</td><td colspan="2">

Badge that the fulfiller activity type is associated with.**Note:** Badges display on the portal to indicate to the employee which department is fulfilling that activity. See [Configure an HR badge](CreateModHRBadges.md) for more information.

</td></tr></tbody>
</table>4.  Click **Save**.

5.  In the **Fulfiller Activity Configuration Mappings** section, map one or more fields from the parent lifecycle event case to the child activity.

    1.  Click **New** or open a record.

    2.  Fill in the fields on the form.

<table id="table_ejy_qzt_tgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity type configuration

</td><td>

This field is automatically set to the name of the fulfiller activity type.

</td></tr><tr><td>

Map from table

</td><td>

HR case table that the parent HR service is associated with.**Note:** Make sure that this table matches that of the HR case table associated with the parent HR service.

</td></tr><tr><td>

Map from field

</td><td>

Field that is being mapped from.**Note:** Make sure that the data type matches that of the target field.

</td></tr><tr><td>

Map to table

</td><td>

This field is automatically set to the table that the fulfiller activity type is associated with.

</td></tr><tr><td>

Map to field

</td><td>

Field that is being mapped to.**Note:** Make sure that the data type matches that of the source field.

</td></tr></tbody>
</table>        For example, the preconfigured fulfiller activity type for catalog items maps the subject\_person field from the HR Lifecycle Events Case \[sn\_hr\_le\_case\] table to the requested\_for field on the Request \[sc\_request\] table so that the activity form is automatically populated with the name of the user that the catalog item is being requested for.

    3.  Click **Submit** or **Update**.

    4.  Repeat the process as needed.

6.  Click **Update**.


**Parent Topic:**[Configure the supporting components for a lifecycle event](../concept/configure-supporting-components-for-lifecycle-event.md)

