---
title: Assign the case viewer role for contacts in B2B2C in Healthcare and Life Sciences Service Management Core
description: Contacts must have the sn\_hcls.case\_viewer role for read access to healthcare case fields.
locale: en-US
release: yokohama
product: Healthcare and Life Sciences Service Management Core
classification: healthcare-and-life-sciences-service-management-core
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [B2B2C with Healthcare and Life Sciences Service Management Core, Configure, Healthcare and Life Sciences Service Management Core, Healthcare and Life Sciences Service Management, Healthcare and Life Sciences]
---

# Assign the case viewer role for contacts in B2B2C in Healthcare and Life Sciences Service Management Core

Contacts must have the sn\_hcls.case\_viewer role for read access to healthcare case fields.

## Before you begin

Configure the account consumer related list to add account consumers. For more information, see [Configure the account consumer related list to add account consumers for B2B2C in Healthcare and Life Sciences Service Management Core](hcls-configure-related-list-b2b2c.md).

Role required: admin

## Procedure

1.  Navigate to **User Administration** &gt; **Users**.

2.  Select a user.

3.  Click the Roles related list.

4.  Click **Edit**.

5.  Add **sn\_hcls.case\_viewer** to the roles list.


## Result

Contacts now have read access to healthcare case fields for use with B2B2C.

## What to do next

Create a table for use with B2B2C. For more information, see [Create a table for B2B2C in Healthcare and Life Sciences Service Management Core](hcls-b2b2c-create-hcls-case-table.md).

