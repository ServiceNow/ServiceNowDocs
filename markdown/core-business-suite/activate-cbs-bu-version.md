---
title: Enable Core Business Suite Foundation business units
description: If you’re using any standard business unit included in Core Business Suite Foundation, update the system properties to enable the Core Business Suite business units for installation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-04-06"
reading_time_minutes: 1
breadcrumb: [Configure, Core Business Suite]
---

# Enable Core Business Suite Foundation business units

If you’re using any standard business unit included in Core Business Suite Foundation, update the system properties to enable the Core Business Suite business units for installation.

## Before you begin

**Note:**

-   If you are already using a standard business unit such as Human Resources, Finance, Health and Safety, Legal, Workplace Services, or Source‑to‑Pay that is included in Core Business Suite Foundation, the Core Business Suite business unit does not appear in the installation section.
-   After you update the required system properties, the Core Business Suite business unit appears in the installation section.
-   After you install a Core Business Suite business unit and apply the default configurations, the existing business unit customizations such as notifications and intake forms are overridden.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the name column, search for **\*cbs**.

    The search lists all Core Business Suite business unit system properties records:

    -   `sn_cbs.override_WSD_tile`
    -   `sn_cbs.override_HEALTH_tile`
    -   `sn_cbs.override_FINANCE_tile`
    -   `sn_cbs.override_HR_tile`
    -   `sn_cbs.override_LEGAL_tile`
    -   `sn_cbs.override_S2P_tile`
3.  Select the system property record for the required business unit.

4.  In the notification bar, select **here** to edit the record in the Core Business Suite application.

5.  Set the value field to **true**.

6.  Select **Update**.


## Result

The Core Business Suite business unit appears in the installation section.

**Parent Topic:**[Configure Core Business Suite Foundation](../concept/configure-cbs.md)

