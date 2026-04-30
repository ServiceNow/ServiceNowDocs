---
title: Downgrade a license using the legacy Software Asset Management plugin
description: Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to downgrade a software license through one of two methods: through a software model record or through a software license record.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [License upgrade and downgrade with the legacy Software Asset Management plugin, Software licenses in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Downgrade a license using the legacy Software Asset Management plugin

Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to downgrade a software license through one of two methods: through a software model record or through a software license record.

## Before you begin

Role required: sam

## About this task

**Note:** Downgrade children set on the software license applies specifically to that license. If a downgrade child is set on the software model, it applies to all licenses of that model.

## Procedure

1.  Complete the following steps to downgrade a license from a software model record.

    1.  Navigate to **Software Asset** &gt; **Software Models**.

    2.  Select a model.

    3.  In the **Downgrade** section, double-click under the **Downgrade child** column heading.

    4.  Select a software model from the list.

    5.  Click the green check mark.

2.  Complete the following steps to downgrade a license from a software license record.

    1.  Navigate to **Software Asset** &gt; **Software Licenses**.

    2.  Select a license.

    3.  Click **New** in the Software Upgrade and Downgrades related list.

    4.  Select a software model from the list.

    5.  Select the **Start** and **End** dates.

    6.  Click **Submit**.


-   **[Identify a downgrade child from a software license record using the legacy Software Asset Management plugin](t_IdentifyADGChildFromASWLicRec.md)**  
Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to identify a downgrade child from a software license record.

**Parent Topic:**[License upgrade and downgrade with the legacy Software Asset Management plugin](../concept/c_UpgradingAndDowngradingLicenses.md)

