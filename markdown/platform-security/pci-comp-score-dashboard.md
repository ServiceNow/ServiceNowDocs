---
title: PCI compliance score dashboard
description: The PCI compliance score dashboard shows how your instance conforms to payment card industry \(PCI\) security standards. Use the dashboard to view your compliance score and modify your configuration to improve security.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Check the daily compliance score and configure security property settings, Instance Security Center, Platform Security]
---

# PCI compliance score dashboard

The PCI compliance score dashboard shows how your instance conforms to payment card industry \(PCI\) security standards. Use the dashboard to view your compliance score and modify your configuration to improve security.

![PCI compliance score dashboard with sample values](../image/pci-comp-dash.png)

## Required ServiceNow AI Platform roles

security\_dashboard\_user or admin, needed to view the PCI compliance score dashboard.

## Access the PCI compliance score dashboard

To open the dashboard, navigate to **System Security** &gt; **Instance Security Center**. From the instance security center, click **Compliance Scores** in the header, then select **PCI Compliance Score**.

## Use cases

For examples of how different people in your organization would use this dashboard, see these use cases.

|User|Dashboard use|
|----|-------------|
|Security dashboard user \(security\_dashboard\_user\)|Continually monitor and manage instance security compliance.|
|Admin \(admin\)|Continually monitor instance security compliance to detect and respond to security threats.|

## Indicators

|Indicator|Description|
|---------|-----------|
|PCI Compliance Score|Displays your instance's compliance score as a percentage. This percentage of represents the percentage of security configurations on your instance that meet compliance standards. The indicator also displays the date the compliance score was calculated, and a comparison with the previous calculated score.|

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

PCI Compliance

</td><td>

![Stacked bar chart](../../../reuse/reporting/image/bar-stacked.svg) Stacked bar chart

</td><td>

Security Configurations \[isc\_security\_configurations\]

</td><td>

Displays compliant and non-compliant security configurations in high, medium, and low categories. Click an area of the report to display the matching security configurations.

</td></tr></tbody>
</table>**Parent Topic:**[Check the daily compliance score and configure security property settings](../../../administer/security/concept/instance-sec-center-hardening.md)

