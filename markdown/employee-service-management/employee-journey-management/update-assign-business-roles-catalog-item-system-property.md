---
title: Update the assign\_business\_roles\_catalog system property
description: The assign\_business\_roles\_catalog system property enables you to assign business roles to users through a catalog item as part of a lifecycle event, and is included with the Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin. If you are using a custom catalog item with your lifecycle event, you must update the system property with the sys id of that item.
locale: en-US
release: zurich
product: Employee Journey Management
classification: employee-journey-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Business roles, Lifecyle events for enterprise, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Update the assign\_business\_roles\_catalog system property

The **assign\_business\_roles\_catalog** system property enables you to assign business roles to users through a catalog item as part of a lifecycle event, and is included with the Lifecycle Events for Enterprise \[com.sn\_hr\_lifecycle\_ent\] plugin. If you are using a custom catalog item with your lifecycle event, you must update the system property with the sys id of that item.

## Before you begin

Copy the sys id of the catalog item that you want to use to assign business roles as part of a lifecycle event.

Role required: sn\_hr\_le\_ent.admin

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

    The System Properties list is displayed.

2.  Open the **sn\_hr\_le\_ent.assign\_business\_roles\_catalog** record.

3.  In the **Value** field, add the sys id of the catalog item that will be used to assign business roles as part of a lifecycle event.

    **Note:** The default value is the sys id of the **Assign business roles to new hire** catalog item that is included as part of the demo data for the lifecycle event for new hire onboarding.

    ![Add the sys id of the catalog item that will be used to assign business roles as part of a lifecycle event.](../image/business-roles-system-property.png)

4.  Click **Update**.


**Parent Topic:**[Business roles](../concept/business-roles.md)

