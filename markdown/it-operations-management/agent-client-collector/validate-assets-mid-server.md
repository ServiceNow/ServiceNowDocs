---
title: Validate assets on the MID Server
description: Validate assets on your MID Server to ensure that they match the assets on your ServiceNow instance. Validating assets ensures that the instance provides accurate data on all of your MID Server assets.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enabling Agent Client Collector data collection, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Validate assets on the MID Server

Validate assets on your MID Server to ensure that they match the assets on your ServiceNow instance. Validating assets ensures that the instance provides accurate data on all of your MID Server assets.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **MID Servers**.

2.  Select a MID Server entry on the MID Servers page.

3.  Select the **Validate Assets** link.

    The **Queues** page appears, displaying the ECC queue.

4.  Refresh the queue to view the new input record.

5.  Select the record to view its results.

    Validation status is visible in the **Payload** section of the form.

    If assets aren't validated, restart the MID Server. Assets sync automatically when the MID Server restarts.


**Parent Topic:**[Enabling Agent Client Collector data collection](../concept/data-collection-enabling.md)

