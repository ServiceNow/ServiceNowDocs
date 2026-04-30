---
title: Upgrade a license using the legacy Software Asset Management plugin
description: Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to upgrade a software license through one of two methods: through a software license record or through a software model record.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [License upgrade and downgrade with the legacy Software Asset Management plugin, Software licenses in the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Upgrade a license using the legacy Software Asset Management plugin

Use the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin to upgrade a software license through one of two methods: through a software license record or through a software model record.

## Before you begin

Role required: sam

## Procedure

1.  Complete the following steps to identify an upgrade parent from a software license record.

    1.  Navigate to **Software Asset** &gt; **Software Licenses** and select a software license.

    2.  Click the **Software Upgrade and Downgrade** tab and click **New**.

    3.  Complete the form.

        |Field|Description|
        |-----|-----------|
        |License|Name and asset number of the software license.|
        |Downgrade Child|Lower version of the software license.|
        |Upgrade parent|Higher version of the software license.|
        |Start date|Start date of the upgrade.|
        |End date|End date of the upgrade.|

    4.  Click **Submit**.

        The software upgrade displays in the Software Upgrade and Downgrades section.

    5.  Select the software upgrade check box and click **Update**.

        The software license is updated in the Software License list.

2.  Complete the following steps to identify an upgrade parent from a software model record.

    1.  Navigate to **Software Asset** &gt; **Software Models**.

    2.  Select a model.

    3.  In the **Upgrade** section, double-click under the **Upgrade parent** column heading.

    4.  Select a software model from the list.

    5.  Click the green check mark and click **Update**.

        The Software Model form is updated.


**Parent Topic:**[License upgrade and downgrade with the legacy Software Asset Management plugin](../concept/c_UpgradingAndDowngradingLicenses.md)

