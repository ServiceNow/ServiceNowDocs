---
title: Personal Deposit Operations dashboard
description: With the Financial Services Personal Deposit Operations dashboard, you can get an insight into how your team and business are performing for the deposit service requests received for your financial services. You can monitor the status of the deposit service cases, see trends, and drill down into the details from a single view.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Personal Deposit Operations dashboard

With the Financial Services Personal Deposit Operations dashboard, you can get an insight into how your team and business are performing for the deposit service requests received for your financial services. You can monitor the status of the deposit service cases, see trends, and drill down into the details from a single view.

**Important:** The Financial Services Personal Deposit Operations dashboard has been modernized to give you a better user experience.

For any time that you specify, you can view the details for closed cases that breached a Service Level Agreement \(SLA\), the open cases that need immediate attention, and the average closing times of the deposit cases.

## Required ServiceNow AI Platform roles

-   sn\_bom\_deposit\_b2c.manager, needed to see the dashboard widgets and data.
-   sn\_bom\_deposit\_b2c.admin, sn\_bom\_pa.admin, and pa\_admin, needed to edit the dashboard.

## Access the Financial Services Personal Deposit Operations dashboard

To access the Financial Services Personal Deposit Operations dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, navigate to **All** &gt; **Deposit Operations** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see Analytics Center.

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout by navigating to **All** &gt; **Deposit Operations** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table id="table_e2b_vdr_hsb"><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Deposit manager

</td><td>

Needs to gain visibility into the status of the deposit cases and do the following tasks:-   Monitor the open deposit cases that have breached a Service Level Agreement \(SLA\) or are about to breach an SLA and need attention
-   Monitor the daily, weekly, and monthly trends of the volume of deposit cases
-   Review the average closing time of the cases
-   Drill down into the details in a deposit service case

</td></tr><tr><td>

Deposit admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **B2C Deposit.Originate deposit account created cases**

    Number of the deposit cases that were created today where the deposit service is Originate deposit account.

-   **B2C Deposit.Add financial relationship created cases**

    Number of the deposit cases that were created today where the deposit service is Add financial relationship.

-   **B2C Deposit.Add standing order created cases**

    Number of the deposit cases that were created today where the deposit service is Add standing order.

-   **B2C Deposit.Cancel standing order created cases**

    Number of the deposit cases that were created today where the deposit service is Cancel standing orders.

-   **B2C Deposit.modify standing order created cases**

    Number of the deposit cases that were created today where the deposit service is Modify standing order.

-   **B2C Deposit.Failed standing order created cases**

    Number of the deposit cases that were created today where the deposit service is Failed standing order.

-   **B2C Deposit.Close deposit account created cases**

    Number of the deposit cases that were created today where the deposit service is Close deposit account.

-   **B2C Deposit.modify standing order open cases**

    Number of the open deposit cases that day where the deposit service is Modify standing order.

-   **B2C Deposit.Originate deposit account open cases**

    Number of the open deposit cases that day where the deposit service is Originate deposit account.

-   **B2C Deposit.Add standing order open cases**

    Number of the open deposit cases that day where the deposit service is Add standing order.

-   **B2C Deposit.Failed standing order open cases**

    Number of the open deposit cases that day where the deposit service is Failed standing order.

-   **B2C Deposit.Cancel standing order open cases**

    Number of the open deposit cases that day where the deposit service is Cancel standing orders.

-   **B2C Deposit.Add financial relationship open cases**

    Number of the open deposit cases that day where the deposit service is Add financial account relationship.

-   **B2C Deposit.Close deposit account open cases**

    Number of the open deposit cases that day where the deposit service is Close deposit account.

-   **B2C Deposit.Number of account closure closed cases checkings**

    Number of the deposit cases that were closed today where the deposit service is Close deposit account and the deposit account is Personal Checking Account.

-   **B2C Deposit.Number of account closure closed cases savings**

    Number of the deposit cases that were closed today where the deposit service is Close deposit account and the deposit account is Personal Saving Account.

-   **B2C Deposit.Number of originate closed cases checking**

    Number of the deposit cases that were closed today where the deposit account is Personal Checking Account.

-   **B2C Deposit.Number of originate closed cases savings**

    Number of the deposit cases that were closed today where the deposit account is Personal Saving Account.

-   **B2C Deposit.Number of created cases savings**

    Number of the deposit cases that were created today where the deposit account is Personal Saving Account and the deposit service is not Originate deposit account or Close deposit account.

-   **B2C Deposit.Number of created cases checkings**

    Number of the deposit cases that were created today where the deposit account is Personal Checking Account and the deposit service is not Originate deposit account or Close deposit account.

-   **B2C Deposit.Number of open cases**

    Number of the open deposit cases that day where the breakdown is Age.

-   **B2C Deposit.Number of closed cases**

    Number of the deposit cases that were closed today with Age and Service breakdowns.

-   **B2C Deposit.Number of closed cases with sla**

    Number of the deposit cases that were closed that day within an SLA. The indicator is used to compare the number of cases that were closed that met an SLA versus the number of cases that breached an SLA.

-   **B2C Deposit.Number of closed cases with breached sla**

    Number of the deposit cases that were closed that day that breached an SLA.

-   **B2C Deposit.Number of open cases breached sla**

    Number of the open deposit cases that day that breached an SLA.

-   **B2C Deposit.Open Cases with SLA Breached greater than 80%**

    Number of the open deposit cases that day where the SLA-elapsed percentage is greater than 80 percent.

-   **B2C Deposit.Summed duration of closed cases**

    Number of hours to close the deposit cases that day Age and Service breakdowns.

-   **B2C Deposit.Average time to close case**

    Average number of hours to close the deposit cases where the breakdown is Service. The score is calculated according to this formula:

    ```
    [B2C Deposit.Summed duration of closed cases]/[B2C Deposit.Number of closed cases]
    ```


## Breakdowns

-   Age
-   Service

