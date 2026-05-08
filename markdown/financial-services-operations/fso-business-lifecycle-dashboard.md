---
title: Business Lifecycle Operations dashboard
description: With the Business Lifecycle Operations dashboard, you can get insight into how your team and business are performing for the business lifecycle cases.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Business Lifecycle Operations dashboard

With the Business Lifecycle Operations dashboard, you can get insight into how your team and business are performing for the business lifecycle cases.

**Important:** The Financial Services Business Lifecycle dashboard has been modernized to give you a better user experience.

You can monitor the status of the lifecycle cases, see trends, and drill down into the details from a single view. For any time that you specify, you can view the details for the open cases, the new cases, and the average closing times of the lifecycle cases.

## Required ServiceNow AI Platform roles

-   sn\_bom\_clo\_b2b.manager, required to view the dashboard widgets and data.
-   sn\_bom\_clo\_b2b.admin, required to edit the dashboard.

## Access the Financial Services Business Lifecycle dashboard

To access the Financial Services Business Lifecycle dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **Business Lifecycle** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see Analytics Center.

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Customer Lifecycle Operations** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table id="table_ygh_jwc_fqb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Account manager

</td><td>

Needs to gain visibility into the real-time status of the business lifecycle cases and do the following tasks:-   Monitor all the open cases that have breached a Service Level Agreement \(SLA\)
-   Monitor all the open cases according to the agent and age
-   Review all the new cases for a service, agent, or agent group
-   Review the average closing time of cases for a service, agent, or group within 30 days
-   Drill down into the details in a category

</td></tr><tr><td>

Account admin

</td><td>

Needs to perform all the Account Manager tasks plus customize views.

</td></tr></tbody>
</table>## Indicators

-   **Open Cases - SLA Breached**

    Percentage of the open cases that breached an SLA. The data is calculated according to this formula:

    ```
    [[Number of open Cases with Breached SLAs]] / [[Number of Open Cases]] * 100
    ```

-   **Open Cases - SLA About to be Breached**

    Average number of the open cases that are close to breaching an SLA. The data for this indicator is collected from the \[task\_sla\] table.

-   **Open Cases by Age**

    Breakdown score and trend of the open cases by age in days. The data is calculated according to this formula:

    ```
    [[Summed age of Open Cases]] / [[Number of Open Cases]] / 24
    ```

-   **Average Time to Close in Last 30 Days**

    Breakdown of the average closing time in days of the cases by the service, agent, or assignment group in the last seven days. The score is calculated according to this formula:

    ```
    [[B2C CLO.Summed duration of closed cases]]/[[B2C CLO.Number of closed cases]]
    ```

-   **New Cases vs. Closed Cases**

    Breakdown of the new cases by the service, agent, or agent group versus the closed cases. The data for the cases is collected from the \[sn\_bom\_clo\_service\] table.

-   **Closed Cases - SLA Met vs. SLA Breached**

    Number of the cases where the SLAs were met versus the cases where the SLAs were breached. The data for the cases is collected from the \[sn\_bom\_clo\_service\] table.


## Breakdowns

-   Age
-   Service

## Filters

The following table shows the available filters in the Business Lifecycle Operations dashboard.

|Name|Type|Description|
|----|----|-----------|
|Age|Bucket|Shows the age ranges in days for the Business Lifecycle cases.|
|Service|List|Fetches the records for all the Business Lifecycle cases.|

**Parent Topic:**[Implementing Platform Analytics solutions](../../application-content-packs/concept/fso-content-pack.md)

