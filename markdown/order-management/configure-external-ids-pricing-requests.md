---
title: Configure context variables for external IDs
description: Set up a context variable for each external ID to be used in pricing requests and map the variable to a reference field in a ServiceNow reference table.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 1
breadcrumb: [External ID support in Sales CRM Pricing API, Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Configure context variables for external IDs

Set up a context variable for each external ID to be used in pricing requests and map the variable to a reference field in a ServiceNow reference table.

## Before you begin

Role required: admin

## About this task

The Sales CRM Pricing API supports external IDs in pricing requests. For each external ID, define a context variable that maps to the following:

-   Source reference table
-   Reference field name

For information on the pricing API, see Sales CRM Pricing API.

**Note:** Only a single reference field for an external ID is supported as a key to resolve an external ID with a sys\_id. To get an accurate and valid response, the external ID or code sent in a reference field must map to a unique record in the source reference table.

## Procedure

1.  Navigate to **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Set the application scope to Context Rule Management.

    Use the scope selection menu icon ![](../../../reuse/icons/product-icons/globe-outline-24.svg) in the header bar to select the scope.

3.  Select the List icon ![](../../../reuse/icons/product-icons/list-outline-24.svg).

4.  Navigate to **Context Rule Management** &gt; **Context Variables**.

5.  Do one of the following:

    -   If creating a context variable, select **New**.
    -   If updating a context variable, select the variable to be updated.
6.  Define or update the context variable for the external ID:

    1.  In the **Type** field, select Reference.

    2.  In the **Label** field, enter the name of the context variable to be displayed in the user interface.

        The **Column name** and **Code** fields are automatically generated based on the **Label name** entered. The default value for the **Type of mapping** field is set to Field mapping.

        **Note:** You can enter your own **Code** value to replace the system-generated code.

    3.  In the **Context type** field, select the context that indicates where the variable is retrieved from, for example the Transaction Header or Transaction Line for an opportunity or quote.

    4.  In the **Reference** field in the Reference Specification section, select the source reference table for the variable.

    5.  In the **Pricing api key field**, select the reference field to be used from the source reference table specified in Step d.

7.  Select **Save**.

    The external ID defined by the context variable can be used in pricing requests.


