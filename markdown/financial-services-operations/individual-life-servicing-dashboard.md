---
title: Individual Life Servicing dashboard
description: With the Individual Life Servicing dashboard, you can get an insight into how your team and business are performing for the individual policy service requests that were received for your insurance services.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Individual Life Servicing dashboard

With the Individual Life Servicing dashboard, you can get an insight into how your team and business are performing for the individual policy service requests that were received for your insurance services.

**Important:** The Individual Life Servicing dashboard has been modernized to give you a better user experience.

The Individual Life Servicing dashboard enables you to monitor the status of the policy service cases, see trends, and drill down into the details from a single view. For any time that you specify, you can view the details for the closed cases that breached a Service Level Agreement \(SLA\), the open cases that need immediate attention, and the average closing times of the policy service cases.

## Required ServiceNow AI Platform roles

-   sn\_ins\_indiv\_life.manager, required to view the dashboard widgets and data.
-   sn\_ins\_indiv\_life.admin, sn\_bom\_pa.admin, and pa\_admin, required to edit the dashboard.

## Access the Individual Life Servicing dashboard

To access the Individual Life Servicing dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Individual Life Servicing** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see Analytics Center.

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Individual Life Servicing** &gt; **Dashboard**.

## Use cases

For examples of how the different people in your organization would use this dashboard, see the use cases in the following table.

<table><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Individual life policy manager

</td><td>

Needs to gain visibility into the real-time status of insurance cases and do the following:-   Monitor all the open insurance cases that breached a Service Level Agreement \(SLA\)
-   Monitor the volume of each insurance case type and their trend
-   Review agent productivity
-   Review the average closing time of cases for a service, agent, or individual
-   Monitor the details of requests by the policy type
-   Drill down into the details in an error category

</td></tr><tr><td>

Individual life policy admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **Individual Life and Disability Servicing.Summed duration of closed cases**

    Number of hours to close the personal lines cases that day with the Stage and Service breakdowns.

-   **Individual Life and Disability Servicing.Number of closed cases**

    Number of the individual life cases that were closed today with the Stage and Service breakdowns.

-   **Individual Life and Disability Servicing.Open Cases with SLA Breached greater than 80%**

    Number of the open individual life cases that day where the SLA-elapsed percentage is greater than 80 percent.

-   **Individual Life and Disability Servicing.Number of closed cases with breached sla**

    Number of the individual life cases that were closed that day that breached an SLA.

-   **Individual Life and Disability Servicing.Number of open cases breached SLA**

    Number of the open individual life cases that day that breached an SLA.

-   **Individual Life and Disability Servicing.Number of open cases**

    Number of the open individual life cases that day.

-   **Individual Life and Disability Servicing.Number of cases rejected by customer**

    Number of the closed cases that were rejected by customers in the last 30 days, where the solution proposed by the agent was rejected.

-   **Individual Life and Disability Servicing.Number of closed cases with sla**

    Number of the individual life cases that were closed that day within an SLA. The indicator is used to compare the number of cases that were closed that met an SLA versus the number of cases that breached an SLA.

-   **Individual Life and Disability Servicing.Number of cases rejected by fulfiller**

    Number of the closed cases in the last 30 days that were rejected by a processor or underwriter.


## Breakdowns

-   Individual Case Stage
-   Individual Life Rejection Reason
-   Individual Life Service

**Parent Topic:**[Implementing Platform Analytics solutions](../../application-content-packs/concept/fso-content-pack.md)

