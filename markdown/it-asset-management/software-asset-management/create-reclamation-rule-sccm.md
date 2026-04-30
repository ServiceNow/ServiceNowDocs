---
title: Create a reclamation rule to import Microsoft SCCM usage data
description: To import your Microsoft SCCM data, create a reclamation rule for the product that you want the usage information for.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Software Asset Management administration, Software Asset Management, IT Asset Management]
---

# Create a reclamation rule to import Microsoft SCCM usage data

To import your Microsoft SCCM data, create a reclamation rule for the product that you want the usage information for.

## Before you begin

Role required: sam\_admin

## About this task

A software product must have a product process, which consists of a filename, that is required for SCCM Usage to pull data. When adding a software product to a reclamation rule, any product processes associated with the software product are shown in the **Product Process** related list. Product processes are stored in the Software Product Process \[samp\_sw\_product\_process\] table.

If a product process doesn’t exist for a software product, you can create a custom one on the form. Product processes are stored in the Custom Product Process \[samp\_custom\_product\_process\] table.

Some software products may not include a product process, but new product processes are added twice every week through the content library updates.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Administration** &gt; **Reclamation Rules** and select **New**.

2.  On the Reclamation Rule form, create a new record \(see table for field descriptions\).

<table id="table_cpp_jm4_yjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the product for which you’re creating the reclamation rule.

</td></tr><tr><td>

Applies to

</td><td>

Type of software to which the reclamation rule applies.-   Installed Software
-   Engineering App License


</td></tr><tr><td>

Reclamation type

</td><td>

Type of data pulled from SCCM.-   Total Usage Time
-   Last Used Date


</td></tr><tr><td>

Notify user

</td><td>

Check box for notifying the user assigned to the software requesting permission via email to remove the software.

</td></tr></tbody>
</table>3.  If you selected **Total Usage Time** in the **Reclamation type** field, complete the fields in the Usage Metering Data section.

<table id="table_wxx_4m4_yjb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Aggregate usage by

</td><td>

Time period over which to aggregate usage information.-   Last Month
-   Last Two Months
-   Last Three Months
-   Last Six Months


</td></tr><tr><td>

Total hours used

</td><td>

Amount of time the software must be used to avoid being reclaimed.

</td></tr></tbody>
</table>4.  If you selected **Last Used Date** in the **Reclamation type** field, complete the fields in the Last Used Data section.

    |Field|Description|
    |-----|-----------|
    |Last used before|Amount of time a user can keep unused software before it’s reclaimed.|

5.  Select **Save**.

6.  On the Software Product related list, complete the following steps if a product doesn't exist for your reclamation rule.

    1.  Select **New**.

    2.  On the Custom Software Product form, [fill in the details](t_AddACustomProduct.md) to add the product information.

    3.  Select **Submit**.

    4.  On the Reclamation Rule form, select **Edit** in the Software Product related list.

7.  On the Software Product related list, select **Edit**.

8.  Select the product that you created with on the Custom Software Product form.

9.  Select **Save**.

10. Complete the following steps if the software product that you selected doesn't have a product process associated with it.

    1.  Select the link in the banner that displays on the Reclamation Rule form after you have applied the software product.

    2.  On the Custom Product Process form, fill in the details to add a process to the product.

        |Field|Description|
        |-----|-----------|
        |Product|Name of the product.|
        |File name|Name of the file associated with the product.|
        |Platform|Platform of the product.|

    3.  Select **Submit**


## Create a reclamation rule to import Microsoft SCCM usage data

Create a reclamation rule to pull in the total usage data for Microsoft Excel from Microsoft SCCM.

To begin creating a reclamation rule, add the following information to the Reclamation Rule form.

|Field|Description|
|-----|-----------|
|Name|Microsoft Excel|
|Applies to|Installed Software|
|Reclamation type|Total Usage Time|
|Usage Metering Data|
|Aggregate usage by|Last Month|
|Total hours used|20|

Select **Save**.

![Reclamation Rule form filled out with Microsoft Excel as the publisher.](../image/reclamation-rule-excel.png)

A software product exists for Microsoft Excel, so you must associate the product with the reclamation rule.

On the Software Product related list, select **Edit**.

On the Edit Members form, navigate to Excel in the Collection column and select Excel. Add it to the Software Product List column.

![Adding the Microsoft Excel product to the reclamation rule.](../image/reclamation-rule-add-product.gif)

Select **Save**.

![Reclamation Rule form with Excel added to the Software Product related list.](../image/reclaimation-rule-excel-product.png)

Two product processes are associated with Excel. Select the Product Process related list to view the product processes.

![Reclamation Rule form with two product processes added to the Product Process related list.](../image/reclaimation-rule-product-process-excel.png)

On the Reclamation Rule form, select **Save**.

## What to do next

The reclamation rule is added to the Reclamation Rules list and the data of the product gets imported from SCCM during the next monthly scheduled import.

**Parent Topic:**[Software Asset Management administration](../concept/c_SAMAdministration.md)

