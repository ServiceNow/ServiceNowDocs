---
title: MFA metrics dashboard
description: The MFA metrics dashboard shows information on your instances multi-factor authentication configuration. Use the dashboard to ensure your MFA configuration meets your security standards.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Monitor instance metrics, Instance Security Center, Platform Security]
---

# MFA metrics dashboard

The MFA metrics dashboard shows information on your instances multi-factor authentication configuration. Use the dashboard to ensure your MFA configuration meets your security standards.

## Required ServiceNow AI Platform roles

security\_dashboard\_user or admin, needed to view the PCI compliance score dashboard.

## Access the MFA metrics dashboard

To open the dashboard, navigate to **System Security** &gt; **Instance Security Center**. From the instance security center, click **Metrics** in the header, then select **MFA Metrics**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|Security dashboard user \(security\_dashboard\_user\)|Continually monitor and manage instance security compliance.|
|Admin \(admin\)|Continually monitor instance security compliance to detect and respond to security threats.|

## Indicators

-   **Users Enrolled for MFA**

    Displays the total number of users on the instance enrolled in MFA . Click to open the Analytics hub for more detail.

-   **Users using MFA Bypass**

    Displays the total number of users using MFA bypass . Click to open the Analytics hub for more detail.


## Data visualizations

<table id="table_tj5_png_mrb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

High Privilege MFA Users

</td><td>

Bar![Bar chart](../../../reuse/reporting/image/bars-total.svg)

</td><td>



</td><td>



</td></tr><tr><td>

MFA User Trend

</td><td>

![Trend chart](../../../reuse/reporting/image/trend.svg) Trend

</td><td>

 

</td><td>

 

</td></tr></tbody>
</table>**Parent Topic:**[Monitor instance metrics](../../../administer/security/concept/monitoring-user-email-antivirus-metrics.md)

