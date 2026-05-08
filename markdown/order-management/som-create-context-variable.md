---
title: Create a custom context variable
description: Create custom context variables to represent product or non-product characteristics that can be used by pricing admins to apply different pricing features, such as pricing adjustments, or product catalog admins to set product offering eligibility rules.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
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

You create the variable name and define the variable type, so that the variable can be used in a decision rule for a rule matrix. After you create the variable, you must also [map the context variable to the transaction entity](som-map-variable.md), such as quote or order, from which the system retrieves the context.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

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

Context variable type. Choose the type of field for the variable. For example, the choice list field type lets your user select from a pre-defined list of choices.For more information on the different field types, see Field types reference.

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

System-generated alphanumeric number based on the label name. You can enter your own code to replace the system-generated code.

</td></tr><tr><td>

Context type

</td><td>

Option that indicates from where the context is retrieved. For example you could select one of the following types:-   Transaction Header: Context is fetched from the header record for a transaction, such as an opportunity, quote, or sales order.
-   Transaction Line: Context is fetched from the line record for an opportunity, quote, or sales order transaction.


</td></tr><tr><td>

Application

</td><td>

Name of the application scope. The default scope is Global.

</td></tr><tr><td>

Parameters

</td><td>

 

</td></tr><tr><td>

Pricing api key field

</td><td>

The reference field for a context variable that defines an external ID used in the Sales CRM Pricing API.

</td></tr><tr><td>

Active

</td><td>

Option that indicates the context variable is available for use in rule matrices.

</td></tr></tbody>
</table>5.  In the Reference Specification section, select the reference table for the context variable that defines an external ID used in the Sales CRM pricing API.

6.  Select **Save**.

    The tab \(related list\) for the **Type** that you selected in Step 4 and the **Variable Mapping** tab are displayed.

7.  Depending on the **Type** you selected, create the values for the type, then select **Save**.

    For example, in Step 4, if you selected the Choice type, select **New** in the **Choices** tab and define the choices.


## What to do next

[Map the custom context variable to a transaction entity](som-map-variable.md).

