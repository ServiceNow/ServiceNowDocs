---
title: Redirect to the Service Operations Workspace home page
description: Enable quick task prioritization by directing agents to the homepage immediately upon logging into the ServiceNow instance. This improves workflow efficiency by granting agents immediate access to essential tools and information, facilitating the timely resolution of critical tasks and issues.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Customize the SOW for ITOM home page, Configuring SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Redirect to the Service Operations Workspace home page

Enable quick task prioritization by directing agents to the homepage immediately upon logging into the ServiceNow instance. This improves workflow efficiency by granting agents immediate access to essential tools and information, facilitating the timely resolution of critical tasks and issues.

## Before you begin

Ensure that the value of the **glide.login.home property** is set to `/now/nav/ui/home`. This property specifies the default homepage that is displayed upon logging in.

Role required: evt\_mgmt\_admin

## Procedure

1.  Select **All** and then search for `sys_properties.list`.

2.  Add the **sn\_sow.service\_desk\_groups** property.

3.  In the **Value** field, enter the sys\_id of the user group to which the operator belongs.

    **Note:** If you want to specify multiple service desk groups, add a comma-separated list of group sys\_ids in the value field.

4.  Select **Update**.


**Parent Topic:**[Customize the Service Operations Workspace for ITOM home page](customize-sow-landing-page-itom.md)

