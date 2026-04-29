---
title: Configuring Template Management for Field Service
description: Set up the advanced configurations for work order templates to enable the templates to process data dynamically instead of using the static information described in the work order templates.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Work orders, Set up work orders and tasks, Configure, Field Service Management]
---

# Configuring Template Management for Field Service

Set up the advanced configurations for work order templates to enable the templates to process data dynamically instead of using the static information described in the work order templates.

Template Management for Field Service provides advanced configurations for work order templates that enable the templates to work dynamically while creating a work order.

As an administrator, you can use templates to dynamically identify the information for populating fields in a work order and creating tasks through the following procedures:

-   Enable the work order templates to map information from source table to work order attributes. For more information, see [Configuring data mapping](setting-up-wo-temp-copy-source-info-wo.md).
-   Identify and create appropriate tasks for a work order based on the defined filtering conditions. For more information, see [Configuring standalone task templates](setting-up-wotemp-create-stand-alone-tasks.md).
-   Use extension points to customize the process of identifying the source of work order. For more information, see [Extension points in Field Service Management](../reference/extension-points-field-service.md).

## Configuration overview

The steps for setting up template management are:

1.  [Activate Template Management for Field Service](../task/activate-template-management.md)

    Install the Template Management for Field Service plugin \(com.snc.fsm\_template\_management\) if you have the admin role.

2.  \(Optional\) [Configuring data mapping](setting-up-wo-temp-copy-source-info-wo.md)

    Configure work templates to fetch fields from any table and add them to a work order form. The source table can be a case, incident, or a change made to the table.

3.  \(Optional\) [Configuring standalone task templates](setting-up-wotemp-create-stand-alone-tasks.md)

    Use template management enables you to create standalone work order task templates and links them to another work order template. This enables the work order templates to identify an appropriate task and create it for different work orders based on the filtering conditions.


