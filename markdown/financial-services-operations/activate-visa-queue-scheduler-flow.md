---
title: Configure the Visa Queue Scheduler Flow
description: Use the Visa Queue Scheduler Flow to control the frequency at which Visa batch queues are processed. This flow runs as a scheduled job at a predefined time interval, triggering the subflow that processes incoming batch queues.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Visa, Integrate, Financial Services Operations \(FSO\)]
---

# Configure the Visa Queue Scheduler Flow

Use the Visa Queue Scheduler Flow to control the frequency at which Visa batch queues are processed. This flow runs as a scheduled job at a predefined time interval, triggering the subflow that processes incoming batch queues.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  In the Search field, search for **Visa Queue Scheduler Flow**.

3.  To set the conditions and frequency for the flow, select the **Trigger** field.

    Locate the flow you want to activate from the list of saved flows and open it.

4.  Select **Activate**.

    **Note:** When using Financial Services Operations Integration with Visa for the first time, you must activate the Visa Queue Scheduler Flow and set the desired frequency. For more information, see [Batch queue APIs processing and scheduling](../reference/components-installed-with-the-financial-services-operations-integration-with-visa.md#section_hfv_ms5_n2c).


**Parent Topic:**[Configuring Financial Services Operations Integration with Visa](configuring-financial-services-operations-integration-with-visa.md)

