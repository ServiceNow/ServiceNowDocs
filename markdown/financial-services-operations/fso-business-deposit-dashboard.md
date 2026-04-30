---
title: Business Deposit Operations dashboard
description: With the Financial Services Business Deposit Operations dashboard, you can get an insight into how your team and business are performing for deposit service requests received for your financial services. You can monitor the status of deposit service cases, see trends, and drill down into the details from a single view.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Business Deposit Operations dashboard

With the Financial Services Business Deposit Operations dashboard, you can get an insight into how your team and business are performing for deposit service requests received for your financial services. You can monitor the status of deposit service cases, see trends, and drill down into the details from a single view.

**Important:** The Financial Services Business Deposit Operations dashboard has been modernized to give you a better user experience.

For any time period that you specify, you can view the details for the closed cases that breached an SLA, the open cases that need immediate attention, and the average closing times of the deposit cases.

## Required ServiceNow AI Platform roles

-   sn\_bom\_deposit\_b2b.manager, needed to see the dashboard widgets and data.
-   sn\_bom\_deposit\_b2b.admin, sn\_bom\_pa.admin, and pa\_admin, needed to edit the dashboard.

## Access the Financial Services Business Deposit Operations dashboard

To access the Financial Services Business Deposit Operations dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Deposit Operations** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see [Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center&version=zurich&pubname=zurich-now-intelligence&ft:locale=en-US).

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Deposit Operations** &gt; **Dashboard**.

## Use cases

For examples of how the different people in your organization can use this dashboard, see the use cases in the following table.

<table id="table_v13_rdr_hsb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Deposit manager

</td><td>

Needs to gain visibility into the status of the deposit cases and do the following tasks:-   Monitor the open deposit cases that have breached a Service Level Agreement \(SLA\) or are about to breach an SLA and need attention
-   Monitor the daily, weekly, and monthly trends of the volume of deposit cases
-   Review the average closing time of cases
-   Drill down into the details in a deposit service case

</td></tr><tr><td>

Deposit admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **B2B Deposit.Originate deposit account created cases**

    Number of the deposit cases that were created today where the deposit service is Originate deposit account.

-   **B2B Deposit.Add financial relationship created cases**

    Number of the deposit cases that were created today where the deposit service is Add financial relationship.

-   **B2B Deposit.Add standing order created cases**

    Number of the deposit cases that were created today where the deposit service is Add standing order.

-   **B2B Deposit.Cancel standing order created cases**

    Number of the deposit cases that were created today where the deposit service is Cancel standing orders.

-   **B2B Deposit.modify standing order created cases**

    Number of the deposit cases that were created today where the deposit service is Modify standing order.

-   **B2B Deposit.Failed standing order created cases**

    Number of the deposit cases that were created today where the deposit service is Failed standing order.

-   **B2B Deposit.Close deposit account created cases**

    Number of the deposit cases that were created today where the deposit service is Close deposit account.

-   **B2B Deposit.modify standing order open cases**

    Number of the open deposit cases that day where the deposit service is Modify standing order.

-   **B2B Deposit.Originate deposit account open cases**

    Number of the open deposit cases that day where the deposit service is Originate deposit account.

-   **B2B Deposit.Add standing order open cases**

    Number of the open deposit cases that day where the deposit service is Add standing order.

-   **B2B Deposit.Failed standing order open cases**

    Number of the open deposit cases that day where the deposit service is Failed standing order.

-   **B2B Deposit.Cancel standing order open cases**

    Number of the open deposit cases that day where the deposit service is Cancel standing orders.

-   **B2B Deposit.Add financial relationship open cases**

    Number of the open deposit cases that day where the deposit service is Add financial relationship.

-   **B2B Deposit.Close deposit account open cases**

    Number of the open deposit cases that day where the deposit service is Close deposit account.

-   **B2B Deposit.Number of account closure closed cases checkings**

    Number of the deposit cases that were closed today where the deposit service is Close deposit account and the deposit account is Business Checking Account.

-   **B2B Deposit.Number of account closure closed cases savings**

    Number of the deposit cases that were closed today where the deposit service is Close deposit account and the deposit account is Business Saving Account.

-   **B2B Deposit.Number of originate closed cases checking**

    Number of the deposit cases that were closed today where the deposit account is Business Checking Account.

-   **B2B Deposit.Number of originate closed cases savings**

    Number of the deposit cases that were closed today where the deposit service is Originate deposit account and the deposit account is Business Saving Account.

-   **B2B Deposit.Number of created cases savings**

    Number of the deposit cases that were created today where the deposit account is Business Saving Account and the deposit service is not Originate deposit account or Close deposit account.

-   **B2B Deposit.Number of created cases checkings**

    Number of the deposit cases that were created today where the deposit account is Business Checking Account and the deposit service is not Originate deposit account or Close deposit account.

-   **B2B Deposit.Number of open cases**

    Number of the open deposit cases that day where the breakdown is Age.

-   **B2B Deposit.Number of closed cases**

    Number of the deposit cases that were closed today with the Age and Service breakdowns.

-   **B2B Deposit.Number of closed cases with sla**

    Number of the deposit cases that were closed that day within an SLA. The indicator is used to compare the number of cases closed that met an SLA versus the number of cases that breached an SLA.

-   **B2B Deposit.Number of closed cases with breached sla**

    Number of the deposit cases that were closed that day that breached an SLA.

-   **B2B Deposit.Number of open cases breached sla**

    Number of the open deposit cases that day that breached an SLA.

-   **B2B Deposit.Open Cases with SLA Breached greater than 80%**

    Number of the open deposit cases that day where an SLA-elapsed percentage is greater than 80 percent.

-   **B2B Deposit.Summed duration of closed cases**

    Number of hours to close the deposit cases that day with the Age and Service breakdowns.

-   **B2B Deposit.Average time to close case**

    Average number of hours to close the deposit cases where breakdown is Service. The score is calculated according to this formula:

    ```
    [B2B Deposit.Summed duration of closed cases]/[B2B Deposit.Number of closed cases]
    ```


## Breakdowns

-   Age
-   Service

**Parent Topic:**[Implementing Platform Analytics solutions](../../application-content-packs/concept/fso-content-pack.md)

