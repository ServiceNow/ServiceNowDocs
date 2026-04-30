---
title: Update an automation attribute
description: Update an automation attribute to include the automation source and time savings information. This information is available in the Automation Center Value dashboard for analysis.
locale: en-US
release: zurich
product: Automation Center
classification: automation-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Working with automations, Use, Automation Center, Workflow Data Fabric]
---

# Update an automation attribute

Update an automation attribute to include the automation source and time savings information. This information is available in the Automation Center Value dashboard for analysis.

## Before you begin

Role required: sn\_ac.automation\_business\_user, sn\_ac.automation\_technical\_user, or sn\_ac.automation\_admin.

## About this task

When you create an automation request from Automation Center, you already provide the cost-saved and time-saved values. That information is displayed in the Automation Center Value dashboard. If required, you can update the values.

When data is sent from ServiceNow RPA and flows or any third-party vendor, the cost-saved and time-saved fields must be updated manually.

## Procedure

1.  Navigate to **All** &gt; **Automation Center** &gt; **Automation Center Home**.

2.  Select the list icon \(![List icon.](../images/autocenter-list-icon.png)\).

3.  On the **Lists** tab, under **Administration**, select **Automation Attributes**.

4.  Select an automation attribute that you want to update, and then select **Edit**.

5.  On the form, fill in the fields.

    **Note:** Only **Cost saved per run** and **Time saved per run** fields can be updated. The other fields are auto-generated.

<table id="id_jw3_jvk_4tb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Automation

</td><td>

Associated automation.

</td></tr><tr><td>

Cost saved per run

</td><td>

Cost saved after each run of the automation.

</td></tr><tr><td>

Published Date

</td><td>

Published date of the associated automation.You can edit this auto-generated field.

</td></tr><tr><td>

Source

</td><td>

Associated automation source.

</td></tr><tr><td>

Time saved per run

</td><td>

Time saved after each run of the automation.

</td></tr></tbody>
</table>6.  Select **Update**.


**Parent Topic:**[Working with automations](../concept/automations.md)

