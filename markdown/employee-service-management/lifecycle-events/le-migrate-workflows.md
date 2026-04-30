---
title: Migrate Lifecycle Events workflows
description: Lifecycle Events customers upgrading from the Washington DC or Xanadu release to the Yokohama release can use a system property to define the workflow technology that the Lifecycle Events app uses for its base system workflows.
locale: en-US
release: zurich
product: Lifecycle Events
classification: lifecycle-events
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Configure, Lifecycle Events, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Migrate Lifecycle Events workflows

Lifecycle Events customers upgrading from the Washington DC or Xanadu release to the Yokohama release can use a system property to define the workflow technology that the Lifecycle Events app uses for its base system workflows.

## Before you begin

Role required: admin \[sn\_hr\_le.admin\]

## About this task

In the Yokohama release, existing customers with Lifecycle Events can use the **sn\_hr\_le.use\_flow** property to migrate each base system workflow that is installed with the app from workflow to flow. This migration enables Lifecycle Events to use flow, the current workflow technology for process automation, rather than workflow, an older workflow technology associated with a legacy product.

The following Lifecycle Events workflows are migrated to flows when you set the **Value** field to **True** in the **sn\_hr\_le.use\_flow** property:

-   Account Notification
-   Add LE activity user to Pulse Survey
-   HR Activity Launcher
-   HR Activity Set Launcher
-   HR Activity Set Trigger Check
-   Lifecycle Event Case Approval
-   Lifecycle Event Notification

Additionally, two configurations are added to the Activity Configurations \[sn\_hr\_le\_fulfiller\_activity\_config\] table when you set the **Value** field to **True** in the **sn\_hr\_le.use\_flow** property. The configurations for the following activities are added to the table to support the corresponding flows:

|Activity|Flow|
|--------|----|
|Approval|Lifecycle Event Case Approval|
|Notification|Lifecycle Event Notification|

The **Configuration Type** field is set to **Flow \(Template\)** in the Activity Configuration record for the previously mentioned activities to support the use of flow.



The **Value** field in the **sn\_hr\_le.use\_flow** property has different default values depending on whether you’re an existing or new Lifecycle Events customer. Beginning with the Yokohama release, for new customers implementing Lifecycle Events, the **Value** field in the **sn\_hr\_le.use\_flow** property is set to **True** by default. Conversely, for existing customers with Lifecycle Events who are upgrading to the Yokohama release, the **Value** field in the **sn\_hr\_le.use\_flow** property is set to **False** by default.

**Important:** This task pertains to existing customers with Lifecycle Events who are upgrading to the Yokohama release. Existing customers should perform this task in a non-production instance to validate whether the underlying changes to Lifecycle Events produce any adverse effects. Only perform this task in your production instance after you thoroughly test and are satisfied with the results.

## Procedure

1.  Navigate to the **All** menu, and enter `sys_properties.list` in the navigation filter.

    The System Properties \[sys\_properties\] table appears.

2.  Select **Name** from the drop-down list associated with the **Search** field.

3.  In the **Search** field, enter `*sn_hr_le`.

    A list of system properties associated with Lifecycle Events appears.

4.  Select the **sn\_hr\_le.use\_flow** property.

5.  Use the **Value** field to specify the option that corresponds with the workflow technology you want Lifecycle Events to use for its base system workflows.

    |Option|Description|
    |------|-----------|
    |**True**|Flow|
    |**False**|Workflow|

6.  Select **Update**.


## What to do next

Using Lifecycle Events builder, delete your existing activity for an approval and recreate a new one. To help identify your existing activity for an approval, ensure the **Activity Type** field in the corresponding Activity record is set to **Approval**.

A new activity for an approval must be created so it can use the corresponding configuration for an approval in the Activity Configurations table. The activity for an approval that you create after setting the **Value** field to **True** in the **sn\_hr\_le.use\_flow** property uses the Activity Configuration record containing the following field values:

-   **Activity** field set to **Approval**.
-   **Configuration Type** field set to **Flow \(Template\)**.

For more information about the Lifecycle Events activity creation process, see [Configure a lifecycle event activity](configure-hr-lifecycle-event-activity.md#).

