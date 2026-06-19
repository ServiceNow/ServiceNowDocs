---
title: Prepare to run the Fivetran collector
description: Create a Fivetran API key before running the collector.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/workflow-data-fabric/prepare-to-run-fivetran-collector.html
release: australia
product: Workflow Data Fabric
classification: workflow-data-fabric
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Fivetran metadata collector, Configuring metadata collectors, Data Catalog, Workflow Data Fabric]
---

# Prepare to run the Fivetran collector

Create a Fivetran API key before running the collector.

## Before you begin

Role required: admin

## About this task

The collector authenticates using a Fivetran API key. The API key owner must have read access to destinations and connectors.

## Procedure

1.  Create a Fivetran API key with read access to destinations and connectors.

    See the [Fivetran role-based access control documentation](https://fivetran.com/docs/getting-started/fivetran-dashboard/account-management/role-based-access-control#rolesinourrbacmodel) for details on creating API keys and assigning permissions.

2.  Save the **API Key** and **API Secret**.

    You need these credentials when configuring the collector.


**Parent Topic:**[Fivetran metadata collector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/workflow-data-fabric/fivetran-metadata-collector.md)

