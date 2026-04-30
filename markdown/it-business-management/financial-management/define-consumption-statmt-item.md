---
title: Define a consumption statement item
description: If your cost and business service usage details are sourced from an external consumption table, then you can source the consumption details of the consumption table for the statement item.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Determine the statement item type, Financial charging application setup - Legacy, Financial Charging - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Define a consumption statement item

If your cost and business service usage details are sourced from an external consumption table, then you can source the consumption details of the consumption table for the statement item.

## Before you begin

Role required: service\_charging\_analyst

**Important:**

This feature is available only when you own an ITBM Analyst license.

## About this task

Business service consumption details can come from a table belonging to one or other platform applications or from an external consumption table, in which case the consumption details can be loaded on to the platform table. The consumption table gives you the daily or monthly consumption details of a business service. Based on the usage, the cost of the service is computed using the unit cost and quantity consumed for a fiscal period.

For example, the monthly utility bill for household power consumption has details of the appliances that you run and the power consumed in Watts, calculated monthly and annually. Based on the unit price and the consumption quantity, the bill amount is generated.

## Procedure

1.  Navigate to **All** &gt; **Financial Charging** &gt; **Administration** &gt; **Statement Items**.

2.  In the Statement Items list, click **New**.

3.  In the What type of Statement Item? query form, click the **Consumption Statement Item** link.

4.  On the form, fill in the fields.

<table id="table_jgm_v32_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the consumption statement item.

</td></tr><tr><td>

Consumption table

</td><td>

Source table that has the consumption data, which is configured as the statement item.

</td></tr><tr><td>

Consumption item

</td><td>

The item for which the consumption data is held in the consumption table.

</td></tr><tr><td>

Consumed date

</td><td>

The column in the consumption table that has the consumed date details.

</td></tr><tr><td>

Active

</td><td>

Check box to make the statement item active.

</td></tr><tr><td>

Business Service

</td><td>

Business service that uses the statement item as a configured item.You can also [define a service](https://www.servicenow.com/docs/access?context=create-or-modify-SPM2-services&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Fiscal unit

</td><td>

Fiscal unit should be a month, quarter, or a period based on the fiscal calendar for which the consumption data is generated.

</td></tr><tr><td>

Aggregate

</td><td>

Consumption table is queried based on the aggregate function you select.

</td></tr><tr><td>

Description

</td><td>

Short description of the statement item.

</td></tr><tr><td>

Consumption table filter

</td><td>

Filter to display the items that meet your conditions.

</td></tr></tbody>
</table><table id="table_v23_gwh_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Price basis

</td><td>

Select the criterion to determine the price.-   Amount retrieves the data from the selected **Amount** field of the consumption table.
-   Ratecard class is based on the pricing policy that is set for the statement item.
-   Unit price is the cost per unit of the item.


</td></tr><tr><td>

Amount field

</td><td>

Amount data is taken from the selected field if the **Price basis** is amount.

</td></tr><tr><td>

Ratecard class

</td><td>

Rate card class.

</td></tr><tr><td>

Consumption table ratecard mapping field

</td><td>

Amount is derived based on the consumption table ratecard mapped field and the rate card item mapping field, if you select **Ratecard class** in the **Price basis** field.

</td></tr><tr><td>

Rate Card Item mapping field

</td><td>

Amount is derived based on the rate card item mapping field and consumption table ratecard mapping field, if you select **Ratecard class** in the **Price basis** field.

</td></tr></tbody>
</table><table id="table_sbs_3wh_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service owner

</td><td>

User who owns the business service and views the consumption statement items.As a service owner, you can manage the showback items. You can view the unit cost, cost recovery based on consumption, and set unit price, discount, or surcharge to the showback item.

</td></tr><tr><td>

Pricing policy

</td><td>

Set the pricing policy for the statement item at the statement item level, statement item breakdown level, or at the item level.If you set the pricing policy at the statement item level, the price adjustment that you do as a service owner reflects the adjusted price at the statement item level. Similarly, for the statement item breakdown and the item levels, the price adjustment is reflected at the respective levels.

</td></tr><tr><td>

Pricing policy method

</td><td>

Set the price adjustment based on a percentage of the average unit cost of the catalog item. Or, override the average unit cost by setting a price per unit for the item.**Note:** If the pricing policy is at the item level, then you can opt for the percentage-based pricing policy method.

</td></tr></tbody>
</table>5.  Click **Submit**.

6.  To generate the charge lines for the consumption statement item, click **Generate Charge Lines** t.

    1.  To generate the charge lines, enter the fiscal period in the Generate charge lines dialog box.

    2.  Click **OK**.

7.  To save the updated record, click **Update**.

8.  To delete a record, click **Delete**.


## What to do next

To [create breakdown records for the consumption statement item](create-consumption-breakdowns.md), click **New** in the Consumption Breakdowns related list.

-   **[Create consumption breakdowns](create-consumption-breakdowns.md)**  
Create consumption breakdown records to make your showback report more detailed by reporting the expense line accounts that comprise the consumption statement item.

**Parent Topic:**[Determine the statement item type](determine-statement-item.md)

