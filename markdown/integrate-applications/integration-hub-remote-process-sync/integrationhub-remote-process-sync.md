---
title: Integration Hub Remote Process Sync
description: Integration Hub Remote Process Sync enables you to set up one-way or bidirectional integrations among multiple ServiceNow instances, so that your process flows stay in sync.
locale: en-US
release: zurich
product: Integration Hub Remote Process Sync
classification: integration-hub-remote-process-sync
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Workflow Data Fabric]
---

# Integration Hub Remote Process Sync

Integration Hub Remote Process Sync enables you to set up one-way or bidirectional integrations among multiple ServiceNow instances, so that your process flows stay in sync.

**Note:** Integration Hub Remote Process Sync requires an Integration Hub subscription. For more information, see [Legal schedules - Integration Hub overview](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/snc-addendum-integrationhub.pdf).

An Integration Hub Remote Process Sync integration lets you span automated workflows for your business process across multiple ServiceNow instances. As a service provider, keep multiple customer instances in sync automatically, using Workflow Studio subflows to automate your process's workflows for all of your customers.

![Keep process flows across multiple instances in sync. For example, automate software request fulfilment among customer and vendor instances.](../images/remote-process-sync-overview.png)

## Benefits

Integration Hub Process Sync provides you with these benefits:

-   Automate cross-enterprise automated processes that span multiple instances, keeping various process stakeholders up-to-date
-   Manage how to synchronize and correlate your record, attachment, and journal field data across multiple instances
-   Ensure order delivery for data updates in remote instances, using a standalone correlation engine and queueing system
-   Manage and troubleshoot errors and outages in your automated mutli-instance processes with the built-in execution engine in Workflow Studio.

## Roles

By default, Remote Process Sync provides the following roles that you can assign to users:

|Role|Users with this role can|
|----|------------------------|
|ih\_process\_sync|Create, update, or delete process sync definitions and related records.|
|ih\_process\_sync\_api|Access Remote Process Sync APIs only.|
|ih\_process\_sync\_run\_as|Run outbound and inbound flows associated with a process sync definition. This user must have access to the tables for which any records are created or updated in the flow.|

## Domain separation

You can use Remote Process Sync to synchronize process flows among multiple domain-separated instances. In a domain-separated environment, the following conditions apply:

1.  When building your integration
    -   Configuration tables have a sys\_domain, and data is domain separated.
    -   Configuration tables are meant to be in the same domain as the parent configuration record.
    -   Subflows may be chosen from the current or any parent domain.
    -   No tables have sys\_overrides , and thus cannot override business rules or UI actions from parent domains.
2.  When your integration runs
    -   Only records from the configuration domain and associated child domains are captured.
    -   Queue tables have a sys\_domain. The outbound record is stored in the same domain as the captured source record. The inbound record is stored in the same domain as the Inbound API user in the Remote System record.
    -   The outbound subflow runs in the same domain as the queued record.
    -   The inbound subflow runs in the same domain as the user specified in the Remote System record's Run Inbound Flows as field.

## Getting started

Before deciding to move forward with Remote Process Sync as your integration framework, consider how this framework compares to other multi-instance ServiceNow AI Platform® integrations. While solutions such as [Instance Data Replication](https://www.servicenow.com/docs/access?context=instance-data-replication&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US) and the [Remote Instance spoke](../../integrationhub-store-spokes/concept/remote-instance-spoke-1.md) support simple multi-instance integrations, Remote Process Sync supports more complex multi-instance integration use cases, focusing on integrating instances by high-level business processes.

**Note:** Remote Process Sync replaces the eBonding spoke for integrating instances.

![Instance Data Replication and the Remote Instance spoke support simple integrations for an entire table or using ServiceNow AI Platform APIs. Remote Process Sync supports more complex multi-instance integrations.](../images/idr-remotespoke-rps-comparison.png "Comparison of Instance Data Replication, Remote Instance spoke, and Remote Process Sync")

When you're ready to start building and managing a Remote Process Sync integration, learn the basics of [Getting started with Remote Process Sync](../reference/getting-started-with-remote-process-sync.md).

