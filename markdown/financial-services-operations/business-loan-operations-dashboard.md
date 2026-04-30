---
title: Business Loan Operations dashboard
description: With the Financial Services Business Loan Operations dashboard, you can get an insight into how your team and business are performing for business loan cases. You can monitor the status of loan cases, see trends, and drill down into the details from a single view.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Business Loan Operations dashboard

With the Financial Services Business Loan Operations dashboard, you can get an insight into how your team and business are performing for business loan cases. You can monitor the status of loan cases, see trends, and drill down into the details from a single view.

**Important:** The Financial Services Business Loan Operations dashboard has been modernized to give you a better user experience.

This dashboard is automatically activated when you install the Financial Services Business Loan Operations application.

For any time period that you specify, you can view the details for the open cases, the new cases, and the average closing times of the loan cases.

## Required ServiceNow AI Platform roles

-   sn\_bom\_loan\_b2b.manager, required to view the dashboard widgets and data.
-   sn\_bom\_loan\_b2b.admin, sn\_bom\_pa.admin, and pa\_admin, required to edit the dashboard.

## Access the Financial Services Business Loan Operations dashboard

To access the Financial Services Business Loan Operations dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Loan Operations** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see [Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Loan Operations** &gt; **Dashboard**.

## Use cases

For examples of how the different people in your organization can use this dashboard, see the use cases in the following table.

<table id="table_ov2_tj4_2fb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Loan manager

</td><td>

Needs to gain visibility into the real-time status of the business loan cases and do the following tasks:-   Monitor all the open cases that have breached a Service Level Agreement \(SLA\)
-   Monitor all the open cases by agent and age of the cases
-   Review all the new cases for a service, agent, or agent group
-   Review the average closing time of cases for a service, agent, or group
-   Drill down into the details in a category

</td></tr><tr><td>

Loan admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **% of Open Cases with Breached SLAs**

    Percentage of open cases that breached an SLA on a specific day. The score is calculated according to this formula:

    ```
     [[Number of open cases with breached SLAs] / [Number of open cases]] * 100
    ```

-   **Avg \# of Open Cases per Agent**

    Average number of the open cases for an agent on a specified day. The score is calculated according to this formula:

    ```
    [[Number of open cases] / [Number of agents]]
    ```

-   **Average Age of Open Cases**

    Breakdown score and trend of the open cases by age in days on a specified day. The score for each service is calculated according to this formula:

    ```
    [[Summed age of open cases] / [Number of open cases]] / 24
    ```

-   **Number of New Cases**

    Breakdown of the new cases by the service, agent, or agent group in the last three months. The data for the cases is collected from the \[sn\_bom\_loan\_b2b\_service\] table.

-   **Average Closing Time of Cases**

    Breakdown of the average closing time in days of the cases by the service, agent, or agent group in the last seven days. The score is calculated according to this formula:

    ```
     [[Summed duration of closed cases] / [Number of closed cases]] / 24
    ```


## Breakdowns

-   Agent
-   Agent Group
-   Age
-   Service

**Parent Topic:**[Implementing Platform Analytics solutions](../../application-content-packs/concept/fso-content-pack.md)

