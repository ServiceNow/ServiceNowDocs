---
title: Validate plugins on the MID Server
description: Validate plugins on your MID Server to ensure that they match the plugins on your ServiceNow instance. Validating plugins ensures that the instance provides accurate data on all of your MID Server plugins.
locale: en-US
release: australia
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ACC deployment - servers, Configuring Agent Client Collector, Agent Client Collector, IT Operations Management]
---

# Validate plugins on the MID Server

Validate plugins on your MID Server to ensure that they match the plugins on your ServiceNow instance. Validating plugins ensures that the instance provides accurate data on all of your MID Server plugins.

## Before you begin

Role required: agent\_client\_collector\_admin

## Procedure

1.  Navigate to **All** &gt; **Agent Client Collector** &gt; **Deployment** &gt; **MID Servers**.

2.  Select a MID Server entry on the MID Servers page.

3.  Select the **Validate ACC Plugins** link.

    The **Queues** page appears, displaying the ECC queue.

4.  Refresh the queue to view the new input record.

5.  Select the record to view its results.

    Validation status is visible in the **Payload** section of the form.

    If plugins aren't validated, restart the MID Server. Plugins sync automatically when the MID Server restarts.


**Parent Topic:**[Deploying Agent Client Collector on servers](../concept/acc-server-deployment.md)

