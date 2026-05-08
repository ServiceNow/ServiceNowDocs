---
title: Procurement Buyer Dashboard
description: Visually analyze how you’re placed with your work and achievements over a given period of time.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Preconfigured metrics and dashboards, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Procurement Buyer Dashboard

Visually analyze how you’re placed with your work and achievements over a given period of time.

**Note:** This dashboard is available only if you install the Performance Analytics for Sourcing and Procurement Operations application.

You can use the Procurement Buyer Dashboard to view all your open sourcing requests, negotiations, purchasing tasks, purchase requisitions, and expiring contracts, in widgets that distinguish these by due dates. You can also view your achievements, which include your year-to-date total spend, further broken down by spend categorization, total savings, negotiation outcomes, and the average cycle time of your assigned sourcing requests and purchase requisitions.

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Procurement Specialist: View your work and achievements.|sn\_shop.procurement\_specialist|
|Procurement Specialist Manager: View your work and achievements. This role contains the specialist role, and hence has access to the buyer dashboard.|sn\_shop.procurement\_specialist\_manager|
|Procurement Administrator: View and make configuration changes to the widgets.|sn\_shop.procurement\_administrator|

## Indicators

-   Number of Open Purchasing Task
-   Number of Open Purchase Requisition
-   Number of Closed Purchase Requisitions - Monthly
-   Purchase Requisition - Avg Cycle Time \(Days\) - Monthly
-   Number of Closed Sourcing Requests - Monthly
-   Number of Open Sourcing Request
-   Number of Open Negotiations
-   Sourcing Request - Avg Cycle Time \(Days\) - Monthly
-   Number of Expiring Contracts

## Breakdowns

-   Cost center
-   Department
-   Negotiation - AssignedTo
-   PurchaseRequisition - AssignedTo
-   PurchaseTask - AssignedTo
-   SourcingRequest - AssignedTo
-   \(PSM\) Contract End Date Breakdown
-   \(PSM\) Due Date Breakdown

## Reports

The Procurement Buyer Dashboard is segregated into the following tabs:

-   **My Work**: View all your open sourcing requests, negotiations, purchasing tasks, purchase requisitions, and expiring contracts.
-   **My Achievements**: View your achievements, which include your year-to-date total spend, spend categorization, total savings, negotiation outcomes, and average cycle times for sourcing request and purchase requisition.

**Note:** All the reports pertain to tasks that the logged-in user is assigned to.

For a detailed analysis on each component, select the respective widget or chart.

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="3">

My Work

</td></tr><tr><td>

My Open Sourcing Requests

</td><td>

Widget

</td><td>

View your total number of sourcing requests that aren’t in a closed state.

</td></tr><tr><td>

My Open Negotiations

</td><td>

Widget

</td><td>

View your total number of negotiations that aren’t in a closed state.

</td></tr><tr><td>

My Expiring Contracts

</td><td>

Widget

</td><td>

View your total number of contracts, associated to purchase requisitions in any state, that have an end date of 90 days out.

</td></tr><tr><td>

My Open Sourcing Requests by Due Date

</td><td>

Pie chart

</td><td>

View the breakdown of the count of your open sourcing requests by due date range.

</td></tr><tr><td>

My Open Negotiations by Due Date

</td><td>

Pie chart

</td><td>

View the breakdown of the count of your open negotiations by due date range.

</td></tr><tr><td>

My Expiring Contracts by Due Date

</td><td>

Pie chart

</td><td>

View the breakdown of the count of your expiring contracts by end date range.

</td></tr><tr><td>

My Open Purchasing Tasks

</td><td>

Widget

</td><td>

View your total number of purchasing tasks that aren’t in a closed state.

</td></tr><tr><td>

My Open Purchasing Tasks by Due Date

</td><td>

Pie chart

</td><td>

View the breakdown of the count of your open purchasing tasks by due date range.

</td></tr><tr><td>

All Open Task Types

</td><td>

Stacked bar chart

</td><td>

View the count of the open purchasing tasks that aren’t assigned to the logged-in user, by task type and due date range. The parent purchase requisition however is assigned to the logged-in user.

</td></tr><tr><td>

My Open Purchase Requisitions

</td><td>

Widget

</td><td>

View your total number of purchase requisitions that aren’t in a closed state.

</td></tr><tr><td>

My Aging Purchase Requisitions

</td><td>

Stacked bar chart

</td><td>

View the breakdown of the count of your purchase requisitions by age \(that is the number of days since opened\) and state.

</td></tr><tr><td class="sub-head" colspan="3">

My Achievements

</td></tr><tr><td>

My YTD Total Spend

</td><td>

Widget

</td><td>

View the year-to-date sum of all the spend for purchase lines managed by the buyer, excluding blanket purchase orders.

</td></tr><tr><td>

My YTD Spend Categorization

</td><td>

Pie chart

</td><td>

View the breakdown of your total year-to-date spend by addressable and non-addressable categories.

 The total spend is the sum of the total line amount on the purchase order line, excluding blanket purchase orders, where the logged-in user is also the one assigned, the state of the purchase order isn’t closed canceled, and the spend categorization is either addressable or non-addressable.

</td></tr><tr><td>

My YTD Total Savings

</td><td>

Widget

</td><td>

View the year-to-date sum of the negotiated savings across all closed complete purchase requisition lines assigned to the buyer.

</td></tr><tr><td>

My YTD Negotiation Outcomes

</td><td>

Stacked bar chart

</td><td>

View your year-to-date negotiation outcomes against the negotiation count, grouped by negotiation type.

 Some of the possible negotiation outcomes are contract renewal, quote, RFx, and so on. Negotiation types can be cost avoidance, standard savings, contract terms negotiations, or unsuccessful negotiations.

 This report shows negotiation outcomes where the corresponding negotiation state is either Closed Complete or Closed Canceled.

</td></tr><tr><td>

My Average Sourcing Request Cycle Time

</td><td>

Bar with line

</td><td>

View the average time from when a sourcing request is created to when its state is Closed Complete or Closed No Decision.

 The report pulls all the sourcing requests that went into Closed Complete or Closed No Decision state for the month, and takes the cycle time from when they were opened. This data is retrieved from the **Duration** field on the sourcing request.

</td></tr><tr><td>

My Average Purchase Requisition Cycle Time

</td><td>

Bar with line

</td><td>

View the average purchase requisition cycle time from when a purchase requisition is created to when its state is Closed Complete, Closed Rejected, or Closed Canceled.

 The report pulls all the purchase requisitions that went into Closed Complete, Closed Rejected, or Closed Canceled status for the month, and takes the cycle time from when they were opened. This data is retrieved from the **Duration** field on the purchase requisition.

</td></tr></tbody>
</table>For information on how to work with dashboards in configurable workspaces, see Dashboards in Platform Analytics.

For information on how to work with widgets and data visualizations in configurable workspaces, see Data visualizations in Platform Analytics.

**Parent Topic:**[Performance Analytics for Sourcing and Procurement Operations](performance-analytics-for-spo.md)

