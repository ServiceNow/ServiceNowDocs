---
title: Reestablish connection after a clone for a provider
description: After you clone your instance, you must reestablish the connection between the provider and consumer instances.
locale: en-US
release: australia
product: Service Exchange
classification: service-exchange
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use for providers, Service Exchange for Providers, Service Exchange]
---

# Reestablish connection after a clone for a provider

After you clone your instance, you must reestablish the connection between the provider and consumer instances.

## Before you begin

Role required: admin

The clone must be completed. For more information on cloning, see [Instance Clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md).

## About this task

After you clone your Service Exchange, the inbound and outbound connections move to an error or down state. You must reestablish the connection between provider and consumer target instances to promote proper functionality.

## Procedure

1.  Navigate to **All** &gt; **Service Exchange Provider** &gt; **Consumer**.

    You see the Inbound and Outbound fields for the cloned consumer are in an error state.

2.  Open the Consumer connection record by selecting the record number in the Number column.

3.  From the related list, select **RPS connections** &gt; **Consumer Instance**.

4.  In the Process Sync Remote System Consumer Instance page, select the **Validate and Activate Remote System** related links.

5.  Activate inactive Capture Definitions.

    1.  Navigate to **All** &gt; **IntegrationHub** &gt; **Remote Process Sync** &gt; **Process Sync Definitions**.

    2.  Select the Service Exchange Provider Definition.

    3.  Select the Capture Definitions related list, change the state of all inactive capture definition to **Active**.


## Result

The state of the Outbound and the Inbound fields changes to **Active**.

**Parent Topic:**[Using Service Exchange for providers](../concept/service-bridge-v2-administer.md)

**Related topics**  


[Reestablish connection after a clone for a consumer](service-bridge-v2-cloning-instances-con.md)

[List of preservers and exclusions tables for cloning](../reference/service-bridge-v2-cloning.md)

