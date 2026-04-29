---
title: Configure system properties for Save as draft option
description: Configure the system properties to enable the Save as draft option for some catalog item. For example, on the permit to work form or for password reset.
locale: en-US
release: australia
product: Contractor Service Center
classification: contractor-service-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Contractor Service Center, Health and Safety, Employee Service Management]
---

# Configure system properties for Save as draft option

Configure the system properties to enable the **Save as draft** option for some catalog item. For example, on the permit to work form or for password reset.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** and enter `sys_properties.list` in the navigation filter.

    The System properties \[sys\_properties\] table appears.

2.  In the **Name** column, search for `glide.sc.enable.save_as_draft.portal.csc`.

3.  Select the **glide.sc.enable.save\_as\_draft.portal.csc** property.

4.  Update the **Value** field to.

    |Value|Result|
    |-----|------|
    |**True**|Enables **Save as draft** option.|
    |**False**|Disables **Save as draft** option.|

5.  Select **Update**.


**Parent Topic:**[Configuring Contractor Service Center](../concept/hs-configure-contractor-service-center.md)

