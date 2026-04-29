---
title: Enable the case type single select property
description: Enable the case type single select property so that customer service agents can use the case type single select version of the case type selector and create cases of a specific type with one click.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring customer service case types, Customer service case types, Case management, Organize agent workspaces, Configure, Customer Service Management]
---

# Enable the case type single select property

Enable the case type single select property so that customer service agents can use the case type single select version of the case type selector and create cases of a specific type with one click.

## Before you begin

Role required: admin

## About this task

In CSM Configurable Workspace, there are three versions of the case type selector available to agents when creating cases of a specific type.

-   With the multi-select version, the agent selects a case type and optionally selects a category and subtype to narrow the available choices before creating a case. This is the default functionality.
-   With the single-select version, the agent selects a case type and creates a case. The system populates some of the fields on the Case form with values that have been predefined in the selection configuration.
-   With the Product Service Select version, the agent selects a product and a service to create a case. For more information, see [Product Service select version of the case type selector](../concept/csm-case-type-select-modals-product-service.md).

To use the single-select version, enable the **sn\_csm\_case\_types.case\_type\_single\_field\_select** property. You must also [create a configuration](create-case-type-single-selection.md).

## Procedure

1.  Navigate to **sys\_properties.list**.

2.  Click the **sn\_csm\_case\_types.case\_type\_single\_field\_select** property in the **Name** field.

3.  Set the **Value** to true.

4.  Click **Update**.


