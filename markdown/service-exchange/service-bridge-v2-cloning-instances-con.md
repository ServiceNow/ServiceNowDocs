---
title: Reestablish connection after a clone for a consumer
description: After you clone your instance, you must reestablish the connection between the consumer and provider instances.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use for consumers, Service Exchange for Consumers, Service Exchange]
---

# Reestablish connection after a clone for a consumer

After you clone your instance, you must reestablish the connection between the consumer and provider instances.

## Before you begin

Role required: admin

The clone must be completed. For more information on cloning, see Instance Clone.

## About this task

After you clone your Service Exchange, the inbound and outbound connections move to an error or down state. You must reestablish the connection between provider and consumer target instances to promote proper functionality.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Provider Connections**.

    You see the Inbound and Outbound fields are in an error state.

2.  Open the Provider connection record by selecting the record number in the Number column.

3.  From the related list, select **RPS connections** &gt; **Provider Instance**.

4.  In the Process Sync Remote System Provider Instance page, select the **Validate and Activate Remote System** related links.

5.  Activate inactive Capture Definitions.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**.

    2.  Select the Service Exchange Customer Definition.

    3.  Select the Capture Definitions related list, change the state of all inactive capture definition to **Active**.


**Related topics**  


[Reestablish connection after a clone for a provider](service-bridge-v2-cloning-instances.md)

[List of preservers and exclusions tables for cloning](../reference/service-bridge-v2-cloning.md)

