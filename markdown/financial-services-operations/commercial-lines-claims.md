---
title: Commercial Lines Claims dashboard
description: With the Commercial Lines Claims dashboard, you can get an insight into how your team and business are performing for the personal policy service requests that were received for your insurance services.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Platform Analytics, Financial Services Operations \(FSO\)]
---

# Commercial Lines Claims dashboard

With the Commercial Lines Claims dashboard, you can get an insight into how your team and business are performing for the personal policy service requests that were received for your insurance services.

The Commercial Lines Claims dashboard enables you to monitor the status of the claim cases, see trends, and drill down into the details from a single view. For any time that you specify, you can view the details for the closed cases that breached an SLA, the open cases that need immediate attention, and the average closing times of the claim cases.

To access the Commercial Lines Claims dashboard, navigate to **All** &gt; **Commercial Lines Claims** &gt; **Dashboard**.

## Required ServiceNow AI Platform roles

-   sn\_ins\_claim\_cml.manager, required to view the dashboard widgets and data.
-   sn\_ins\_claim\_cml.admin, sn\_bom\_pa.admin, and pa\_admin, required to edit the dashboard.

## Use cases

For examples of how different people in your organization can use this dashboard, see the use cases in the following table.

<table><thead><tr><th>

User

</th><th>

Dashboard use

</th></tr></thead><tbody><tr><td>

Commercial lines claims manager

</td><td>

Needs to gain visibility into the real-time status of the claim cases and do the following tasks:-   Monitor all the open claim cases that have breached a Service Level Agreement \(SLA\)
-   Monitor the volume of each claim case type and their trend
-   Review the average closing time of the cases for a representative, processor, or group

</td></tr><tr><td>

Commercial lines claims admin

</td><td>

Needs to be able to customize views.

</td></tr></tbody>
</table>## Indicators

-   **Commercial Claim.Number of denied cases**

    Number of the commercial claim cases that were rejected and closed today.

-   **Commercial Claim.Number of open cases**

    Daily number of the open commercial claim cases.

-   **Commercial Claim.Summed duration of closed cases**

    Number of hours to close the commercial claim cases that day with Stage and Service breakdowns.

-   **Commercial Claim.Number of closed cases**

    Number of the commercial claim cases that were closed today with Stage and Service breakdowns.

-   **Commercial Claim.Open Cases with SLA Breached greater than 80%**

    Number of the open commercial claim cases that day where an SLA-elapsed percentage is greater than 80 percent.

-   **Commercial Claim.Number of closed SIU cases**

    Daily number of the commercial claim cases that were closed by the special investigations unit \(SIU\).

-   **Commercial Claim.Sum of total claim payout**

    Daily number of the claim payout on the closed cases.

-   **Commercial Claim.Number of closed cases with breached sla**

    Number of the commercial claim cases that were closed that day that breached an SLA.

-   **Commercial Claim:Number of created cases**

    Number of the open commercial claims cases that were created that day.

-   **Commercial lines.Number of bop change coverage open cases**

    Number of the open commercial claim cases that day where the commercial service is a bop change coverage account.

-   **Commercial Claim.Number of closed cases within sla**

    Number of the commercial claim cases that were closed that day within an SLA. The indicator is used to compare the number of cases that were closed that met an SLA versus the number of cases that breached an SLA.


## Breakdowns

-   SLA percentage
-   Commercial Claim.Age
-   Commercial Claim.Account
-   Commercial Claim.Product
-   Commercial Claim.Service
-   Commercial Claim.Stage

**Parent Topic:**[Implementing Platform Analytics solutions](../../application-content-packs/concept/fso-content-pack.md)

