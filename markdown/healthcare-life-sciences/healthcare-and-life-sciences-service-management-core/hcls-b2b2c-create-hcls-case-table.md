---
title: Create a table for B2B2C in Healthcare and Life Sciences Service Management Core
description: Create a table that extends the Healthcare case table.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [B2B2C with Healthcare and Life Sciences Service Management Core, Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Create a table for B2B2C in Healthcare and Life Sciences Service Management Core

Create a table that extends the Healthcare case table.

## Before you begin

Assign the case viewer role for contacts. For more information, see [Assign the case viewer role for contacts in B2B2C in Healthcare and Life Sciences Service Management Core](hcls-b2b2c-grant-contact-case-creation.md).

Role required: admin

## About this task

The Healthcare and Life Sciences Service Management Core case table must be extended in order for new cases to be created.

## Procedure

1.  Navigate to **System Definitions** &gt; **Tables**.

2.  Click **New**.

3.  On the form, enter a label.

4.  Set the **Extends table** field to the **Healthcare case** table.

5.  In the Controls related list, add the **sn\_customerservice.customer** user role.


## Result

A table is created that extends the Healthcare case table for use with B2B2C.

## What to do next

Create a record producer for use with B2B2C. For more information, see [Create a record producer for B2B2C in Healthcare and Life Sciences Service Management Core](hcls-b2b2c-create-record-producer.md).

