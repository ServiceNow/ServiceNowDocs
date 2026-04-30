---
title: Define a service catalog statement item
description: A business service can be represented by a service catalog category or a catalog item. When a service request from the service catalog is fulfilled, the price listed for the service in the service catalog item is captured as the cost of the statement item for a fiscal period.
locale: en-US
release: zurich
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 3
breadcrumb: [Determine the statement item type, Financial charging application setup - Legacy, Financial Charging - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Define a service catalog statement item

A business service can be represented by a service catalog category or a catalog item. When a service request from the service catalog is fulfilled, the price listed for the service in the service catalog item is captured as the cost of the statement item for a fiscal period.

## Before you begin

Role required: service\_charging\_analyst

**Important:**

This feature is available only when you own an ITBM Analyst license.

## Procedure

1.  Navigate to **All** &gt; **Financial Charging** &gt; **Administration** &gt; **Statement Items**.

2.  Click **New**.

3.  Click **Service Catalog Statement Item**.

4.  On the form, fill in the fields.

<table id="table_yql_3gn_tz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the service catalog statement item.

</td></tr><tr><td>

Business Service

</td><td>

Business service that uses the statement item as a configured item.You can [create a service](https://www.servicenow.com/docs/access?context=create-or-modify-SPM2-services&version=zurich&pubname=zurich-it-service-management&ft:locale=en-US).

</td></tr><tr><td>

Catalog

</td><td>

Catalog on which the statement item should be reported. Shows the list of catalogs in the system.

</td></tr><tr><td>

Category

</td><td>

Catalog items under the selected Category that are used for reporting the consumption details.

</td></tr><tr><td>

Catalog item

</td><td>

Catalog items under the selected Catalog and Category for which the consumption is reported.

</td></tr><tr><td>

Active

</td><td>

Check box to make the service catalog statement item active.

</td></tr><tr><td>

Fiscal Unit

</td><td>

Fiscal unit should be a month, quarter, or a period based on the fiscal calendar for which the statement item is generated.

</td></tr><tr><td>

Description

</td><td>

Short description of the statement item.

</td></tr></tbody>
</table><table id="table_lxt_zxh_fdc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Service owner

</td><td>

User who owns the business service and who views the service catalog statement items.A service owner can manage the showback items, view the unit cost, cost recovery based on consumption, and set unit price, discount, or surcharge to the showback item.

</td></tr><tr><td>

Pricing policy

</td><td>

Pricing policy can be for the statement item at any of the following levels:-   **Statement item level**: The adjusted price reflects at the statement item level.
-   **Statement item breakdown level**: The adjusted price reflects at the statement item breakdown level.
-   **Catalog item level**: The adjusted price reflects at the individual catalog item level in the expense lines.


</td></tr><tr><td>

Pricing policy method

</td><td>

Price adjustment based on a percentage of the average unit cost of the catalog item. Or, overriding the average unit cost by unit price pricing policy method.**Note:** If the pricing policy is at catalog item level, then you can opt for percentage-based pricing policy method.

</td></tr></tbody>
</table>5.  Click **Submit**.

6.  To generate charge lines for the service catalog statement item, click **Generate Charge Lines**.

    1.  To generate the charge lines, enter the fiscal period.

        **Note:**

        Charge lines for a service catalog statement item are generated based on the preconfigured Opened \(system property value is opened\_at\) date field in the Requested Items table. The dates of the requested items that fall within the fiscal period are considered for generating the charge lines. However, as a service charging analyst you can configure the system property \(com.snc.showback.catalog.consumed\_date\) value to a date field of your choice in the Requested Items \(sc\_req\_item\) table.

    2.  Click **OK**.

7.  To save the updated record, click **Update**.

8.  To delete a record, click **Delete**.


## What to do next

To [create breakdown records for the service catalog statement item](create-service-catalog-breakdowns.md), click **New** in the Service Catalog Breakdowns related list.

-   **[Create service catalog breakdowns](create-service-catalog-breakdowns.md)**  
Create service catalog breakdowns by fragmenting the service catalog category of the business service to its catalog item components into a more detailed level.

**Parent Topic:**[Determine the statement item type](determine-statement-item.md)

