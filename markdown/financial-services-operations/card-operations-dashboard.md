---
title: Dispute Management dashboard
description: With the Dispute Management dashboard, you can get an insight into how your team and business are performing for the card service requests that were received for your financial services.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Analytics and reporting solutions, Financial Services Operations \(FSO\)]
---

# Dispute Management dashboard

With the Dispute Management dashboard, you can get an insight into how your team and business are performing for the card service requests that were received for your financial services.

**Important:** The Dispute Management dashboard has been modernized to give you a better user experience.

You can monitor the status of card service cases from a single view. For any time that you specify, you can view the details for the closed cases that breached a Service Level Agreement \(SLA\), the open cases that need immediate attention, and the average closing times of the card cases.

## Required ServiceNow AI Platform roles

-   sn\_bom\_credit\_card.dispute\_manager, needed to see the dashboard widgets and data.
-   sn\_bom\_credit\_card.admin, sn\_bom\_pa.admin, and pa\_admin, needed to edit the dashboard.

## Access the Dispute Management dashboard

To access the Dispute Management dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Card Operations** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see [Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center&version=yokohama&pubname=yokohama-now-intelligence&ft:locale=en-US).

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Card Operations** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Card dispute manager

</td><td>

Needs to gain visibility into the status of the dispute cases and do the following tasks:-   Monitor the open dispute cases that have breached a Service Level Agreement \(SLA\) or are about to breach an SLA and need attention
-   Monitor the daily, weekly, and monthly trends of the volume of dispute cases
-   Review the average closing time of cases
-   Drill down into the details in a dispute service case

</td></tr><tr><td>

Credit card admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **Card Dispute.Number of closed cases with sla**

    Number of the dispute cases that were closed that day within an SLA. The indicator is used to compare the number of cases closed that met SLA versus the number of cases that breached an SLA.

-   **Card Dispute.Number of open cases breached sla**

    Number of the open dispute cases that day that breached an SLA.

-   **Card Dispute.Number of chargeback tasks**

    Number of the tasks where the dispute was a chargeback.

-   **Card Dispute.Summed duration of closed cases**

    Number of hours to close the dispute cases that day with Age and Service breakdowns.

-   **Card dispute.Number of open cases**

    Number of the open dispute cases that day where the breakdown is Age.

-   **Card Dispute.Number of dispute write off**

    Number of the dispute transactions where the outcome was a write off.

-   **Card Dispute.Number of successful chargebacks**

    Number of the transactions where the outcome was a successful chargeback.

-   **Card Dispute.Number of closed cases**

    Number of the dispute cases closed today where the breakdowns are Age and Service.

-   **Card Dispute.Number of closed cases with breached sla**

    Number of the dispute cases closed that day that breached an SLA.

-   **Card Dispute.Open Cases with SLA Breached greater than 80%**

    Number of the open dispute cases that day where the SLA-elapsed percentage is greater than 80 percent.

-   **Card Dispute.Number of created cases**

    Number of the dispute cases that were created today.


## Breakdowns

-   Age
-   Card network
-   Chargeback code
-   Dispute reason
-   Service

