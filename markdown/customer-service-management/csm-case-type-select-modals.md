---
title: Case type selector
description: The case type selector enables customer service agents to quickly and easily create the right kind of case for a contact or consumer by selecting from a list of available case types or services.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Customer service case types, Case management, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Case type selector

The case type selector enables customer service agents to quickly and easily create the right kind of case for a contact or consumer by selecting from a list of available case types or services.

## Overview

The case type selector is a component that provides agents with the ability to select the appropriate case type or service when creating a case. For example, an agent can use the case type selector to do the following:

-   Select a case type and create a case of that type.
-   Select a product from a list of products owned by the customer and create a case for that product.
-   Select a service and create a case for that specific service.

The selections that an agent can make is determined by the case type selector configuration. The system administrator can configure [different versions of the case type selector](csm-case-type-select-modals.md#section_h24_lf1_yxb) by setting [properties](csm-case-type-select-modals.md#section_p3t_k3f_svb). The different versions include:

-   Multi-select \(default\)
-   single-select
-   [Product Service select](csm-case-type-select-modals-product-service.md)

![Multi-select version of the case type selector with fields for selecting a category and case type](../image/case-type-multi-select.png "Case type selector (multi-select version)")

## Using the case type selector

The system displays the case type selector when an agent creates a case from a list or a record.

<table id="table_ulq_m3j_yxb"><thead><tr><th>

Agent action

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Select **New**

</td><td>

Select this action from case lists and case type lists such as My Cases or My Complaint Cases.

</td></tr><tr><td>

Select **Create Case**

</td><td>

Select this action from the following records:-   Interaction
-   Account
-   Contact
-   Consumer
-   Sold Product
-   Install Base Item
-   Case
-   Child Case

</td></tr></tbody>
</table>Some declarative actions available with the Customer Service Case Types plugin are disabled by default. For more information, see [Configure case type and case task type declarative actions](../task/config-case-type-declarative-action.md).

## Case type selector versions

Different versions of the case type selector are available for agents to use. The system administrator can configure system properties to determine the version of the case type selector that is presented to agents.

<table id="table_s2h_fff_svb"><thead><tr><th>

Version

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Multi-select

</td><td>

With the multi-select version, the agent selects a case type and optionally selects a category to narrow the available choices before creating a case.

 A category subtype field can also be configured. This field can be a choice list field or a reference field from the Case Type table.

**Note:** If a subtype has not been configured for a case type, the subtype field is not displayed.

 The multi-select version of the case type selector is the default functionality.

 For more information, see [Select a category and subtype for a case type](manage-csm-case-types.md#section_l3d_jr3_3kb).

</td></tr><tr><td>

Single-select

</td><td>

With the single-select version, the agent selects a case type from a list of available case types and creates a case with one click. The system uses configured field mapping to fill in some of the fields on the Case form.

 The display of the single-select version is controlled by the **sn\_csm\_case\_types.case\_type\_single\_field\_select** system property.

-   When enabled, the system displays the single-select version.
-   When disabled, the system displays the multi-select version.

**Note:** The single-select version is only available in CSM Configurable Workspace.

 For more information, see the following topics:

-   [Enable the case type single select property](../task/enable-case-type-single-select-prop.md)
-   [Create a configuration for case type single-select](../task/create-case-type-single-selection.md)

</td></tr><tr><td>

Product Service Select

</td><td>

With the Product Service Select version, the agent selects a product and/or a service to create a case. For more information, see [Product Service select version of the case type selector](csm-case-type-select-modals-product-service.md).

 The display of the Product Service Select version is controlled by the **sn\_csm\_case\_types.service\_definition\_select** system property.

-   When enabled, the system displays the Product Service Select version of the case type selector.
-   When disabled, the system uses the value of the **sn\_csm\_case\_types.case\_type\_single\_field\_select** property.

</td></tr></tbody>
</table>## Case type select properties

The following properties determine which version of the case type selector is presented to agents.

<table id="table_jlr_53f_svb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_csm\_case\_types.case\_type\_single\_field\_select

</td><td>

Set this property to true to enable the case type single select feature in CSM Configurable Workspace. When enabled, an agent can use this feature to create a case of a specific type with a single selection in the case type selector.-   **Type:** true \| false
-   **Default value:** false
-   **Location:** System Property \[sys\_properties\] table

</td></tr><tr><td>

sn\_csm\_case\_types.service\_definition\_select

</td><td>

Set this property to true to enable the Product Service Select version of the case type selector in CSM Configurable Workspace. When enabled, an agent can use this version to create a record based on the selected product or service.

-   **Type:** true \| false
-   **Default value:** true
-   **Location:** System Property \[sys\_properties\] table

 This property overrides the **sn\_csm\_case\_types.case\_type\_single\_field\_select** property.

-   When set to true, the system displays the Product Service Select version of the case type selector.
-   When set to false, the system uses the value of the **sn\_csm\_case\_types.case\_type\_single\_field\_select** property.
-   If both properties are set to true, the **sn\_csm\_case\_types.service\_definition\_select** property takes precedence.
-   If both properties are set to false, the system displays the multi-select version of the case type selector.

</td></tr><tr><td>

sn\_csm\_case\_types.service\_definition\_select\_count

</td><td>

Determines the number of the products and services displayed in the Product Service Select version of the case type selector.-   **Type:** integer
-   **Default value:** 25
-   **Location:** System Property \[sys\_properties\] table

</td></tr></tbody>
</table>## Configuring service definitions for cases and case tasks

The system administrator creates the [service definitions](csm-service-definitions.md) for cases and case tasks, along with their relationships. The service definition manager and service definition admin can also create these service definitions and relationships.

For case task service definitions, the system administrator can include logic and default field values that the system uses when creating the case tasks. For more information, see [Configuring service definitions](csm-service-definitions-configure.md).

