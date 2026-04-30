---
title: Procurement Strategy &amp; Ops Dashboard
description: Visually analyze how your organization is placed strategically and operationally, over a given period of time.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Performance Analytics for Sourcing and Procurement Operations, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Procurement Strategy &amp; Ops Dashboard

Visually analyze how your organization is placed strategically and operationally, over a given period of time.

**Note:** This dashboard is available only if you install the Performance Analytics for Sourcing and Procurement Operations application.

You can use the Procurement Strategy &amp; Ops Dashboard to view your organization's strategic performance, which includes year-to-date total spend, spend categorization, total savings, negotiation outcomes, spend by category and supplier, and utilization of active blanket purchase orders. On the operations side, you can view your organization's open sourcing requests, negotiations, expiring contracts, and purchase requisitions and their details. You can filter by cost center or department and select specific elements to view relevant details.

On the SLA side, you can view the basic cycle times for different record types, time taken for each state, comparison of breached versus unbreached records, breached time in comparison with standard SLA time, and team performance in terms of processing records and also the excess time taken for breached records. You can filter the records by task type.

**Note:** The widgets plot metrics or data from the day the upgrade is taken, as the triggers for collecting metrics are enabled only after the upgrade. So, historical data isn’t available automatically after the upgrade but is accumulated thereafter. Also, if any new case types are introduced in the system and you want to add its metrics to the SLA dashboard, ensure that you update the indicator source.

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Procurement Specialist Manager: View your organization's strategic and operational performance. You can view your organization's SLA-related details. This role has the same access as a procurement specialist, except that they have access to the manager dashboards.|sn\_shop.procurement\_specialist\_manager|
|Procurement Administrator: View and make configuration changes to the widgets.|sn\_shop.procurement\_administrator|

## Indicators

-   Number of Expiring Contracts
-   Number of Open Negotiations
-   Number of Open Purchase Requisition
-   Number of Open Sourcing Request
-   Number of Total \(ATF\) Purchase Requisition
-   Order Line Revisioned Line Amount
-   Order Line Total Line Amount\(History Line\)
-   PSM - Average cycle time for record types
-   PSM - Average cycle time in each state for record types
-   PSM - Breached SLA by record type
-   PSM - Number of closed record types
-   PSM - Procurement Team Performance.Count
-   PSM - ProcurementSLA.duration of records
-   PSM - ProcurementSLA.standard time
-   Purchase Order - Total Line Amount
-   \(ATF\) Purchase Line - Total Line Amount

## Breakdowns

-   Cost center
-   Department
-   Negotiation - AssignedTo
-   ProcurementSLA - HasBreached
-   ProcurementUsers - AssignedTo
-   Product Category
-   PurchaseRequisition - AssignedTo
-   PurchaseTask - AssignedTo
-   SourcingRequest - AssignedTo
-   State
-   Supplier
-   Task type
-   \(PSM\) Contract End Date Breakdown
-   \(PSM\) Due Date Breakdown

## Reports

The Procurement Strategy &amp; Ops Dashboard is segregated into the following tabs:

-   **Strategic**: View your organization's strategic performance, which includes year-to-date total spend, spend categorization, total savings, negotiation outcomes, spend by category and supplier, and utilization of active blanket purchase orders.
-   **Operations**: View your organization's open sourcing requests, negotiations, expiring contracts, and purchase requisitions and their details.
-   **SLA**: View your organization's average time to complete records, breached SLA by record type, and a comparison between average time and SLA time of breached records.

**Note:** By default, YTD is configured to start from January. However, this can be configured to start from any month if need be.

For a detailed analysis on each component, select the respective widget or chart.

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

Strategic

</td></tr><tr><td>

Total Spend - YTD

</td><td>

Widget

</td><td>

View the total year-to-date amount across the organization for all standard purchase orders, excluding blanket and closed canceled purchase orders. Only standard purchase orders and purchase order releases are considered.

</td></tr><tr><td>

Spend Categorization - YTD

</td><td>

Pie chart

</td><td>

View the breakdown of the total year-to-date spend across the organization by addressable and non-addressable categories.

 The total spend is the sum of the total line amount on the purchase order line, excluding blanket purchase orders, where the state of the purchase order isn’t closed canceled, and the spend categorization is either addressable or non-addressable.

</td></tr><tr><td>

Total Savings - YTD

</td><td>

Widget

</td><td>

View the year-to-date sum of the negotiated savings across the organization for all standard purchase orders, excluding blanket and closed canceled purchase orders. Only standard purchase orders and purchase order releases are considered.

</td></tr><tr><td>

Negotiation Outcomes - YTD

</td><td>

Stacked bar chart

</td><td>

View the year-to-date negotiation outcomes across the organization against the negotiation count, grouped by negotiation type.

 Some of the possible negotiation outcomes are contract renewal, quote, RFx, and so on. Negotiation types can be cost avoidance, standard savings, contract terms negotiations, or unsuccessful negotiations.

 This report shows negotiation outcomes where the corresponding negotiation state is either Closed Complete or Closed Canceled.

</td></tr><tr><td>

Spend by Category - YTD

</td><td>

List

</td><td>

View the year-to-date committed spend, that is purchase order created, across the organization, grouped by the category associated to the supplier product on the purchase order line.

</td></tr><tr><td>

Total Spend by Supplier - YTD

</td><td>

List

</td><td>

View the total year-to-date amount across the organization for all standard purchase orders, excluding blanket and closed canceled purchase orders, grouped by supplier. Only standard purchase orders and purchase order releases are considered.

</td></tr><tr><td>

Utilization of Active Blanket Purchase Orders

</td><td>

List

</td><td>

View the released or subtotal percentage of the active blanket purchase orders across the organization that are within the end date.

</td></tr><tr><td class="sub-head" colspan="3">

Operations

</td></tr><tr><td>

Open Sourcing Requests

</td><td>

Widget

</td><td>

View the total number of sourcing requests across the organization that aren’t in a closed state.

</td></tr><tr><td>

Open Negotiations

</td><td>

Widget

</td><td>

View the total number of negotiations across the organization that aren’t in a closed state.

</td></tr><tr><td>

Expiring Contracts

</td><td>

Widget

</td><td>

View the total number of contracts, associated to purchase requisitions in any state, across the organization, that has an end date of 90 days out.

</td></tr><tr><td>

Open Sourcing Requests by Due Date

</td><td>

Pie chart

</td><td>

View the breakdown of the count of open sourcing requests across the organization by due date range.

</td></tr><tr><td>

Open Negotiations by Due Date

</td><td>

Pie chart

</td><td>

View the breakdown of the count of open negotiations across the organization by due date range.

</td></tr><tr><td>

Expiring Contracts by End Date

</td><td>

Pie chart

</td><td>

View the breakdown of the count of expiring contracts across the organization by end date range.

</td></tr><tr><td>

Open Purchase Requisitions

</td><td>

Widget

</td><td>

View the total number of purchase requisitions across the organization that aren’t in a closed state.

</td></tr><tr><td>

Aging Purchase Requisitions

</td><td>

Stacked bar chart

</td><td>

View the breakdown of the count of purchase requisitions across the organization by age \(that is the number of days since opened\) and state.

</td></tr><tr><td>

After-the-Fact \(ATF\) Purchase Requisitions

</td><td>

Bar with line

</td><td>

View the count and $ value of After-the-Fact \(ATF\) purchase requisitions.$ value is the value of purchase lines that satisfy the ATF criteria. For example, if there’s one ATF purchase requisition with two lines \(purchase requisition line 1 is ATF with line amount $10, and purchase requisition line 2 isn’t ATF with line amount $5\), the count of ATF purchase requisitions is 1 and the $ value is $10.

Revised ATF purchase requisitions and their values aren’t considered.

</td></tr><tr><td class="sub-head" colspan="3">

SLA

</td></tr><tr><td>

Average time to complete record

</td><td>

Bar with line

</td><td>

View the average cycle time and count for record types such as sourcing request, purchase requisition, negotiation, and cases. While the count is shown on the Y-axis and is represented by the bar, the line represents the time.Fact data for this widget is derived from database views created from metric definitions that track psm\_unique\_state and active fields of PSM record types.

</td></tr><tr><td>

Average time to complete by state

</td><td>

Stacked bar chart

</td><td>

View the breakup of the time taken in each state of the record.For example, if a sourcing request took three days to complete, then the time taken in each state of the sourcing request like pending review, requires decision, awaiting response, and so on, is displayed here.

This widget should be read in conjunction with the previous widget to get an understanding of the average time, and the breakup of this average time into various states.

Data for this widget is derived from database views created from metric definitions that track psm\_unique\_state and active fields of PSM record types.

</td></tr><tr><td>

Breached SLA by record type

</td><td>

Stacked bar chart

</td><td>

View a comparison between the records that were processed within the SLA time versus those that weren't. This gives an idea of the percentage work done that is within the SLA and the percentage that is breaching it.For example, if 100 records were processed in a week and 70 records were processed within the SLA time, then 70% of the work is done within the SLA and 30% is breaching it.

Data for this widget is derived from the Task SLA table that is fed by SLA definitions created on the active fields of PSM record types.

</td></tr><tr><td>

Average time vs SLA time of breached records

</td><td>

Time series column

</td><td>

View the actual time taken versus the allotted SLA time. This gives an understanding of the extra time that is taken when compared to the SLA time.Data for this widget is derived from the Task SLA table that is fed by SLA definitions created on the active fields of PSM record types.

</td></tr><tr><td>

Employee performance by record type

</td><td>

Stacked bar chart

</td><td>

View the count of records of types sourcing request, purchase requisition, negotiation, and cases that have been processed by your team.Data for this widget is derived from database views created from metric definitions that track active fields of PSM record types.

</td></tr><tr><td>

Employee performance breaches in durations

</td><td>

Stacked bar chart

</td><td>

View the time taken for the breached records of the team.The Procurement Specialist Manager can not only see the time taken for the breached records, but can also drill down to get the exact duration and the SLA time to get the details of time exceeded by SLA.

Data for this widget is derived from the Task SLA table that is fed by SLA definitions created on the active fields of PSM record types.

</td></tr></tbody>
</table>For information on how to work with dashboards in configurable workspaces, see [Dashboards in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

For information on how to work with widgets and data visualizations in configurable workspaces, see [Data visualizations in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-data-visualizations&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Performance Analytics for Sourcing and Procurement Operations](performance-analytics-for-spo.md)

