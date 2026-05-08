---
title: Create SLOs, SLIs, and error budget policies
description: Define service level objectives \(SLOs\), service level indicators \(SLIs\), and error budget policies to monitor service health. These tools help you and your teams track performance and respond when needed.
locale: en-US
release: australia
product: Service Level Objective Management
classification: service-level-objective-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using SLO Management, Service Level Objective Management, ITOM AIOps, IT Operations Management]
---

# Create SLOs, SLIs, and error budget policies

Define service level objectives \(SLOs\), service level indicators \(SLIs\), and error budget policies to monitor service health. These tools help you and your teams track performance and respond when needed.

## Before you begin

To send notifications when an error budget policy is breached, your team must have a notification destination configured. You can check by navigating to **Teams** &gt; **\[Your team\]** &gt; **SLO Notification destinations** in Service Operations Workspace. For more information, see [Create a notification destination in SRM](create-notification-destination.md).

**Note:** By default, the outage data source for SLIs includes unplanned and degradation outages. Administrators can include planned outages by adding `planned` to the `sn_sow_slo.outage_supported_types` system property value.

Role required: srm\_admin, srm\_manager, or srm\_responder

## About this task

Create SLOs, SLIs, and error budget policies to monitor service health and help make sure that your services support business goals.

In Service Reliability Management \(SRM\), an SLO must have at least one SLI. SLIs can be filtered to a service or configuration item \(CI\) within the parent service hierarchy. Filtering an SLI to a CI can help you more accurately track service health and identify root causes faster.

Each SLI can be associated with only one SLO, helping prevent conflicting performance expectations.

**Note:** SLOs can also be generated automatically using the SLO creator agent. For details, see [Generating service level objectives](../../now-assist-itom/concept/now-assist-itom-slo-generation.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** &gt; **Services \(![Services icon](../../service-reliability/image/icon-sr-services.png)\)**.

2.  On the **Services** page, select the service you want to monitor, then select the **Reliability metrics** tab and select **Add SLO &amp; SLI**.

3.  In the Service Level Objective \(SLO\) form, fill in the fields for your SLOand select **Next**.

    For information about the SLO fields, see [Create SLO form](../../service-reliability/reference/sr-create-slo-sli-form.md).

4.  In the Service Level Indicators \(SLI\) form, select the data source for your SLI.

<table id="choicetable_bsn_r5m_dhc"><thead><tr><th align="left" id="d373960e184">

Data source

</th><th align="left" id="d373960e187">

Description

</th></tr></thead><tbody><tr><td id="d373960e193">

**Alerts**

</td><td>

Base the SLI on alerts from integrated monitoring tools.Use alerts when you want your SLI to include early warning signs and a broader view of reliability.

</td></tr><tr><td id="d373960e204">

**Outages**

</td><td>

Base the SLI on outages detected by monitoring tools and reported by users.Use outages when you want to measure actual downtime and customer impact.

</td></tr></tbody>
</table>    **Note:** If you create multiple SLIs for an SLO, they must use the same data source.

5.  In the same form, select **Add indicators for &lt;data source&gt;**, fill in the fields for your SLI, and then select **Next**.

    For more information about the SLI fields, see [Create SLI form](../../service-reliability/reference/sr-create-sli-form.md).

6.  In the Error budget policies form, select **Add policy**, and fill in the fields for your error budget policy.

    For more information, see [Add an error budget policy form](../reference/sr-create-error-budget-form.md).

    **Note:** If you don't add an error budget policy, the SLO objective percentage is only informational. Adding a policy helps you take corrective actions based on the performance data. If you're not ready to add a policy, you can add one later.

7.  Review your SLO, SLI, and error budget policy, and then select **Activate**.

    Your SLO, SLI, and error budget policy are now active. The SLO record opens, displaying its reliability state and error budget information.


## What to do next

See the following to learn how to monitor and manage your SLOs:

-   [Working with reliability metrics](../concept/sr-work-SLI-SLO.md) - Learn where and how to view SLO performance.
-   [Edit a reliability metric](sr-edit-sli-slo.md) - Update your SLOs to keep them aligned with your reliability goals.

**Parent Topic:**[Using SLO Management](using-service-level-objective-management.md)

