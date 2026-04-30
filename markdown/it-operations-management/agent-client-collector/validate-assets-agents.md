---
title: Validate plugins on agents
description: Validate plugins on your agents to ensure that they match the plugins on your ServiceNow instance. Validating plugins ensures that the instance provides accurate data on all of your agents' plugins.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Agent Client Collector, IT Operations Management]
---

# Validate plugins on agents

Validate plugins on your agents to ensure that they match the plugins on your ServiceNow instance. Validating plugins ensures that the instance provides accurate data on all of your agents' plugins.

## Before you begin

Role required: agent\_client\_collector\_admin

## About this task

Only plugins that are able to be executed are validated. For example, if you’re running an agent on a macOS, only macOS plugins on your instance are validated.

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Agents**.

2.  Select an agent on the **Agent Client Collectors** page.

3.  Select the **Validate ACC Plugins** link.

    The **Queues** page appears, displaying the ECC queue.

4.  Refresh the queue to view the new input record.

5.  Select the record to view its results.

    Validation status is visible in the **Payload** section of the form.

    If plugins aren't validated, navigate back to the **Agent Client Collectors** page and select the **Clear ACC Plugins** link.

    The plugins automatically re-sync the next time a command runs which requires the plugin.


