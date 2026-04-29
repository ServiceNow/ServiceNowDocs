---
title: Create product characteristics and characteristic options
description: Add product characteristics and characteristic options that you can later add to your product offerings in Sales and Order Management.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Defining product characteristics and characteristic options, Create product offerings, Configuring product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales and Order Management]
---

# Create product characteristics and characteristic options

Add product characteristics and characteristic options that you can later add to your product offerings in Sales and Order Management.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_admin or sn\_prd\_pm.product\_catalog\_manager

## About this task

Use this procedure to build product characteristics \(also called attributes\) and characteristic options, which you add to product offerings and specifications. For example, if the product offering is a bike, characteristics might include bike size and color. The characteristic options are the option choices, such as the various bike sizes and colors available. These options appear in the configurator when your agents add configurable products to opportunities, quotes, and orders or when customers submit orders using the Business Portal.

When you define a characteristic, you select the data input type, which indicates how the characteristic option is entered in the product configurator, such as Single Line Text, Choice \(radio buttons or drop-down list\), and Yes/No selections. Complex data input types are also available to define complex characteristics that have hierarchical attribute structures. You use the object data type to define complex characteristics, which have a top-level parent attribute and associated child characteristics. These structures can also include data arrays, another complex data type that you can use to specify multiple instances of the same data input type, such as multiple lines of text or integers.

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

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

System-generated alphanumeric value based on the product characteristic name. Although system generated, you can edit the code to represent a SKU or any other industry specific product codes.**Note:** If you enter a product characteristic name that has non-English characters, special symbols, or both, the **Code** value may be a hash of alphanumeric characters that uniquely identifies the characteristic, if your admin has set the **sn\_prd\_pm.use\_hash\_to\_generate\_characteristic\_code** system property to false. If this property is set to true, the system can't generate an alphanumeric **Code** value that includes non-English characters, special symbols, or both.

</td></tr><tr><td>

Description

</td><td>

Brief description of the characteristic, for example DSL speed.

</td></tr><tr><td>

Input type

</td><td>

List of input options that identify the functionality for the characteristic, such as check box or a line of text. Depending on the input type, additional options become available:-   **Address**: Input for the entry of an address.
-   **Attachment**: Input for the attachment of an external document.
-   **CheckBox**: Option that can be selected or cleared. You can specify a **Default value** to be displayed for the option.
-   **Choice**: Options that can be chosen for the characteristic. In the Characteristic options tab, you indicate how the option is to be selected in the product configurator, either as a Radio button or from a Drop-down list. You can also specify a **Default value** to be displayed for the option.
-   **Date**: Date picker for selecting the day, month, and year, for example an activation date.
-   **Date/Time**: Date picker for selecting the day, month, year, and time of day for example, an activation date at a specific hour, minutes, and seconds.
-   **Duration**: Input for the entry of a duration of time.
-   **Email**: Input for the entry of an email address.
-   **Label**: Input for the selection that enables the production of a label.
-   **Single Line Text**: Input for the free-form entry of a single line of text. You can specify a **Default value** to be displayed for the option.
-   **Yes/No**: Input that requires the selection of a Yes/No response. You can specify a **Default value** to be displayed for the option.
-   **Integer**: Input that requires a numeric value, such as number of support hours. You can specify a **Default value** to be displayed for the option.
-   **Decimal**: Input for numbers that require a decimal point, such as currency or car mileage that require fractions.
-   **Object**: Input for defining the top-level characteristic in a hierarchy of characteristics that consists of a parent characteristic and its child characteristics. A top-level characteristic has one or more child characteristics. The child characteristics can be any of the data input types or an object or array type. The Characteristic Relationship tab opens for specifying the associated characteristic options.
-   **Array.Date**: Input that includes one or more instances of dates as child characteristics. You specify a Min and Max value for the array size. The default Min and Max value is 1.
-   **Array.Datetime**: Input that includes one or more instances of child characteristic of datetime. You also specify a Min and Max value for the array size. You specify a Min and Max value for the array size. The default Min and Max value is 1.
-   **Array.Decimal**: Input that includes one or more instances of a child characteristic of decimals. You specify a Min and Max value for the array size. The default Min and Max value is 1.
-   **Array.Integer**: Input that includes one or more instances of a child characteristic of the integer data type. You specify a Min and Max value for the array size. The default Min and Max value is 1.
-   **Array.Object**: Input that includes one or more instances of a child characteristic of the object data type. You specify a Min and Max value for the array size. The default Min and Max value is 1.
-   **Array.SingleLineText**: Input that includes one or more instances of a child characteristic of the SingleLineTest data type. You specify a Min and Max value for the array. The default Min and Max value is 1.


</td></tr></tbody>
</table>5.  Select **Save**.

    Depending on the **Input type** you selected, you may need to complete additional steps if the new characteristic has more options.

6.  If the new characteristic has more options, complete the following steps:

    1.  In the Characteristic Options tab, select **New**.

    2.  Enter the Option for the characteristic and select **Save**.

        The option is added to the characteristic. Repeat this step to add as many options as needed.

        For example, if you create a SIM card type characteristic, you then create the associated Nano, eSim, Micro, Mini, and Standard options.

        Later, when you are configuring product offerings, you can add the characteristics and options.

    3.  Select **Save**.

7.  If the new characteristic is an object that has child characteristics as part of hierarchical attribute structure, complete the following steps to create a characteristic relationship between the parent characteristic and child characteristics in the characteristic hierarchy:

    1.  In the Characteristic Relationships tab, select **New**.

    2.  In the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Display name|The name of the characteristic relationship, for example Routing addresses|
        |Parent characteristic|The parent-level characteristic in the characteristic hierarchy.|
        |Mandatory|Option that indicates the characteristic is required and must be entered or selected in the product configurator.|
        |Order|The position of this child characteristic in the attribute hierarchy.|
        |Child characteristic|Characteristic that is a child of the parent characteristic displayed. Select the characteristic from the drop-down list.|

        **Note:** A parent-level characteristic \(object input type\) must have at least one child characteristic relationship defined for the hierarchical structure.

    3.  Select **Save**.


## What to do next

Continue working on other areas related to the product offering or specification. For example:

-   [Add product visuals](som-product-config-add-visuals.md)
-   [Add product catalog categories](som-product-config-offering-categories.md)
-   [Create product offering relationships](som-product-config-offering-relationships.md)
-   [Add related contracts to product offerings](som-product-config-related-contracts.md)
-   [Add a unit of measure to a product offering](som-product-config-add-unit-of-measure.md)
-   [Create a product offering version](som-product-config-create-new-version.md)
-   [Create product offering relationship groups](som-product-config-relationship-groups.md)
-   If you're creating technical products such as telecommunications products, you can create the product, service, and resource specification categories and associate them to model categories.

