---
title: Financial Services Complaint Management dashboard
description: With the Financial Services Complaint Management dashboard, you can get an insight into how your team and business are performing for the complaints that were received for your financial services. You can monitor the status of the complaint service cases, see trends, and drill down into the details from a single view.
locale: en-US
release: xanadu
product: Financial Services Complaint Management
classification: financial-services-complaint-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Analytics and reporting for Financial Services Complaint Management, Financial Services Complaint Management, Common applications, Financial Services Operations \(FSO\)]
---

# Financial Services Complaint Management dashboard

With the Financial Services Complaint Management dashboard, you can get an insight into how your team and business are performing for the complaints that were received for your financial services. You can monitor the status of the complaint service cases, see trends, and drill down into the details from a single view.

**Important:** The Financial Services Complaint Management dashboard has been modernized to give you a better user experience.

For any time that you specify, you can view the details for the closed cases that breached an SLA, the open cases that need immediate attention, and the average closing times of the complaint cases.

## Required ServiceNow AI Platform roles

-   sn\_bom\_compl.manager, needed to see the dashboard widgets and data.
-   sn\_bom\_compl.admin, needed to edit the dashboard.

## Access the Financial Services Complaint Management dashboard

To access the Financial Services Complaint Management dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Complaint Management** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see [Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Complaint Management** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table id="table_lqm_w3z_ypb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Complaint manager

</td><td>

Needs to gain visibility into the status of the complaint cases and do the following tasks:-   Monitor the open complaint cases that have breached a Service Level Agreement \(SLA\) or are about to breach an SLA and need attention
-   Monitor the volume of the complaint cases for each complaint category and their trend
-   Review the average closing time of the cases for each category
-   Drill down into the details in a complaint category

</td></tr><tr><td>

Complaint admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **Number of open cases breached sla**

    Number of the open complaint cases in the last seven days that breached an SLA.

-   **Open Cases with SLA Breached greater than 80%**

    Number of the open complaint cases where the SLA-elapsed percentage in the last six days is greater than 80 percent.

-   **Number of open cases**

    Breakdown of the open complaint cases in the last seven days with the Age and Type breakdowns.

-   **Number of new cases**

    Number of the new complaint cases opened today. The indicator is used to compare and see the trend of the number of cases that were created versus the number of cases that were closed in the last seven days.

-   **Average time to close case**

    Breakdown of the average number of hours to close complaint cases by Complaint Type. The score is calculated according to this formula:

    ```
    [FSO Complaint.Summed duration of closed cases]/[FSO Complaint.Number of closed cases]
    ```

-   **Number of closed cases with sla**

    Number of the cases that were closed that day within an SLA. The indicator is used to compare the number of cases that were closed that met an SLA versus the number of cases that breached an SLA in the last seven days.

-   **Number of closed cases**

    Breakdown of the complaint cases that were closed today with the Type and Category breakdowns.


## Breakdowns

-   Age
-   Category
-   Type

## Data visualizations

The following table shows the available data visualizations in the Financial Services Complaint Management application.

<table id="table_qqm_w3z_ypb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Closed Cases – Top 10 Complaint Categories

</td><td>

Horizontal Bar ![Horizontal bar graph icon.](../../performance-analytics/image/horizontal-bar.png)

</td><td>

Complaint Case\[sn\_bom\_compl\_service\]

</td><td>

Breakdown of top ten complaint categories that have maximum number of closed cases \(in descending order\) in last six months.

</td></tr></tbody>
</table>## Filters

The following table shows the available filters in the Financial Services Complaint Management application.

|Name|Type|Description|
|----|----|-----------|
|Age|Bucket|Shows the age ranges in days for complaint cases.|
|Complaint Category|Choice|Shows all the active complaint categories for the Complaint service \[sn\_bom\_compl\_service\] table.|
|Complaint Type|Choice|Shows all the active complaint types for the Complaint service \[sn\_bom\_compl\_service\] table.|

**Parent Topic:**[Platform Analytics Solutions for Financial Services Operations](../../application-content-packs/concept/fso-content-pack.md)

