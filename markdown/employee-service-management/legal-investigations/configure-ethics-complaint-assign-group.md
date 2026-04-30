---
title: Configure system properties to update ethics complaint assignment group
description: As an admin, configure the sn\_lg\_investigate.ethics\_complaints\_assignment\_group system property to use a different assignment group to assign ethics complaints.
locale: en-US
release: yokohama
product: Legal Investigations
classification: legal-investigations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up Legal Investigations, Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Employee Service Management]
---

# Configure system properties to update ethics complaint assignment group

As an admin, configure the `sn_lg_investigate.ethics_complaints_assignment_group` system property to use a different assignment group to assign ethics complaints.

## Before you begin

Role required: sn\_lg\_ops.legal\_admin

## About this task

`sn_lg_investigate.ethics_complaints_assignment_group` is a configurable system property that is used to configure default assignment group for ethics complaints raised using quick links in Employee Center. The sys\_id of any group that is protected with the Universal Request sensitive role and has fulfillers who can work on ethics complaints is enabled to configure the system property.

Alternatively, configure the property from [Set up Legal Investigations with HR Service Delivery Employee Relations](integrate-lsd-hrsd.md#step_li_prop_group).

## Procedure

1.  In the filter navigator, enter `sys_properties.list`.

2.  In the **Name** column, search for the `sn_lg_investigate.ethics_complaints_assignment_group` property.

3.  Select the property.

4.  If you aren’t able to edit the property in the current application scope, select the word **here** in the message at the top of the page.

5.  Update the **Value** field with the sys\_id of the new assignment group.

6.  Select **Update**.


## Result

You can now use the new assignment group to assign ethics complaints.

