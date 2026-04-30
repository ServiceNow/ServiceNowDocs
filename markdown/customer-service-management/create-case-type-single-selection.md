---
title: Create a configuration for case type single-select
description: Create a configuration for the single-select version of the case type selector and define the fields and values that the system uses to auto-populate the Case form.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring customer service case types, Customer service case types, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Create a configuration for case type single-select

Create a configuration for the single-select version of the case type selector and define the fields and values that the system uses to auto-populate the Case form.

## Before you begin

Role required: admin

## About this task

In CSM Configurable Workspace, there are three versions of the case type selector available to agents when creating cases of a specific type.

-   With the multi-select version, the agent selects a case type and optionally selects a category and subtype to narrow the available choices before creating a case. This is the default functionality.
-   With the single-select version, the agent selects a case type and creates a case. The system populates some of the fields on the Case form with values that have been predefined in the selection configuration.
-   With the Product Service Select version, the agent selects a product and a service to create a case. For more information, see [Product Service select version of the case type selector](../concept/csm-case-type-select-modals-product-service.md).

To use the single-select version, follow the procedure below to configure one or more selections that are available to agents when creating a case. You must also [enable the case type single select property](enable-case-type-single-select-prop.md).

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Case Types** &gt; **Manage Case Types**.

2.  Select a case type.

3.  In the Case Type Selections related list, click **New**.

4.  In the **Name** field, enter a descriptive name for the case type selection.

    This is the name that agents see in the **Case Type** field on the Select Case Type pop-up window.

5.  In the **Default case type field values** fields, select the desired fields and the corresponding values.

    The system uses this field and value configuration to auto-populate those fields on the Case form when an agent creates a case of this type.

6.  Click **Submit**.

    The system saves the configuration in the Service Definition \(sn\_case\_type\_selection\) table and adds it to the Case Type Selections related list.


