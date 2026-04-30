---
title: Customer Service Agent dashboard
description: The Customer Service Agent dashboard provides quick access to your cases based on criteria that help you prioritize your work. The dashboard also displays summary data on metrics for your organization.
locale: en-US
release: xanadu
product: Analytics and Reporting Solutions for Customer Service
classification: analytics-and-reporting-solutions-for-customer-service
topic_type: concept
last_updated: "2024-08-08"
reading_time_minutes: 2
breadcrumb: [Customer Service Platform Analytics Solutions, Analytics and reporting for Customer Service Management, Customer Service Management]
---

# Customer Service Agent dashboard

The Customer Service Agent dashboard provides quick access to your cases based on criteria that help you prioritize your work. The dashboard also displays summary data on metrics for your organization.

To view the Customer Service Agent dashboard, navigate to **Performance Analytics** &gt; **Dashboards**. Click the **All** tab and select **Customer Service Management** from the Group menu. Click the **Customer Service Agent** or **Customer Service Agent - Advanced** tile.

The Customer Service Management - Advanced Performance Analytics Solution adds the Customer Service Agent - Advanced dashboard. The Advanced dashboard contains two additional indicators: Exceeding Chat Target and Exceeding Case Target.

## End users and roles

The Customer Service Agent dashboard includes the following end users and roles.

|End user and goal|Required role|
|-----------------|-------------|
|Customer service agent: View and prioritize your assigned cases. View case trends for all agents.|sn\_customerservice\_agent|
|Customer service manager: View and prioritize your assigned cases. View case trends for all agents.|sn\_customerservice\_manager|
|Content administrator: Can edit the dashboard and manage users, groups, and roles for the dashboard.|pa\_admin|
|Content creator: Can view the dashboard.|pa\_viewer|

![Tab displaying different report types from the Customer Service Agent dashboard. For the text description, refer to the Reports section.](../image/csm-agent-my-work.png "My Work tab")

## Reports

The Customer Service Agent dashboard includes the following reports.

<table id="table_xvt_hl4_2fb"><thead><tr><th>

Title

</th><th>

Description

</th></tr></thead><tbody><tr><td>

My Open Cases

</td><td>

Cases assigned to me that are not resolved, closed, or canceled.

</td></tr><tr><td>

My Cases With Problems

</td><td>

Cases assigned to me that are part of a parent case that is assigned to a system admin.**Note:** To view this data in the dashboard, add the sn\_problem\_read role to the sn\_customerservice\_agent role.

</td></tr><tr><td>

My New Cases

</td><td>

Cases that I have not yet responded to.

</td></tr><tr><td>

My Group's P1 Cases

</td><td>

P1 cases that are assigned to a member of my group.

</td></tr><tr><td>

My Group's Open Cases

</td><td>

Cases assigned to a member of my group that are not resolved, closed, or canceled.

</td></tr><tr><td>

My KBs Created

</td><td>

List of all KB articles that I created.

</td></tr></tbody>
</table>![Customer Service Agent dashboard displaying overall organizational trends in various line graphs. For the text description, refer to the following Indicators table.](../image/csm-agent-org-trends.png "Organizational Trends tab")

## Indicators

The Customer Service Agent dashboard includes the following indicators.

<table id="table_ez3_gnx_23b"><thead><tr><th>

Indicator

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CSAT

</td><td>

Average customer satisfaction based on survey results. The percent change in the current period appears under the total percentage. For more information about CSAT, see [Customer service satisfaction surveys](c_CustomerServiceSatisfactionSurvey.md).

</td></tr><tr><td>

First Call Resolution

</td><td>

Percentage of cases that were resolved during first contact with the customer. The percent change in the current period appears under the total percentage.

</td></tr><tr><td>

Exceeding Chat Target

</td><td>

Percentage of all Chat work items that have exceeded the target wait time. For more information about the Chat service channel, see [Advanced Work Assignment service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) **Note:** This indicator is only viewable on the Customer Service Agent - Advanced dashboard.

</td></tr><tr><td>

Exceeding Case Target

</td><td>

Percentage of all Case work items that have exceeded the target wait time. For more information about the Case service channel, see [Advanced Work Assignment service channels](https://www.servicenow.com/docs/access?context=awa-service-channels&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) **Note:** This indicator is only viewable on the Customer Service Agent - Advanced dashboard.

</td></tr><tr><td>

Avg. Time to Resolution

</td><td>

Average time for a case to be marked as closed or resolved.**Note:** On the Customer Service Agent - Advanced dashboard, this indicator is called Mean Time to Resolve.

</td></tr><tr><td>

Backlog Growth

</td><td>

Number of backlogged cases for all agents over time.

</td></tr></tbody>
</table>