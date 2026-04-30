---
title: Group Life Servicing dashboard
description: With the Group Life Servicing dashboard, you can get an insight into how your team and business are performing for the group policy service requests that were received for your insurance services.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Analytics and reporting for Group Life Servicing, Group Life Servicing, Life Insurance Servicing, Insurance applications, Financial Services Operations \(FSO\)]
---

# Group Life Servicing dashboard

With the Group Life Servicing dashboard, you can get an insight into how your team and business are performing for the group policy service requests that were received for your insurance services.

**Important:** The Group Life Servicing dashboard has been modernized to give you a better user experience.

The Group Life Servicing dashboard enables you to monitor the status of the policy service cases, see trends, and drill down into the details from a single view. For any time that you specify, you can view the details for the closed cases that breached an SLA, the open cases that need immediate attention, and the average closing times of the policy service cases.

## Required ServiceNow AI Platform roles

-   sn\_ins\_group\_life.manager, required to view the dashboard widgets and data.
-   sn\_ins\_group\_life.admin, sn\_bom\_pa.admin, and pa\_admin, required to edit the dashboard.

## Access the Group Life Servicing dashboard

To access the Group Life Servicing dashboard, navigate to **Workspaces** &gt; **Financial Services Workspace** &gt; **Analytics Center** \(![Analytics center icon.](../../../product/fso-personal-lines-claims/image/analytics-center-icon.png)\).

Alternatively, you can navigate to **All** &gt; **Group Life Servicing** &gt; **Analytics**.

You can also access the dashboard from the Platform Analytics Workspace. For more information about the Platform Analytics Workspace, see [Analytics Center](https://www.servicenow.com/docs/access?context=analytics-center&version=xanadu&pubname=xanadu-now-intelligence&ft:locale=en-US).

If you have upgraded from an earlier version, you can access the existing Core UI dashboard layout as usual by navigating to **All** &gt; **Group Life Servicing** &gt; **Dashboard**.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Group life policy manager

</td><td>

Needs to gain visibility into the real-time status of the insurance cases and do the following tasks:-   Monitor all the open insurance cases that have breached an SLA \(Service Level Agreement\)
-   Monitor the volume of each insurance case type and their trend
-   Review agent productivity
-   Review the average closing time of cases for a service, agent, or group
-   Monitor the details of requests by the policy type
-   Drill down into the details in an error category

</td></tr><tr><td>

Group life policy admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **Group Life and Disability Servicing.Summed duration of closed cases**

    Number of hours to close the personal lines cases that day with the Stage and Service breakdowns.

-   **Group Life and Disability Servicing.Number of closed cases**

    Number of the group life cases that were closed today with the Stage and Service breakdowns.

-   **Group Life and Disability Servicing.Open Cases with SLA Breached greater than 80%**

    Number of the open group life cases that day where the SLA-elapsed percentage is greater than 80 percent.

-   **Group Life and Disability Servicing.Group life change member info**

    Number of group life cases where the policy service is changing member information.

-   **Group Life and Disability Servicing.Number of closed cases with breached sla**

    Number of the group life cases that were closed that day that breached an SLA.

-   **Group Life and Disability Servicing.Number of open cases breached SLA**

    Number of the open group life cases that day that breached an SLA.

-   **Group Life and Disability Servicing.Number of open cases**

    Number of the open group life cases that day.

-   **Group Life and Disability Servicing.Number of cases rejected by customer**

    Number of the closed cases that were rejected by customers in the last 30 days, where the solution proposed by the agent was rejected.

-   **Group Life and Disability Servicing.Number of closed cases with sla**

    Number of the group life cases that were closed that day within an SLA. The indicator is used to compare the number of cases that were closed that met an SLA versus the cases that breached an SLA.

-   **Group Life and Disability Servicing.Number of cases rejected by fulfiller**

    Number of the closed cases in the last 30 days that were rejected by a processor or underwriter.

-   **Group Life and Disability Servicing.Group life send policy documents**

    Number of the group life cases where the policy service is sending policy documents.

-   **Group Life and Disability Servicing.Group life update policy**

    Number of the group life cases where the policy service is updating a policy.


## Breakdowns

-   Group Case Stage
-   Group Life Rejection Reason
-   Group Life Service

**Parent Topic:**[Platform Analytics Solutions for Financial Services Operations](../../application-content-packs/concept/fso-content-pack.md)

