---
title: Personal Lines Servicing dashboard
description: With the Personal Lines Servicing dashboard, you can get an insight into how your team and business are performing for the personal policy service requests that were received for your insurance services.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Personal Lines Servicing dashboard

With the Personal Lines Servicing dashboard, you can get an insight into how your team and business are performing for the personal policy service requests that were received for your insurance services.

**Important:** The Personal Lines Servicing dashboard has been modernized to give you a better user experience.

The Personal Lines Servicing dashboard enables you to monitor the status of the policy service cases, see trends, and drill down into the details from a single view. For any time that you specify, you can view the details for the closed cases that breached a Service Level Agreement \(SLA\), the open cases that need immediate attention, and the average closing times of the policy service cases.

## Required ServiceNow AI Platform roles

-   sn\_ins\_policy\_b2c.manager, required to view the dashboard widgets and data.
-   sn\_ins\_policy\_b2c.admin, sn\_bom\_pa.admin, and pa\_admin, required to edit the dashboard.

## Access the Personal Lines Servicing dashboard

To access the Personal Lines Servicing dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Personal Lines Servicing** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see [Analytics Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center.md).

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout by navigating to **All** &gt; **Personal Lines Servicing** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Personal lines manager

</td><td>

Needs to gain visibility into the real-time status of insurance cases and do the following tasks:-   Monitor all the open insurance cases that have breached a Service Level Agreement \(SLA\)
-   Monitor the volume of each insurance case type and their trend
-   Review agent productivity
-   Review the average closing time of the cases for a service, agent, or group
-   Monitor the details of requests by the policy type
-   Drill down into the details in an error category

</td></tr><tr><td>

Personal lines admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **Personal Lines Servicing.Summed duration of closed cases**

    Number of hours to close the personal lines cases that day with Stage and Service breakdowns.

-   **Personal Lines Servicing.Number of closed cases**

    Number of the personal lines cases that were closed today with Stage and Service breakdowns.

-   **Personal Lines.Open Cases with SLA Breached greater than 80%**

    Number of the open personal lines cases that day where the SLA-elapsed percentage is greater than 80 percent.

-   **Personal Lines: Number of change coverage cases created for both auto and home**

    Number of the personal lines cases that were created today where the personal lines service is the Personal auto change coverage account or homeowners change coverage.

-   **Personal Lines Servicing.Number of closed cases with breached sla**

    Number of the personal lines cases that were closed that day that breached an SLA.

-   **Personal Lines:Number of open cases breached SLA**

    Number of the open personal lines cases that day that breached an SLA.

-   **Personal lines.Number of change coverage open cases for auto and home**

    Number of the open personal lines cases that day where the personal lines service is Personal auto change coverage account or homeowners change coverage.

-   **Personal Lines Servicing.Number of cases rejected by customer**

    Number of the cases that were rejected by a customer.

-   **Personal Lines Servicing.Number of closed cases with SLA**

    Number of the personal lines cases that were closed that day within an SLA. The indicator is used to compare the number of cases closed that met an SLA versus the number of cases that breached an SLA.


## Breakdowns

-   Policy Case Stage
-   Policy Service
-   Policy Rejection Reason

**Parent Topic:**[Implementing Platform Analytics solutions](../../application-content-packs/concept/fso-content-pack.md)

