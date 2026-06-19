---
title: Configure the Visa Queue Scheduler Flow
description: Use the Visa Queue Scheduler Flow to control the frequency at which Visa batch queues are processed. This flow runs as a scheduled job at a predefined time interval, triggering the subflow that processes incoming batch queues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/financial-services-operations/financial-services/activate-visa-queue-scheduler-flow.html
release: zurich
product: Financial Services
classification: financial-services
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

    **Note:** When using Financial Services Operations Integration with Visa for the first time, you must activate the Visa Queue Scheduler Flow and set the desired frequency. For more information, see [Batch queue APIs processing and scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/components-installed-with-the-financial-services-operations-integration-with-visa.md).


**Parent Topic:**[Configuring Financial Services Operations Integration with Visa](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/financial-services-operations/financial-services/configuring-financial-services-operations-integration-with-visa.md)

