---
title: Add a price adjustment definition to a decision table​ in License and Permit Playbook
description: As an admin, you can use a price adjustment definition in the License and Permit Playbook to add adjustments to field prices based on the conditions of fields that are not price fields​, such as the residency status of the constituent for the location they are requesting the permit or license in.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create a pricing configuration decision table, Configure decision tables, License and Permit Playbook, Playbooks and Solutions, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Add a price adjustment definition to a decision table​ in License and Permit Playbook

As an admin, you can use a price adjustment definition in the License and Permit Playbook to add adjustments to field prices based on the conditions of fields that are not price fields​, such as the residency status of the constituent for the location they are requesting the permit or license in.

## Before you begin

Role required: admin

## About this task

A base amount can be entered and saved for each license/permit option, and can be modified from its current value to a new value based on one or more control conditions. A price adjustment definition consists of only one price field, and as an admin, you can create multiple.​

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Decision Tables**, and open a decision table that has been associated with a License and Permit case type​.

    For information on how to associate a decision table with the case type, see [Associate a decision table with a License &amp; Permit case type​​](psds-associate-decision-table-with-lpr.md).

    You should be brought to Workflow Studio.

2.  Select **Add condition column**.

3.  Set the Input to **case**, and set Data to evaluate to **Field**.​

4.  Under Field, select the field that controls the pricing for the price adjustment in question.

5.  Enter the name of the aforementioned field in the condition column label​, and select **Done**.

6.  Repeat steps 4-6 for all price control fields​.

7.  Select **Add new decision row**.

8.  Select the newly added cell under any of the price control columns to add control conditions.

9.  Specify the control condition for that field.

    If the field type is a choice, the input value cannot be “None”. Select the appropriate condition from the dropdown.

10. Repeat steps 11-12 to add conditions for other control fields.​

11. If the price field where the adjustment applies is set to choice, enter the price choice affected.If the price field where the adjustment applies is not choice, set the value to true.​

12. Enter the adjustment price in the newly-added cell under the Price column, the price when those control conditions apply.

    If the price field is a Boolean, the value of the price field has to be set to **true**​. If the price field is a choice, the value of the price field cannot be set to **none**​. Enter the value of the adjustment price in the field.

13. Select **Save**, then **Close**.


