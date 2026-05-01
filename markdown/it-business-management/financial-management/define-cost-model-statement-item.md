---
title: Define a cost model statement item
description: The cost of the item or service is derived from the allocation lines of financial modeling application. The statement item captures the cost from the segment accounts, specific accounts in a segment, or buckets in an account, which gives you the cost of the statement item for a fiscal period.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-05-01"
reading_time_minutes: 3
breadcrumb: [Determine the statement item type, Financial charging application setup - Legacy, Financial Charging - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Define a cost model statement item

The cost of the item or service is derived from the allocation lines of financial modeling application. The statement item captures the cost from the segment accounts, specific accounts in a segment, or buckets in an account, which gives you the cost of the statement item for a fiscal period.

## Before you begin

Role required: service\_charging\_analyst

**Important:**

This feature is available only when you own an ITBM Analyst license.

## Procedure

1.  Navigate to **All** &gt; **Financial Charging** &gt; **Administration** &gt; **Statement Items**.

2.  Click **New** in the Statement Items list.

3.  Click **Cost Model Statement Item** link in the What type of Statement Item? query form.

4.  Fill in the form fields.

<table id="table_wb1_tgm_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the cost model statement item.

</td></tr><tr><td>

Cost model

</td><td>

The cost model used in the Financial Modeling application from which the cost data are retrieved for the statement item.

</td></tr><tr><td>

Unit cost metric

</td><td>

Calculates unit cost based on the weighted metric.

</td></tr><tr><td>

Segment

</td><td>

Segment for which cost is to be reported.

</td></tr><tr><td>

Active

</td><td>

Enable the check box to make the cost model statement item active.

</td></tr><tr><td>

Business service

</td><td>

Business service that uses the statement item as a configured item.You can also [define a service](https://www.servicenow.com/docs/access?context=create-or-modify-SPM2-services&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Fiscal unit

</td><td>

Defines the fiscal unit to be a month, quarter, or a period.Defaults based on the selected cost model.

</td></tr><tr><td>

Transactional table

</td><td>

Name of the transactional table that the segment refers to.Defaults based on the selected segment.

</td></tr><tr><td>

Description

</td><td>

Short description of the statement item.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Segment accounts filter|Filter conditions to report on the segment accounts that meet your conditions.|
    |Buckets Filter|Filter condition to the buckets that allocate expenses to the accounts in the segment.|

<table id="table_urp_dxh_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Sub Segment

</td><td>

Secondary segment for the segment you selected.Sub segments are segments under the selected segment in the cost model hierarchy.

</td></tr><tr><td>

Transactional table

</td><td>

Name of the transactional table that the sub segment refers to.Defaults based on the selected sub segment.

</td></tr><tr><td>

Sub Accounts Filter

</td><td>

Filter conditions to report on the segment accounts that meet your conditions.

</td></tr></tbody>
</table><table id="table_xly_dxh_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service owner

</td><td>

User who owns the service and who views the consumption statement items.As a service charging owner, you can manage the showback items. You can view the unit cost, cost recovery based on consumption, and set unit price, discount, or surcharge to the showback item.

</td></tr><tr><td>

Pricing policy

</td><td>

Pricing policy can be set for the statement item at any of the following levels:-   **Statement item level**: The price adjustment that you do in the console reflects at the statement item level.
-   **Statement item breakdown level**: Reflects the adjusted price at the statement item breakdown level.
-   **Account level**: The adjusted price is reflected at the account level in the expense lines.


</td></tr><tr><td>

Pricing policy method

</td><td>

Price adjustment based on a percentage of the average unit cost of the segment account. Or, overriding the average unit cost by unit price pricing policy method.**Note:** If the pricing policy is at account level, then you can opt for percentage based pricing policy method.

</td></tr></tbody>
</table>5.  Click **Submit**.

6.  To generate charge lines for the cost model statement item, click **Generate Charge Lines**.

    1.  To generate the charge lines, enter the fiscal period in the Generate charge lines dialog box.

    2.  Click **OK**.

        The statement lines generated for showback are extension of the expense lines.

7.  To save the updated record, click **Update**.

8.  To delete a record, click **Delete**.


## What to do next

To [create breakdown records for the cost model statement item](create-cost-model-breakdowns.md), click **New** in the Cost Model Breakdowns related list.

-   **[Create cost model breakdowns](create-cost-model-breakdowns.md)**  
Create breakdowns for the cost model statement item providing more clarity by reporting the components that constitute the cost model statement item and the cost associated with each of these components.

**Parent Topic:**[Determine the statement item type](determine-statement-item.md)

