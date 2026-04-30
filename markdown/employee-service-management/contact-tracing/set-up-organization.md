---
title: Create an organization and load sites
description: Create an organization for which you are collecting the Wi-Fi access logs using Mist Systems. After you have created an organization, load sites using a scheduled job.
locale: en-US
release: xanadu
product: Contact Tracing
classification: contact-tracing
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Retrieving Wi-Fi access log data, Contact Tracing, Safe Workplace, Health and Safety, Employee Service Management]
---

# Create an organization and load sites

Create an organization for which you are collecting the Wi-Fi access logs using Mist Systems. After you have created an organization, load sites using a scheduled job.

## Before you begin

Role required: sn\_imt\_tracing.wifi\_admin

## About this task

Each floor in the organization can be considered as a site. Each site can be further divided into zones. Each zone can have multiple Wi-Fi access points.

## Procedure

1.  Navigate to **All** &gt; **Contact Tracing** &gt; **Mist Systems** &gt; **Organizations**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the organization.|
    |Organization Id|Unique ID of the organization. You must have the network admin role to get the organization ID. For more information, see the [Mist Systems documentation](https://www.mist.com/documentation/find-org-site-id/).|
    |Active|Option for marking the availability status of the organization. If the organization is removed, clear this check box.|
    |Vendor|Mist Systems|
    |API token|API token that is generated for the organization. You must have the network admin role to get the API token. For more information, see the [Mist Systems documentation](https://www.mist.com/documentation/using-postman/).|

4.  Click **Submit**.

5.  Click **Load Sites**.

    The sites of the organization are fetched from the Mist Systems and displayed in the **Sites** related list. Later, the **Load Mist Sites** scheduled job runs at the configured time and updates the sites list for each of the organizations.

    The **BLE enabled** option helps you to identify potentially infected employees from the Wi-Fi access logs by correlating everyone who connected to the Wi-Fi network using Bluetooth LE devices. If a site is BLE enabled, the **BLE enabled** check box on the Sites form is selected.


**Parent Topic:**[Retrieving Wi-Fi access log data](../concept/wifi-access-management.md)

