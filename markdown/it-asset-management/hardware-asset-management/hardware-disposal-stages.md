---
title: Hardware disposal order stages
description: A hardware disposal order goes through various stages in the disposal process before it’s completed. With each stage, the task that's associated with that stage changes too.
locale: en-US
release: yokohama
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Hardware Asset Management reference, Hardware Asset Management, IT Asset Management]
---

# Hardware disposal order stages

A hardware disposal order goes through various stages in the disposal process before it’s completed. With each stage, the task that's associated with that stage changes too.

Closing a task in the hardware disposal process completes that task and automatically creates the next task in the process. For example, after you close the Schedule Pickup task, the state for that task changes to Closed Complete and the next task, Asset Departure, is created. This process continues until you close all the tasks required for disposing of the selected assets. After you close all the tasks, the disposal order is completed.

|Hardware disposal stages|Task|Description|
|------------------------|----|-----------|
|Draft|Verify Assets|Hardware disposal record is created.|
|Scheduling|Schedule Pickup|Scheduling details for the hardware asset disposal order.|
|Transit|Asset Departure|Verified assets are ready for departure.|
|Confirmation|Vendor Confirmation|Hardware disposal order is confirmed by the vendor.|
|Documentation|Disposal Documentation|Documentation for the disposal record is attached.|
|Completed|None|Hardware disposal record request is completed.|
|Cancelled|None|Disposal order can be canceled only until the transit stage.|

**Parent Topic:**[Hardware Asset Management reference](../concept/reference-hardware-asset-management.md)

