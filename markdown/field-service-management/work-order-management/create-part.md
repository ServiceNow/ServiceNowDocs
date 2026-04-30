---
title: Create and source a part requirement request on the Field Service Contractor Portal
description: Create a part requirement request for a work order task that is assigned to you.
locale: en-US
release: zurich
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Requesting and receiving required parts, Contractor Portal, Completing work orders on the web interface, Use, Field Service Management]
---

# Create and source a part requirement request on the Field Service Contractor Portal

Create a part requirement request for a work order task that is assigned to you.

## Before you begin

Role required: wm\_ext\_agent and wm\_ext\_manager

## About this task

Creating a part requirement request automatically creates a part requirement number and a transfer order number so you can view the required part details and source the part.

## Procedure

1.  Navigate to **All** &gt; **Field Service Contractor Portal** &gt; **Homepage** &gt; **Requests** &gt; **Create and Source Parts**.

2.  On the form, fill in the fields.

3.  |Field|Description|
|-----|-----------|
|Task Number|Number assigned to the work order task. Select a task that is not in the Closed or Canceled state.|
|Model|The part model needed to complete the work order task.|
|Required by date|Date by which all parts should be delivered. The date is filled in automatically based on the expected travel start time provided in the work order task. If necessary, change the date manually.|
|Required quantity|Total quantity necessary to complete the work order task. This field becomes read-only when a hardware item is selected in the Model field.|
|From Stockroom|Location of the stockroom from which the item is to be shipped.|
|To Stockroom|Location of the stockroom where the item is to be shipped.|
|Asset|Asset requested by the transfer order line, for example, a specific printer.|

4.  Click **Submit**.


## Result

The **Part Requirements** and **Transfer Orders** related list is updated automatically with the part requirements information in the work order task form.

