---
title: Set system properties for scheduler
description: Set the system property sn\_ap\_apm.exception.engine.scheduler\_cool\_off\_period which defines the time interval in minutes after which the invoice is picked for processing.
locale: en-US
release: zurich
product: Accounts Payable Operations
classification: accounts-payable-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Components installed with Accounts Payable Invoice Processing, Install Accounts Payable Invoice Processing, Configure, Accounts Payable Operations, Finance and Supply Chain]
---

# Set system properties for scheduler

Set the system property `sn_ap_apm.exception.engine.scheduler_cool_off_period` which defines the time interval in minutes after which the invoice is picked for processing.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All**.

2.  Search `sys_properties_list.do` and open the system property.

3.  Search for `sn_ap_apm.exception.engine.scheduler_cool_off_period` and open the system property.

    The system property `sn_ap_apm.exception.engine.scheduler_cool_off_period` opens as a record. The **Value** field displays the default value as 240. You can edit the record in editing mode.

4.  In the **Value** field, you can enter the value according to your choice.

5.  Select **Update**.


## Result

The system properties for scheduler is set.

**Related topics**  


[Set APO properties](set-apo-properties.md)

