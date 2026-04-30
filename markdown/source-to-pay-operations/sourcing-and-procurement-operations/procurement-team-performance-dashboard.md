---
title: Procurement Team Performance Dashboard
description: Visually analyze how your team is performing on sourcing requests, purchase requisitions, negotiated savings, and negotiation outcomes, over a given period of time, with the help of the Procurement Team Performance Dashboard.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Performance Analytics for Sourcing and Procurement Operations, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Procurement Team Performance Dashboard

Visually analyze how your team is performing on sourcing requests, purchase requisitions, negotiated savings, and negotiation outcomes, over a given period of time, with the help of the Procurement Team Performance Dashboard.

**Note:** This dashboard is available only if you install the Performance Analytics for Sourcing and Procurement Operations application.

## End user and roles

|End user and goal|Required role|
|-----------------|-------------|
|Procurement Specialist Manager: View your organization's overall performance. This role has the same access as a procurement specialist, except that they have access to the manager dashboards.|sn\_shop.procurement\_specialist\_manager|
|Procurement Administrator: View and make configuration changes to the widgets.|sn\_shop.procurement\_administrator|

## Indicators

-   Number of Total Cost Avoidance Negotiations
-   Number of Total Negotiations
-   Number of Closed Purchase Requisitions - Monthly
-   Number of All Purchase Requisition - Monthly
-   Purchase Line Total Negotiated Savings
-   Purchase Requisition - Avg Cycle Time \(Days\) - Monthly
-   Number of Closed Sourcing Requests - Monthly
-   Purchase Line Negotiated Savings
-   Number of Total Contract Terms Negotiations
-   Number of Total Negotiation Unsuccessful
-   Sourcing Request - Avg Cycle Time \(Days\) - Monthly
-   Number of All Sourcing Request - Monthly
-   Parent Line Negotiated Savings
-   Number of Total Standard Savings Negotiations

## Breakdowns

-   Negotiation - AssignedTo
-   PurchaseRequisition - AssignedTo
-   SourcingRequest - AssignedTo

## Reports

**Note:** By default, YTD is configured to start from January. However, this can be configured to start from any month if need be.

For a detailed analysis on each component, select the respective widget or chart.

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Average Sourcing Request Cycle Time

</td><td>

Bar with line

</td><td>

View the average time from when a sourcing request is created to when its state is Closed Complete or Closed No Decision.

 The report pulls all the sourcing requests across the organization that went into Closed Complete or Closed No Decision state for the last five months, and takes the cycle time from when they were opened. This data is retrieved from the **Duration** field on the sourcing request.

 You can set a target cycle time that serves as a benchmark for the organization, and easily visualize how current cycle times compare against it.

</td></tr><tr><td>

Sourcing Request Cycle Time - Last Month

</td><td>

List

</td><td>

View the average cycle time for sourcing requests by buyer across the organization.

 You can also view the number of open sourcing requests that were assigned to the buyer as of last month, which were either closed last month or open throughout the duration of the month.

</td></tr><tr><td>

Average Purchase Requisition Cycle Time

</td><td>

Bar with line

</td><td>

View the average purchase requisition cycle time from when a purchase requisition is created to when its state is Closed Complete, Closed Rejected, or Closed Canceled.

 The report pulls all the purchase requisitions across the organization that went into Closed Complete, Closed Rejected, or Closed Canceled status for the last four months, and takes the cycle time from when they were opened. This data is retrieved from the **Duration** field on the purchase requisition.

 You can set a target cycle time that serves as a benchmark for the organization, and easily visualize how current cycle times compare against it.

</td></tr><tr><td>

Purchase Requisition Cycle Time - Last Month

</td><td>

List

</td><td>

View the average cycle time for purchase requisitions by buyer across the organization.

 You can also view the number of open purchase requisitions that were assigned to the buyer as of last month, which were either closed last month or open throughout the duration of the month.

</td></tr><tr><td>

Negotiated Savings by Buyer - YTD

</td><td>

List

</td><td>

View the sum of the year-to-date negotiated savings across all closed complete purchase lines across the organization.

</td></tr><tr><td>

Negotiation Outcomes by Buyer - YTD

</td><td>

List

</td><td>

View the list of buyers across the organization along with their corresponding year-to-date negotiation outcomes, where the corresponding negotiation state is either Closed Complete or Closed Canceled.

 Some of the possible negotiation outcomes are contract renewal, quote, RFx, and so on. Negotiation types can be cost avoidance, standard savings, contract terms negotiations, or unsuccessful negotiations.

</td></tr></tbody>
</table>For information on how to work with dashboards in configurable workspaces, see [Dashboards in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-dashboards&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

For information on how to work with widgets and data visualizations in configurable workspaces, see [Data visualizations in Platform Analytics](https://www.servicenow.com/docs/access?context=analytics-center-data-visualizations&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

**Parent Topic:**[Performance Analytics for Sourcing and Procurement Operations](performance-analytics-for-spo.md)

