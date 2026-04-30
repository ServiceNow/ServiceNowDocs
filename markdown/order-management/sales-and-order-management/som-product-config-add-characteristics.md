---
title: Create product characteristics and characteristic options
description: Add product characteristics and characteristic options that you can later add to your product offering in Sales Customer Relationship Management.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Create product offerings, Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Create product characteristics and characteristic options

Add product characteristics and characteristic options that you can later add to your product offering in Sales Customer Relationship Management.

## Before you begin

Role required: sn\_prd\_pm\_product\_catalog\_admin and sn\_prd\_pm\_product\_catalog\_manager

## About this task

Use this procedure to build product characteristics and characteristic options, which you add to product offerings. For example, If the product offering is a bike, characteristics might include bike size and color, and the characteristic options are the option choices, such as the various bike sizes and colors available. The options appear in the product configurator as agents are creating orders or building quotes.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Characteristics** &gt; **Characteristics**.

3.  Select **New**.

4.  In the form, fill in the fields.

<table id="table_otz_zqz_m1c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the product characteristic.

</td></tr><tr><td>

Code

</td><td>

System-generated alphanumeric number based on the product characteristic name. Although system generated, you can edit the code to represent a SKU or any other industry specific product codes.

</td></tr><tr><td>

Description

</td><td>

Brief description of the characteristic, for example DSL speed.

</td></tr><tr><td>

Input type

</td><td>

List of input options that identify the functionality for the characteristic. Depending on the input type, additional options become available:-   **Address**: Input for the entry of an address
-   **Attachment**: Input for the attachment of an external document.
-   **CheckBox**: Option that you select or clear.
-   **Choice**: Options that you choose for the characteristic. If you select **Choice**, you can define options for the characteristic in the Characteristic Options tab.
-   **Date/time**: Input for the entry of a date and time of day.
-   **Duration**: Input for the entry of a duration of time.
-   **Email**: Input for the entry of an email address.
-   **Label**: Input for the selection that enables the production of a label.
-   **Single Line Text**: Input for the free-form entry of a single line of text.
-   **Yes/No**: Input that requires the selection of a Yes/No response.


</td></tr></tbody>
</table>5.  Select **Save**.

    Depending on the **Input type** you selected, you may need to complete additional steps if the new characteristic has more options.

6.  If the new characteristic has more options, complete the following steps:

    1.  In the Characteristic Options tab, select **New**.

    2.  Enter the Option for the characteristic and select **Save**.

        The option is added to the characteristic. Repeat this step to add as many options as needed. Later, when you are configuring product offerings, you can add the characteristics and options.


## What to do next

-   [Add product visuals](som-product-config-add-visuals.md)
-   [Add product catalog categories](som-product-config-offering-categories.md)
-   [Create product offering relationships](som-product-config-offering-relationships.md)
-   [Add related contracts to product offerings](som-product-config-related-contracts.md)
-   [Add a unit of measure to a product offering](som-product-config-add-unit-of-measure.md)
-   [Create a product offering version](som-product-config-create-new-version.md)
-   [Create product offering relationship groups](som-product-config-relationship-groups.md)
-   If you're creating telecommunications products, create the product, service, and resource specification categories and associate them with model categories.

