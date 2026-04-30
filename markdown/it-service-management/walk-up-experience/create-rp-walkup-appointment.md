---
title: Create a record producer to capture Walk-up Experience appointment records
description: Capture Walk-up Experience appointment records by creating unique record producers for your individual walk-up locations. The Appointment Booking Service Configuration form contains required fields that refer to variables in the associated record producer.
locale: en-US
release: zurich
product: Walk-Up Experience
classification: walk-up-experience
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure Walk-up Experience appointment booking, Walk-up Experience appointment booking administration, Book Walk-up Experience appointments, Configure, Walk-up Experience, IT Service Management]
---

# Create a record producer to capture Walk-up Experience appointment records

Capture Walk-up Experience appointment records by creating unique record producers for your individual walk-up locations. The Appointment Booking Service Configuration form contains required fields that refer to variables in the associated record producer.

## Before you begin

Role required: appointment\_booking\_admin or admin

## About this task

In order to properly configure your walk-up location services for appointment booking, you must first create a unique record producer for each walk-up location. You must also add variable sets to the record producer. By creating the unique record producer with appropriate variable sets, you can capture all your walk-up appointment records for each location.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Record Producers**.

2.  Click **New** to open the Record Producer New Record form.

3.  Provide a unique name for the record producer in the **Name** field.

4.  Search for and select **Walk-up Appointment \[wu\_appointment\]** in the **Table name** field.

5.  Provide a short description for added detail.

6.  Click **Submit**.

7.  Return to the Record Producers list and search for your newly created record producer.

8.  Click to open your newly created record producer.

9.  Scroll down the form and click to open the Variable Sets tab.

10. Select **Edit** to add the appropriate variable sets to the record producer.

11. Select and add the following variable sets to the record producer using the add button: *sn\_appointment\_variable\_set* and *sn\_walkup\_variable\_set*.

12. Click **Save**.


**Parent Topic:**[Configure Walk-up Experience appointment booking](../concept/walkup-appointment-booking-config.md)

