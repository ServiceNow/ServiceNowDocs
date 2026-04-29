---
title: Configure the HR case creation form for an HR service
description: Configure the fields that appear on the HR case creation form for an HR service.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure an HR service, HR service configuration, HR services, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Configure the HR case creation form for an HR service

Configure the fields that appear on the HR case creation form for an HR service.

## Before you begin

Role required: sn\_hr\_core.admin

## About this task

This is the form that displays when an HR agent selects an HR service from the **Create New Case** module. You can include additional fields on the HR case creation form so that HR agents are able to collect relevant information before beginning work on the case. The case creation configuration records can be applied to one or more HR services.

## Procedure

1.  Navigate to **All** &gt; **HR Administration** &gt; **HR Services** &gt; **HR Service Configuration**.

2.  Open the HR service.

3.  In the **Case creation service config** field, open the case creation configuration record.

    **Note:** To create a new case creation configuration record for the HR service, click the **Lookup** icon, and then click **New**.

4.  Fill in the fields on the form.

<table id="table_j3f_1gj_lfb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the case creation service configuration record.

</td></tr><tr><td>

Task create table

</td><td>

Name of the HR case table that the record is associated with.

</td></tr><tr><td>

Left task fields

</td><td>

Fields to add on the left side of the form.**Note:** Only fields added to the Left task fields appear on the User segment groups form. Fields added to the Right task fields do not appear o the User segment groups form. For more information, see [Create a user segment group](bulk-case-segment.md).

</td></tr><tr><td>

Right task fields

</td><td>

Fields to add on the right side of the form.

</td></tr><tr><td>

Bottom task fields

</td><td>

Fields to add on the bottom of the form.

</td></tr></tbody>
</table>    **Note:** When adding the Description\(rich\_description\) field, the TinyMCE HTML editor does not appear until after the case is created and viewable. Any HTML formatted edits can be added after the case is created.

5.  Click **Submit** or **Update** on the case creation service configuration record.

6.  Click **Update** on the HR service form.


## Additional fields for tuition reimbursement HR case creation forms

You are part of an enterprise HR organization using the HR Service Delivery application. You have several HR services related to tuition reimbursement, and you know this case type requires the HR agent to collect information such as the school name, course title, and course justification before case work can begin. If that information is collected prior to case creation, you can save your organization time by avoiding the back-and-forth the HR agent and employee must engage in to capture the relevant information.

To do this, you need to configure the HR case creation form for tuition reimbursement HR services to include additional fields that ask for the school or program name, course title, course justification, course start date, and course end date. So you create a case creation service configuration record and associate it with the HR Total Rewards Case \[sn\_hr\_core\_case\_total\_rewards\] table. For the left, right, and bottom task fields, you add the additional fields you want to appear on the form.

![Fill in the relevant fields on the HR case creation configuration form.](../image/hr-case-creation-configuration-record.png)

Once the configuration is complete, HR agents that select the tuition reimbursement request service from the **Create New Case** module will see the additional fields that you added. This enables the HR agent to collect the relevant information before beginning work on the case.

![And this is how the configured fields appear on the HR creation form.](../image/hr-case-creation-config-example.png)

**Parent Topic:**[Configure an HR service](configure-hr-service.md)

