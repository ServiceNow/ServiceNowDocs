---
title: Create a custom Common Platform Enumeration \(CPE\) mapping for firmware in your operational technology \(OT\) assets
description: If the CPE mapping for firmware that is embedded into your OT assets isn't already represented in the Enterprise Asset Management Content Service, create a custom CPE mapping.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Normalizing firmware for OT assets, Managing enterprise models and assets, Enterprise Asset Management, IT Asset Management]
---

# Create a custom Common Platform Enumeration \(CPE\) mapping for firmware in your operational technology \(OT\) assets

If the CPE mapping for firmware that is embedded into your OT assets isn't already represented in the Enterprise Asset Management Content Service, create a custom CPE mapping.

## Before you begin

**Important:** You can create custom CPE mappings only using the OT Asset Workspace. To use the OT Asset Workspace, install the OT Asset Management application on your ServiceNow instance. See [Install OT Asset Management](install-otam.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin

## About this task

CPE is a standardized naming scheme that enables you to map your information technology \(IT\) systems, software, and packages to corresponding vulnerability management data in the National Vulnerability Database \(NVD\). You can use these mappings to identify and mitigate potential vulnerabilities across your IT infrastructure. All official CPE names are listed in the CPE Product Dictionary, which is hosted and maintained by the National Institute of Standards and Technology \(NIST\).

## Procedure

1.  Navigate to **All** &gt; **OT Asset Workspace** &gt; **Normalization**.

2.  Select the **Custom firmware CPE** tab.

3.  Select **New**.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Firmware product|Firmware product that you want to map to vulnerability management data in the NVD.|
    |Firmware version|Version of the firmware product that you want to map to vulnerability management data in the NVD.|
    |CPE publisher|Publisher of the firmware product, as listed in the CPE Product Dictionary.|
    |CPE product|Name of the firmware product, as listed in the CPE Product Dictionary.|
    |CPE version|Version of the firmware product, as listed in the CPE Product Dictionary.|

5.  Select **Save**.


