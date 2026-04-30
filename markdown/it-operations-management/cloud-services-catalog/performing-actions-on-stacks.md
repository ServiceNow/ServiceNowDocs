---
title: Actions on stacks
description: Access a particular stack to perform a Day 2 or life-cycle operations such as stop, start, deprovision, ModifyLease, or ModifySchedule.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Exploring the My Stacks tab, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Actions on stacks

Access a particular stack to perform a Day 2 or life-cycle operations such as stop, start, deprovision, ModifyLease, or ModifySchedule.

When you request a life-cycle operation on a stack or resource, the system generates a change request. An approval policy specifies that the change is auto-approved or that a user on the approver list must approve the change.

The stacks and resources undergo life-cycle operations from the time that they're started, provisioned, de-provisioned, and then stopped. At times, you must update or stop a particular resource's schedule for configuration issues. You can select a stack or resource to perform these operations. The actions include only the appropriate operations for the selected resource or stack. Not all operations are supported for all providers or for all service categories \(resource types\) by default.

The following example shows the actions that the Cloud Services Catalog application supports on stacks. The actions are stop, start, deprovision, ModifyLease, or ModifySchedule.

![Actions on stacks.](../image/performing-actions-on-stacks.png "Actions on stacks")

The following table lists the operations that the Cloud Services Catalog application supports as actions on stacks.

|Action|Function|
|------|--------|
|Stop|Stops the selected virtual machine \(VM\). The resource status changes to off. No setting is required.|
|Start|Starts the VM that you select. The resource status changes to on. No setting is required.|
|Deprovision|Terminates the selected stack and sends a notification to the stack owner. No setting required.|
|ModifyLease|Changes the lease end date.|
|ModifySchedule|Modifies the schedule profile and schedule time zone.|

**Parent Topic:**[Exploring the My Stacks tab](manage-stacks.md)

