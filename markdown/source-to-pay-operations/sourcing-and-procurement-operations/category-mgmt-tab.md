---
title: Category management tab
description: The Category management tab provides an overview of spend, savings, and pipeline projects, highlights savings opportunities, and enables creating pipeline projects directly from filtered lists.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Spend and Savings Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Category management tab

The Category management tab provides an overview of spend, savings, and pipeline projects, highlights savings opportunities, and enables creating pipeline projects directly from filtered lists.

To view the Category management tab in the Source-to-Pay Workspace, you must have the sn\_spend\_mgmt.sourcing\_category\_manager role and have the following applications installed:

-   Spend and Savings Management \(sn\_spend\_mgmt\)
-   Sourcing Pipeline Management \(sn\_spend\_pipeline\)

![Category management tab](../image/category-mgmt-tab.png "Category management tab")

## Components in the Category management tab

<table id="table_owl_24z_lxb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Global filters

</td></tr><tr><td>

Global filters

</td><td>

Filter

</td><td>

You can filter the data using the following filter types and sources:-   Date: Supports predefined ranges \(for example, Last 3 months, Last 6 months, Last month, Last year, This year, YTD\) and custom date ranges.
-   Category: Multi-select drop-down list populated from the Spend category table.
-   Supplier: Multi-select drop-down populated from the 'Supplier' table.

To apply a filter, select a filter type \(for example, Supplier\), and choose one or more filter values \(such as Adobe Systems or Apple, Inc.\), and then move the selected filter value from the Available list to the Applied list.

</td></tr><tr><td class="sub-head" colspan="3">

Overview

</td></tr><tr><td>

Total spend

</td><td>

Single Score with Line graph

</td><td>

Displays total spend from all settled invoices for the selected time period, along with a trend line showing spend progression over time.**Note:** The spend data covers only the last 750 days. You can run the `Populate line payments on invoice line` fix script and modify the period to retrieve spend data for their preferred date range.

</td></tr><tr><td>

Savings

</td><td>

Bar graph

</td><td>

Displays the savings amount \(planned, realized, active\) for all pipeline projects for the selected time period.**Note:** Displays the savings score based on the annualized data provided on the pipeline object. When calculating each pipeline project’s savings, the dashboard considers the overlap between the selected date-range filter and the project’s start and end dates.

</td></tr><tr><td>

Pipeline projects by type

</td><td>

Ring chart

</td><td>

Displays the pipeline projects by the following type for the selected time period:-   Supplier optimization
-   Contract optimization
-   Savings potential
-   Spend optimization
-   Risk reduction

</td></tr><tr><td class="sub-head" colspan="3">

Contracts

</td></tr><tr><td>

Expiring within 180 days

</td><td>

Single score

</td><td>

Contracts with end dates within the next 180 days.

</td></tr><tr><td>

Auto-renewing within 90 days

</td><td>

Single score

</td><td>

Contracts with auto-renew flag set to true and renewal due in 90 days.

</td></tr><tr><td>

Unconsolidated spend

</td><td>

Single score

</td><td>

Contracts with the same suppliers for different business owners or purchasing entity.

</td></tr><tr><td>

Contracts

</td><td>

List

</td><td>

All contracts for the selected category.When you create a pipeline project from the Contracts list by selecting **Pipeline project** &gt; **Create new** or **Add to existing**, the **Project type** field in the Create New Pipeline Project form is automatically populated with Contract Optimization. You can view the contract details in the Associated Records section.

**Note:** A contract record can be associated with only one active pipeline project record at a time.

</td></tr><tr><td class="sub-head" colspan="3">

Purchase order lines

</td></tr><tr><td>

Off-contract spend

</td><td>

Single score

</td><td>

POLs of POs where the contract field is null \(no linked contract\).

</td></tr><tr><td>

Non-preferred supplier spend

</td><td>

Single score

</td><td>

POLs of POs with suppliers where Preferred flag is set to **No**.

</td></tr><tr><td>

Spend fragmentation

</td><td>

Single score

</td><td>

Same product procured from different suppliers.

</td></tr><tr><td>

Purchase order lines

</td><td>

List

</td><td>

POLs in the selected category.When you create a pipeline project from the Purchase Orders list by selecting **Pipeline project** &gt; **Create new** or **Add to existing**, the **Project type** field in the Create New Pipeline Project form is automatically populated with Spend Optimization. You can view the purchase order details in the Associated Records section.

**Note:** A purchase order line record can be associated with only one active pipeline project record at a time.

</td></tr><tr><td class="sub-head" colspan="3">

Suppliers

</td></tr><tr><td>

Total suppliers in this category

</td><td>

Single score

</td><td>

Suppliers with performance score less than 95%.**Note:** The widgets in the Suppliers section vary based on whether Third-party Risk Management or Supplier Lifecycle Operations is installed.

</td></tr><tr><td>

Non-preferred suppliers

</td><td>

Single score

</td><td>

Suppliers where Preferred flag is set to **No**.

</td></tr><tr><td>

New Suppliers Added

</td><td>

Single score

</td><td>

New suppliers added in the selected time period.

</td></tr><tr><td>

Suppliers

</td><td>

List

</td><td>

List of active suppliers.When you create a pipeline project from the Suppliers list by selecting **Pipeline project** &gt; **Create new** or **Add to existing**, the **Project type** field in the Create New Pipeline Project form is automatically populated with Supplier Optimization. You can view the supplier details in the Associated Records section.

**Note:** A supplier record can be associated with only one active pipeline project record at a time.

</td></tr></tbody>
</table>**Parent Topic:**[Spend and Savings Management](spo-spend-mgmt.md)

