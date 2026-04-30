---
title: Customer Service Manager dashboard
description: The Customer Service Manager dashboard displays charts and summary data on metrics like backlog, resolution rates, SLA, customer satisfaction, and per-agent KPIs.
locale: en-US
release: xanadu
product: Analytics and Reporting Solutions for Customer Service
classification: analytics-and-reporting-solutions-for-customer-service
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Customer Service Platform Analytics Solutions, Analytics and reporting for Customer Service Management, Customer Service Management]
---

# Customer Service Manager dashboard

The Customer Service Manager dashboard displays charts and summary data on metrics like backlog, resolution rates, SLA, customer satisfaction, and per-agent KPIs.

To view the Customer Service Manager dashboard, navigate to **Performance Analytics** &gt; **Dashboards**. Click the **All** tab and select **Customer Service Management** from the Group menu. Click the **Customer Service Manager** or **Customer Service Manager - Advanced** tile.

The Customer Service Management - Advanced Performance Analytics Solution adds the Customer Service Manager - Advanced dashboard. The Advanced dashboard contains the additional tab Work Assignment Analytics.

## End users and roles

|End user and goal|Required role|
|-----------------|-------------|
|Customer service manager: View case metrics like backlog, resolution rates, SLA, customer satisfaction, and per-agent KPIs to understand the current performance of customer service at your organization.|sn\_customerservice\_manager|
|Content administrator: Can edit the dashboard and manage users, groups, and roles for the dashboard.|pa\_admin|
|Content creator: Can view the dashboard.|pa\_viewer|

## Dashboard breakdowns

The Customer Service Manager dashboard uses the Case Assignment Group breakdown. Select one or more groups to view data for only those groups. By default, data from all groups is shown on the dashboard.

![Tab displaying different case records and trend lines from the Customer Service Manager Advanced dashboard. For the text description, refer to the Overview indicators section.](../image/csm-manager-overview.png "Overview tab")

## Overview indicators

|Indicator|Description|
|---------|-----------|
|CSAT|Average customer satisfaction based on survey results. The percent change in the current period appears under the total percentage. For more information about CSAT, see [Customer service satisfaction surveys](c_CustomerServiceSatisfactionSurvey.md).|
|First Call Resolution|Percentage of cases that were resolved during first contact with the customer. The percent change in the current period appears under the total percentage.|
|Mean Time to Resolve|Average time for a case to be marked as closed or resolved. The percent change in the current period appears under the total percentage.|
|Customers Impacted by Major Case|Number of customers impacted by major cases.|
|Child Cases Auto Created from Major Case|Percentage of child cases that are automatically created from a major case.|
|Open Backlog - Blocked|Number of cases that are blocked and are not resolved.|
|Open Backlog - Unblocked|Number of cases that are not blocked and are not resolved.|
|Backlog Growth|Number of backlogged cases for all agents over time.|

|Indicator|Description|
|---------|-----------|
|CSAT|Average customer satisfaction based on survey results. The percent change in the current period appears under the total percentage. For more information about CSAT, see [Customer service satisfaction surveys](c_CustomerServiceSatisfactionSurvey.md).|
|First Call Resolution|Percentage of cases that were resolved during first contact with the customer. The percent change in the current period appears under the total percentage.|
|Open Cases with Breached SLAs|Percentage of cases that have remained open past the time required by the Service Level Agreement \(SLA\).|
|Unassigned Open Cases|Number of open cases that are not assigned to an agent.|
|Avg. Time to Resolution|Average time for a case to be marked as closed or resolved. The percent change in the current period appears under the total percentage.|
|Backlog Growth|Number of backlogged cases for all agents over time.|
|Open Case Backlog|Chart of cumulative open cases and case age over time.|
|Open Backlog|Number of cases that are not resolved.|

![Tab displaying different reports and records for cases from the Customer Service Manager Advanced dashboard. For the text description, refer to the Analysis indicators section.](../image/csm-manager-analysis.png "Analysis tab")

Trend chart of case backlog over time. Click and move your cursor to view data for any date. Indicators display data for the selected date.

## Analysis indicators

|State|Indicator|Description|
|-----|---------|-----------|
|Open Backlog - Unblocked|% Not Updated in 5 Days|Percentage of open cases that agents have not updated within the last 5 days.|
|% Marked as Major|Percentage of open cases that are major.|
|% with Breached SLAs|Percentage of open cases that have remained open past the time required by the SLA.|
|% with Priority P1|Percentage of open cases that are critical priority.|
|% Escalated|Percentage of open cases that have been escalated.|
|% with Problem|Percentage of open cases connected to a problem.|
|% Agent Reassignment|Percentage of open cases where the Assigned to field has changed at least once.|
|% of Major Candidates|Percentage of open cases that have been proposed as major case candidates.|
|% Re-opened At Least Once|Percentage of open cases where the State was previously Resolved.|
|% with Request|Percentage of open cases connected to a request.|
|Resolved or Closed|% with Problem|Percentage of closed cases connected to a problem.|
|% Caused by Change|Percentage of closed cases caused by a change.|
|Closed in Same Day|Number of cases that were closed on the same day they were created.|
|% Re-opened At Least Once|Percentage of closed cases that were reverted to the open State at least once.|
|% Resolved Major Cases|Percentage of closed cases that are major cases.|
|% Re-assigned|Percentage of closed cases that are reassigned.|
|% with Breached SLAs|Percentage of closed cases that remained open past the time required by the SLA.|
|% with Change|Percentage of closed cases connected to a problem.|
|% with Incident|Percentage of closed cases connected to an incident.|
|% with Request|Percentage of closed cases connected to a request.|

## Analysis breakdowns

Select a breakdown to view cases grouped by that breakdown.

Cases in the Open Backlog - Unblocked state can be grouped by the following breakdowns.

-   Case Assignment Group
-   Case Assigned To
-   Account
-   Product
-   State
-   Priority
-   Category
-   Channel

Cases in the Open Backlog - Blocked state can be grouped by the following breakdowns.

-   Blocked Action Status
-   Case Assignment Group

Cases in the Resolved or Closed state can be grouped by the following breakdowns.

-   Case Assignment Group
-   Case Assigned To
-   Account
-   Product
-   Age
-   Priority
-   Category
-   Contact



![Tab displaying case spotlight reports and case list details from the Advanced dashboard. For text descriptions, refer to the Case Spotlight breakdowns and Case Spotlight reports sections.](../image/csm-manager-case-spotlight.png)

## Case Spotlight breakdowns

Select values for the breakdowns to filter the data shown on the dashboard.

-   Assignment Group
-   Case State
-   Case Priority
-   Opened

## Case Spotlight reports

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Cases Above Spotlight Threshold

</td><td>

Number of cases that exceed the Case Spotlight threshold. Every case where **State** is New, Open, or Awaiting info is scored based on priority and last updated date. The score is compared against the threshold value to put cases with high priority in the spotlight.**Note:** You can edit the Case Spotlight spotlight group threshold and criteria to put different types of cases in the spotlight based on your organization's needs.

</td></tr><tr><td>

Spotlight Cases P1 - Critical

</td><td>

Number of cases that exceed the Case Spotlight threshold and are Priority 1.

</td></tr><tr><td>

Spotlight Cases - Unassigned

</td><td>

Number of cases that exceed the Case Spotlight threshold and are not assigned to an agent.

</td></tr><tr><td>

Case Spotlight

</td><td>

List of cases that exceed the Case Spotlight threshold.

</td></tr></tbody>
</table>

![Tab displaying different case resolution reports and agent efficiency trends from the Customer Service Manager - Advanced dashboard. For the text description, refer to the Agent analysis indicators section.](../image/csm-manager-agent-analysis.png)

## Agent analysis indicators

<table id="table_ixq_hcp_f3b"><thead><tr><th>

Indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Avg. Time to Resolution

</td><td>

Average time for a case to be marked as closed or resolved for each agent. Ranked from fastest to slowest.**Note:** On the Customer Service Manager - Advanced dashboard, this indicator is called Mean Time to Resolve.

</td></tr><tr><td>

First Call Resolution

</td><td>

Percentage of cases for each agent that were resolved during first contact with the customer. Ranked from highest to lowest.

</td></tr><tr><td>

CSAT

</td><td>

Average customer satisfaction for each agent based on survey results. Ranked from highest to lowest. For more information about CSAT, see [Customer service satisfaction surveys](c_CustomerServiceSatisfactionSurvey.md).

</td></tr><tr><td>

Agent Efficiency Trend \(Mean Time to Resolve\)

</td><td>

Average time for a case to be marked as closed or resolved for each agent shown over time.

</td></tr><tr><td>

Closed Cases by Agent and Account.

</td><td>

Number of cases closed by each agent for each account.

</td></tr></tbody>
</table>![Tab displaying different work assignment reports from the Customer Service Manager - Advanced dashboard. For text descriptions, refer to the Work Assignment Analytics reports and Work Assignment Analytics indicators sections.](../image/csm-manager-work-assignment.png "Work Assignment Analytics tab")

**Note:** The Work Assignment Analytics tab can only be viewed on the Customer Service Manager - Advanced dashboard. Customer Service \[com.sn\_customerservice\] and Performance Analytics - Content Pack - Advanced Work Assignment \[com.snc.pa.awa\] must be activated on your instance.

## Work Assignment Analytics reports

|Report|Description|
|------|-----------|
|Average Chat Wait Time - Last Hour|Average amount of time that customers have spent waiting for an agent response in the past hour for chat work items.|
|Average Case Wait Time - Last Hour|Average amount of time that customers have spent waiting for an agent response in the past hour for case work items.|

## Work Assignment Analytics indicators

|Indicator|Description|
|---------|-----------|
|Exceeding Target Work Items|Percentage of all work items that have exceeded the target wait time.|
|Assigned Work Items|Percentage of all work items that are assigned to agents.|
|Abandoned Work Items|Percentage of all work items that agents have abandoned.|

![Customer Service Manager Advanced dashboard showing the number of open cases filtered with short description in the word cloud view along with Trend line and Related Records.](../image/csm-manager-text-analysis.png "Text Analytics tab")

**Note:** The Text Analytics tab is visible only if the Performance Analytics Premium for Customer Service plugin \[com.snc.pa.premium.cs\] is installed.

Text Analytics displays a word cloud of most frequently used words and phrases in the short descriptions of open cases, providing insight into emerging issues reported by users.

-   Drill down on a word to view other words associated with cases that contain that keyword.
-   Search the word cloud for specific terms.

**Trend line**: Shows the frequency of top keywords over time. Click and move your cursor to view data for any date.**Related Records**: List of cases containing the keywords you selected from the word cloud.

