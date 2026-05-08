---
title: Configure an appointment booking record producer
description: Configure an appointment booking record producer and enable the appointment booking variable set to display the correct fields in that record producer.
locale: en-US
release: australia
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure Appointment Booking, Configuring Appointment Booking, Additional scheduling configuration options, Setting up a Field Service scheduling method, Configure, Field Service Management]
---

# Configure an appointment booking record producer

Configure an appointment booking record producer and enable the appointment booking variable set to display the correct fields in that record producer.

## Before you begin

Enable the appointment booking variable set to display the appointment selection widget on the record producer.

Role required: catalog\_admin

## About this task

A record producer is a specific type of catalog item that creates task-based records, such as appointment records, from the service catalog. Appointment booking supports both work order and task extended tables. You can use record producers to create the required task records before creating any appointment record. For more information, see Record Producer.

The variable set **sn\_appointment\_variable\_set** adds Calendar component to the catalog and record producer.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definitions** &gt; **Record Producers**.

2.  Click the desired record producer.

3.  In the **Variable Sets** related list, click **Edit**.

4.  Select **sn\_appointment\_variable\_set** and move it to the Variable Sets list.

5.  Click **Save**.


