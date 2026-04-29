---
title: Configuring data mapping
description: Configure the work order templates to fetch data from a source table to populate fields in a work order form while creating a work order. The source table can be case, incident, change, or others depending on the source of origin for a work order.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Template Management, Work orders, Set up work orders and tasks, Configure, Field Service Management]
---

# Configuring data mapping

Configure the work order templates to fetch data from a source table to populate fields in a work order form while creating a work order. The source table can be case, incident, change, or others depending on the source of origin for a work order.

You first create a table map to specify the fields to be copied from the source table to the work order table and then link the table mapping to a work order template. The extension points in template management, enables your work order template to process the followings configuration. For more information, see [Extension points in Field Service Management](../reference/extension-points-field-service.md).

## Configuration overview

The steps for setting up data mapping configurations are:

1.  [Create field mapping from a source table to a work order](../task/map-source-table-to-wo.md)

    Use table mapping to ensure that when a work order is created from its source, the information from the source table is copied to the appropriate target fields in the work order.

2.  [Enable work order template to fetch data from the source table](../task/associate-table-mappings-with-wotemplate.md)

    Enable work order template to identify the source of work order and then map data from that source table to the work order fields.


