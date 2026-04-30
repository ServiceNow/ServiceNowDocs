---
title: Validate assets on agents
description: Validate assets on your agents to ensure that they match the assets on your ServiceNow instance. Validating assets ensures that the instance provides accurate data on all of your agents' assets.
locale: en-US
release: yokohama
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Enabling Agent Client Collector data collection, Agent Client Collector Framework, Agent Client Collector, IT Operations Management]
---

# Validate assets on agents

Validate assets on your agents to ensure that they match the assets on your ServiceNow instance. Validating assets ensures that the instance provides accurate data on all of your agents' assets.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Only assets that are able to be executed are validated. For example, if you’re running an agent on a macOS, only macOS assets on your instance are validated.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select an agent on the **Agent Client Collectors** page.

3.  Select the **Validate Assets** link.

    The **Queues** page appears, displaying the ECC queue.

4.  Refresh the queue to view the new input record.

5.  Select the record to view its results.

    Validation status is visible in the **Payload** section of the form.

    If assets aren't validated, navigate back to the **Agent Client Collectors** page and select the **Clear Assets** link.

    The assets automatically re-sync the next time a command runs which requires the asset.


**Parent Topic:**[Enabling Agent Client Collector data collection](../concept/data-collection-enabling.md)

