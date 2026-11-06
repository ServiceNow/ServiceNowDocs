---
title: Exclude software assets on CIs
description: Exclude specific configuration items \(CIs\) from Software Asset Management when you don’t need to track license compliance for them, such as third-party leased devices. This lets you scope compliance calculations to only the CIs you choose, and expand that scope later as needed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/software-asset-management/exclude-software-assets-cis.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2026-10-19"
reading_time_minutes: 2
keywords: [exclude software, configuration items, CIs, Exclude from SAM, hardware, license compliance]
breadcrumb: [License exclusions, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Exclude software assets on CIs

Exclude specific configuration items \(CIs\) from Software Asset Management when you don’t need to track license compliance for them, such as third-party leased devices. This lets you scope compliance calculations to only the CIs you choose, and expand that scope later as needed.

## Before you begin

Role required: sam\_admin

## About this task

There may be cases where you don’t want certain CIs included in software license compliance tracking. For example, some devices may be leased from a third party, so your organization isn’t responsible for license compliance on the software installed on them. Or, you may want to roll out Software Asset Management gradually, starting with devices at a specific location, such as the New York office, before expanding to other locations.

To handle these cases, specify CIs to exclude in the Software Asset Management application. After you exclude, the system leaves out any software installed on those CIs when calculating license compliance.

## Procedure

1.  In the Hardware \[cmdb\_ci\_hardware\] table, add a true or false \(Boolean\) column to exclude a CI from SAM.

    For example, Exclude from SAM \[u\_exclude\_from\_sam\].

2.  Set the value of the **Exclude from SAM** column to true for devices for which you don't need to manage installed software in the application.

    **Note:** The default value of the **Exclude from SAM** column is **false**. By default, the system manages installed software on all devices.

3.  Navigate to **Software Asset** &gt; **Administration** &gt; **Properties**.

4.  Enter the column name, `u_exclude_from_sam`, in the field next to the property **Enter the name of the true/false field added to cmdb\_ci\_hardware table to exclude software installed on selected devices from Software Asset Management**.

    After the scheduled job **SAM — Adjust Installs for excluded CIs** runs, the system excludes software installed on devices with the **Exclude from SAM** column set to **true**.

5.  Set the value of the **Exclude from SAM** column for the device to **false**.

    After the scheduled job **SAM — Adjust Installs for excluded CIs** runs, the system starts managing software installs on these devices.

6.  Complete the following steps to start managing software installs on all previously excluded devices.

    1.  Navigate to **Software Asset** &gt; **Administration** &gt; **Properties**.

    2.  Delete the column name \[u\_exclude\_from\_sam\] from the **Enter the name of the true/false field added to cmdb\_ci\_hardware table to exclude software installed on selected devices from Software Asset Management** property.

    3.  Select **Save**.

        After the scheduled job **SAM — Adjust Installs for excluded CIs** runs, the system starts managing the software installed on all previously excluded devices.


**Parent Topic:**[License exclusions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/software-asset-management/software-asset-management-license-exclusions.md)

