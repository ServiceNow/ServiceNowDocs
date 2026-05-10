---
title: Personal Lines Claims dashboard
description: With the Personal Lines Claims dashboard, you can get an insight into how your team and business are performing for the claim service requests that were received for your personal lines policies.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Personal Lines Claims dashboard

With the Personal Lines Claims dashboard, you can get an insight into how your team and business are performing for the claim service requests that were received for your personal lines policies.

The Personal Lines Claims dashboard enables you to monitor the status of the claim cases, see trends, and drill down into the details from a single view. For any given duration, you can view the details for the closed cases that breached a Service Level Agreement \(SLA\), open cases that need immediate attention, and duration of closed claim cases.

**Important:** Platform Analytics Workspace is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

To access the Personal Lines Claims dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see [Analytics Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center.md).

## Required ServiceNow AI Platform roles

-   sn\_ins\_claim\_pers.manager, required to view the dashboard widgets and data.
-   sn\_ins\_claim\_pers.admin, sn\_bom\_pa.admin, and pa\_admin, required to edit the dashboard.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Personal lines claims manager

</td><td>

Needs to gain visibility into the real-time status of the claim cases and do the following tasks:-   Monitor all the open claim cases that have breached a Service Level Agreement \(SLA\)
-   Monitor the volume of each claim case type and their trend
-   Review the average closing time of cases for a representative, processor, or group

</td></tr><tr><td>

Personal lines claims admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **Personal Lines Claims.Open cases**

    Daily number of the open cases.

-   **Personal Lines Claims.Number of open cases breached SLA**

    Daily number of the open cases with a breached SLA.

-   **Personal Lines Claims.No of cases created**

    Number of the cases that were created today or daily.

-   **Personal Lines Claims.Number of denied cases**

    Number of the cases that were closed today with denied claims.

-   **Personal Lines Claims.Summed duration of closed cases**

    Summed duration of the hours of cases that were closed today.

-   **Personal Lines Claims.Number of closed cases**

    Number of the cases that were closed today.

-   **Personal Lines Claims.Number of closed cases with SLA**

    Number of the cases that were closed today within an SLA.

-   **Personal Lines Claims.Number of closed cases with breached SLA**

    Number of the personal lines cases that were closed that day with a breached SLA. The indicator is used to compare the number of cases that were closed that met an SLA versus the number of cases that breached an SLA.

-   **Personal Lines Claims.Open cases with SLA breached greater than 80%**

    Number of the open personal lines cases where the SLA-breached percentage is greater than 80 percent \(actual time elapsed &gt;80%\).

-   **Personal Lines Claims.Number of paid cases**

    Daily number of the paid cases with an SLA.

-   **Personal Lines Claims.SIU cases**

    Daily number of the personal lines claims open cases in SIU review.

-   **Personal Lines Claims.Claims payout trend**

    Trend of the claim payout daily on the closed cases.


## Breakdowns

-   Stage
-   Age
-   Claim service
-   Customer
-   Product
-   SLA percentage

**Parent Topic:**[Implementing Platform Analytics solutions](../../application-content-packs/concept/fso-content-pack.md)

