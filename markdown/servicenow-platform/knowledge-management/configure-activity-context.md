---
title: Configure activity contexts for Self-Service Analytics
description: Define the type of activities you want to collect as Self-Service Analytics data for a user entity such as consumers and customer contacts.
locale: en-US
release: xanadu
product: Knowledge Management
classification: knowledge-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configure Self-Service Analytics, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure activity contexts for Self-Service Analytics

Define the type of activities you want to collect as Self-Service Analytics data for a user entity such as consumers and customer contacts.

## Before you begin

Role required: sn\_ssa\_core.self\_service\_manager

## About this task

The activity types you add to an activity context are already predefined for use in applications that use the Subscriptions and Activity Feed Framework. This framework is available when you install the Subscriptions and Activity Feed Framework plugin \(com.snc.activity\_subscriptions\). The plugin is activated when you activate the Self-Service Analytics Core plugin \(com.snc.self\_service\_analytics\_core\).

## Procedure

1.  Navigate to **All** &gt; **Self-Service Analytics** &gt; **Configuration** &gt; **Activity Context**.

2.  In the Activity Contexts list, search for and select the activity context for your user entity.

    -   For consumers, select **Consumer**.
    -   For customer contacts, select **Contact**.
    -   For user entities other than consumers and customer contacts, click **New** to create another activity context.
    **Note:** To get the activity contexts Consumer and Contact by default, you must install Self-Service Analytics for Customer Service \(com.snc.pa.self\_service\_analytics\_csm\) plugin.

3.  On the Activity Context form, verify the default field values for consumers and customer contacts, or fill in the values for a custom configuration.

<table id="table_bxj_sbx_4jb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Unique name for your activity context.

</td></tr><tr><td>

Context Table

</td><td>

Table that includes the user entity whose actions need to be tracked and displayed on the Self-Service Analytics dashboard.For example, if you want to track all actions for a customer contact, select the Contact \[customer\_contact\] table. Similarly, if you want to track all actions for a consumer, select the Consumer \[csm\_consumer\] table.​

</td></tr><tr><td>

Module

</td><td>

Module associated with the application that stores the activities data.

</td></tr><tr><td>

Application

</td><td>

Scope of the application. This field is automatically set based on the application scope selected in the application picker.

</td></tr><tr><td>

Domain

</td><td>

Domain in which the activities records exist.

</td></tr></tbody>
</table>4.  If you are creating a new activity context, click **Submit** and then select the newly created activity context link from the Activity Contexts list.

5.  In the Activity Context Groups related list, map an activity context with activity groups.

    -   For consumers and customer contacts, verify the default field values for an existing configuration.
    -   For user entities other than consumers and customer contacts, click **New** to create another activity group or map with an existing activity group.
    For a new activity group mapping, on the Activity Group form, fill in the fields and click **Submit**. In the Activity Context Groups related list, you then have to select the newly created activity group and add available activity types to the activity group.

    |Field|Description|
    |-----|-----------|
    |Activity Context|Activity context associated with the activity group.|
    |Activity Group|Option to search for and select an activity group.|
    |Application|Defines the scope of the application. This field is automatically populated based on the application scope.|
    |Domain|Domain in which the activities records exist.|

6.  In the Activity Context Types related list, map an activity context with an activity type.

    -   For consumers and customer contacts, verify the default field values for an existing configuration.
    -   For user entities other than consumers and customer contacts, click **New** to create another mapping or use an existing configuration.
    For a new activity type mapping, on the Activity Source Context Mapping form, fill in the fields and click **Submit**.

<table id="table_cvd_kkb_nlb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Activity Context

</td><td>

Activity context associated with the activity source.

</td></tr><tr><td>

Context Table

</td><td>

Table that includes the user entity whose actions need to be tracked and displayed on the Self-Service Analytics dashboard.This field is auto-populated based on the selected activity context.

</td></tr><tr><td>

Activity Type

</td><td>

Activity type you want to associate with the activity context.

</td></tr><tr><td>

Source Table

</td><td>

Table from which the data for the activity context is populated.

</td></tr><tr><td>

Filter Criteria

</td><td>

Filter conditions applied on the source table.

</td></tr><tr><td>

Advanced Mapping

</td><td>

Option to enable advanced mapping of activity source and activity context. You enter a script in the **Advanced Mapping Script** field.

</td></tr><tr><td>

Advanced Mapping Script

</td><td>

Script to use if the source and context mapping is not sufficient. This field appears only when the **Advanced Mapping** option is selected.

</td></tr><tr><td>

Module

</td><td>

Module associated with the application that stores the activities data.

</td></tr><tr><td>

Application

</td><td>

Scope of the application that contains the user entity. This field is automatically set based on the application scope selected in the application picker.

</td></tr><tr><td>

Domain

</td><td>

Domain in which the activities records exist.

</td></tr><tr><td>

Fetch from Activities

</td><td>

Option to enable a business rule defined for an activity type.

</td></tr></tbody>
</table>7.  On the Activity Context form, click **Update**.


## What to do next

[Configure pattern elements for Self-Service Analytics](configure-pattern-element.md).

**Parent Topic:**[Configure Self-Service Analytics](config-ssa.md)

