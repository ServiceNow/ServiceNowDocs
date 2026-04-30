---
title: PCI configuration controls score dashboard
description: Use the PCI configuration controls score dashboard to review your PCI configuration and determine which security checks are non-compliant. You can change the configuration of the non-compliant security checks from the instance security center.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Check the daily compliance score and configure security property settings, Instance Security Center, Platform Security]
---

# PCI configuration controls score dashboard

Use the PCI configuration controls score dashboard to review your PCI configuration and determine which security checks are non-compliant. You can change the configuration of the non-compliant security checks from the instance security center.

![PCI compliance score dashboard with sample values](../image/pci-config-control-score.png)

## Required ServiceNow AI Platform roles

The security\_dashboard\_user or admin role is required to view the PCI compliance score dashboard.

## Access the PCI configuration controls score dashboard

To open the dashboard, navigate to **System Security** &gt; **Instance Security Center**. From the instance security center, click **Compliance Scores** in the header, then select **PCI Configuration Controls Score**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|Security dashboard user \(security\_dashboard\_user\)|Continually monitor and manage PCI configuration controls compliance on your instance. Modify PCI configuration to ensure compliance and improve instance security.|
|Admin \(admin\)|Continually monitor PCI configuration controls compliance to detect and respond to potential security threats.|

## Indicators

-   **PCI Configuration Controls Score**

    Displays your instance's PCI configuration controls score as a percentage. This percentage of represents the percentage of security PCI control configurations on your instance that meet compliance standards. The indicator also displays the date the compliance score was calculated, and a comparison with the previous calculated score.


## Data visualization

<table id="table_tj5_png_mrb"><thead><tr><th>

Title

</th><th>

Type

</th><th>

Source table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

PCI Configuration Controls

</td><td>

![Stacked bar chart](../../../reuse/reporting/image/bar-stacked.svg) Stacked bar chart

</td><td>

Security Configurations \[isc\_security\_configurations\]

</td><td>

Displays compliant and non-compliant PCI control configurations in high, medium, and low categories. Click an area of the report to display the matching security configurations.

</td></tr></tbody>
</table>**Parent Topic:**[Check the daily compliance score and configure security property settings](../../../administer/security/concept/instance-sec-center-hardening.md)

