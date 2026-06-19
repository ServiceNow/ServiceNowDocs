---
title: Create a custom context variable
description: Create custom context variables to represent product or non-product characteristics that can be used by pricing admins to apply different pricing features, such as pricing adjustments, or product catalog admins to set product offering eligibility rules.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/sales-and-order-management/som-create-context-variable.html
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Product pricing, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Create a custom context variable

Create custom context variables to represent product or non-product characteristics that can be used by pricing admins to apply different pricing features, such as pricing adjustments, or product catalog admins to set product offering eligibility rules.

## Before you begin

Before creating a custom variable, review the context variables available in the Context Variables \[sn\_csm\_ctxrul\_mgt\_context\_variable\] table to verify whether you need a new one. This table identifies the system-defined variables provided with Product Catalog Management and Pricing Management and also any custom variables that have been created.

For example, the system-defined context variables provided for non-product attributes include: Account, Shipping Country, Shipping City, Shipping State, Shipping Zip, Billing Country, Billing City, Billing State, Billing Zip, and Transaction Date.

Role required: admin

## About this task

As an administrator, you can create custom context variables for items such as non-product characteristics, that your pricing and product catalog administrators can use in rule matrices to control pricing features or product offering eligibility. For example, your pricing administrator might want to define pricing adjustments based on sales segment, but sales segment isn’t a system-defined context variable.

You create the variable name and define the variable type, so that the variable can be used in a decision rule for a rule matrix. After you create the variable, you must also [map the context variable to the transaction entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/som-map-variable.md), such as quote or order, from which the system retrieves the context.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** \[Omitted image "list-outline-24.svg"\] Alt text: view.

2.  Navigate to **Context Rule Management** &gt; **Context Variables**.

3.  In the Context Variables list, select **New**.

4.  On the form, fill in the fields.

<table id="table_fxl_wh5_g1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Type

</td><td>

Context variable type. Choose the type of field for the variable. For example, the choice list field type lets your user select from a predefined list of choices.For more information on the different field types, see .

**Note:** Depending on the **Type** selected, other fields and sections in the form are displayed.

</td></tr><tr><td>

Label

</td><td>

Name of the context variable to be displayed in the user interface, such as sales segment.

</td></tr><tr><td>

Column name

</td><td>

ID of the context variable for which the context variable type is created. The system assigns this name automatically based on the **Label** name entered, for example sales\_segment.

</td></tr><tr><td>

Code

</td><td>

System-generated alphanumeric number based on the label name. You can enter your own code to replace the system-generated code.**Note:** After the context variable is used in a published pricing or product eligibility matrix, the **Code** value can't be changed.

</td></tr><tr><td>

Context type

</td><td>

Option that indicates from where the context is retrieved. For example you can select a context type such as:-   Transaction Header: Context is fetched from the header record for a transaction, such as an opportunity, quote, or sales order.
-   Transaction Line: Context is fetched from the line record for an opportunity, quote, or sales order transaction.


</td></tr><tr><td>

Application

</td><td>

Name of the application scope. The default scope is Global.

</td></tr><tr><td>

System defined

</td><td>

Option indicating the context variable is defined by the pricing system.

</td></tr><tr><td>

Applicable to

</td><td>

Option indicating the module to which this context variable applies. Currently supports Pricing. The pricing engine uses this field to determine which context variables to resolve during pricing calculations.If the context variable is used in pricing, select Pricing. Otherwise, leave this field as **None**.

</td></tr><tr><td>

Type of mapping

</td><td>

Option indicating how the context variable is mapped:-   Field mapping: Map the context variable to a transaction entity.
-   Scripted: JavaScript that you provide in the **Script** field, which defines complex logic for computing values using the context variable. For example, a script might be used for the following:
    -   Calculations, such as discount percentages or account age
    -   Complex lookups, such as checks for accounts that have made purchases
    -   Business logic, such inventory check or eligibility
    -   Aggregrations across lines, for example, the number of products in a cart.


</td></tr><tr><td>

Pricing api key field

</td><td>

Reference field for a context variable that defines an external ID used in pricing requests in the Sales CRM Pricing API. For more information on external IDs and custom context variables, see [External ID support in Sales CRM Pricing API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/external-ids-pricingapi.md).

</td></tr><tr><td>

Active

</td><td>

Option that indicates the context variable is available for use in rule matrices.

</td></tr></tbody>
</table>5.  If you're using the external ID feature in the Sales CRM Pricing API, in the Reference Specification section, select the reference table for the context variable that defines an external ID to be used in a pricing request.

    For more information on external IDs and custom context variables, see [External ID support in Sales CRM Pricing API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/external-ids-pricingapi.md).

6.  Select **Save**.

    The tab \(related list\) for the **Type** that you selected in Step 4 and the **Variable Mapping** tab are displayed.

7.  Depending on the **Type** you selected, create the values for the type, then select **Save**.

    For example, in Step 4, if you selected the Choice type, select **New** in the **Choices** tab and define the choices.


## What to do next

For context variables that are mapped to fields, [map the custom context variable to a transaction entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/sales-and-order-management/som-map-variable.md).

