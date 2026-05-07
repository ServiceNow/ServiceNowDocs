---
title: Create a customer service case of a specific type
description: Customer service agents can create different types of cases by making selections from the case type selector.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage cases, Use, Customer Service Management]
---

# Create a customer service case of a specific type

Customer service agents can create different types of cases by making selections from the case type selector.

## Before you begin

Role required: sn\_customerservice\_agent

## About this task

The types of cases that agents can create depend on the configuration of the [customer service case types](../concept/customer-service-case-types.md) and [service definitions](../concept/csm-service-definitions.md) features. For more information, see the following topics:

-   [Configure customer service case types](configure-csm-case-types.md)
-   [Manage customer service case types](../concept/manage-csm-case-types.md)
-   [Configuring service definitions](../concept/csm-service-definitions-configure.md)

In CSM Configurable Workspace, agents use the [Case type selector](../concept/csm-case-type-select-modals.md) to make selections and create cases.

**Note:** In the Core UI, use the Case interceptor to make selections and create a case.

## Procedure

1.  Create a case by selecting one of the following actions.

    The case type selector appears by default with the options the agent has for creating a case in the context of the record.

    **Note:** The `sn_csm_case_types.enable_service_selector` property which enables the case type selector is set to true for zBoot customers, and can be enabled for upgrade customers.

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
-   Related lists: child case, case task
-   List view
-   Case task list view


</td></tr></tbody>
</table>2.  Make selections from the version of the case type selector that has been configured by the system administrator.

<table id="table_ulg_q1l_dwb"><thead><tr><th>

Version

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

Multi-select

</td><td>

1.  Select a **Case Type**.
2.  If desired, select an optional category and subtype to narrow the available choices.
3.  Select **Create Case**.
 **Note:** If a subtype hasn't been configured for a case type, the field for the subtype is not displayed.

</td></tr><tr><td>

Single-select

</td><td>

1.  Select a **Case Type**.
2.  Select **Create Case**.


</td></tr><tr><td>

Product Service Select

</td><td>

1.  Enable or disable the **This case is for an owned product** check box. This check box controls the display of the **Product** field
2.  If displayed, select a **Product**.
3.  Select a **Service**.
4.  Select a **Case type**.
5.  Select **Create Case**.


</td></tr></tbody>
</table>3.  Fill in the fields on the Case form.

    For more information about these fields, see [Create a customer service case](t_CreateACaseFromCustServApp.md).

4.  Select **Save**.


