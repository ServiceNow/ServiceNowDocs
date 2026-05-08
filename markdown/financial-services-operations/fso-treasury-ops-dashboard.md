---
title: Treasury Operations dashboard
description: With the Financial Services Treasury Operations dashboard, you can get an insight into how your team and business are performing for the treasury service requests that were received for your financial services.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Treasury Operations dashboard

With the Financial Services Treasury Operations dashboard, you can get an insight into how your team and business are performing for the treasury service requests that were received for your financial services.

**Important:** The Financial Services Treasury Operations dashboard has been modernized to give you a better user experience.

You can monitor the status of the treasury service cases, see trends, and drill down into the details from a single view. For any time that you specify, you can view the details for the closed cases that breached a Service Level Agreement \(SLA\), the open cases that need immediate attention, and the average closing times of the treasury cases.

## Required ServiceNow AI Platform roles

-   sn\_bom\_treasury.manager, needed to see the dashboard widgets and data.
-   sn\_bom\_treasury.admin, sn\_bom\_pa.admin, and pa\_admin, needed to edit the dashboard.

## Access the Financial Services Treasury Operations dashboard

To access the Financial Services Treasury Operations dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Treasury Operations** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see Analytics Center.

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Treasury Operations** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table id="table_zht_mn1_3qb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Treasury manager

</td><td>

Needs to gain visibility into the status of treasury cases and do the following tasks:-   Monitor the open treasury cases that have breached a Service Level Agreement \(SLA\) or are about to breach an SLA and need attention
-   Monitor the volume of the treasury cases for each treasury product
-   Review the average closing time of the cases
-   Drill down into the details in a treasury product

</td></tr><tr><td>

Treasury admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **FSO Treasury.Number of closed cases with sla**

    Number of the cases that were closed that day within an SLA. The indicator is used to compare the number of cases that were closed that met an SLA versus the number of cases that breached an SLA.

-   **FSO Treasury.Number of closed cases with breached sla**

    Number of the treasury cases that were closed that day that breached an SLA.

-   **FSO Treasury.Number of open cases**

    Number of the open treasury cases that day with the Age and Service breakdowns.

-   **FSO Treasury.Number of closed cases**

    Number of the treasury cases that were closed today with the Age and Service breakdowns.

-   **FSO Treasury.Average time to close case**

    Average number of the hours to close the treasury cases where the breakdown is Service. The score is calculated according to this formula:

    ```
    [FSO Treasury.Summed duration of closed cases]/[FSO Treasury.Number of closed cases]
    ```

-   **FSO Treasury.Summed duration of closed cases**

    Total number of hours to close the treasury cases that day with the Age and Service breakdowns.

-   **FSO Treasury.Number of new cases**

    Number of the new treasury cases that were opened today with the Age and Service breakdowns. This indicator, when used with the Number of closed cases indicator, is used to compare and see the trend of the number of cases created versus the cases closed.

-   **FSO Treasury.Number of open cases is going to breach sla**

    Number of the open treasury cases that day where the SLA-elapsed percentage is equal to or greater than 80 percent.

-   **FSO Treasury.Number of open cases breached sla**

    Number of the open treasury cases that day that breached an SLA.


## Breakdowns

-   Age
-   Service

## Filters

The following table shows the available filters in the Treasury Operations dashboard.

|Name|Type|Description|
|----|----|-----------|
|FSO Treasury.Service|Task record|Fetches all the records from the Service Definition \[sn\_bom\_service\_definition\] table where Task type starts with `sn_bom_treasury` and ends with `service`.|
|Age|Bucket|Shows the age ranges in days for treasury cases.|

**Parent Topic:**[Implementing Platform Analytics solutions](../../application-content-packs/concept/fso-content-pack.md)

