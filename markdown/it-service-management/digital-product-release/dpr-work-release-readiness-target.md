---
title: Retarget a release
description: Change the release readiness target to reschedule the release period.
locale: en-US
release: zurich
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Retarget a release

Change the release readiness target to reschedule the release period.

## Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(![Releases icon.](../image/dpr-icon-release.png)\).

3.  Select a release from the list to open.

4.  On the Release form, select **Overview**.

5.  Select the release action icon \(![Release action icon.](../../site-reliability-ops/image/icon-actions-menu.png)\) and then select **Retarget release**.

    **Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

6.  On the Retarget release dialog box, select a different release readiness target from **Release readiness target**.

    **Note:** The new release readiness target date must be within the defined schedule of the release.

7.  You can also make the release as an out-of-band release by selecting **Out of band**.

    This option depends on the system properties—**out\_of\_band\_release\_allowed** and **out\_of\_band\_release\_roles**. For more information, see [Digital Product Release properties](../reference/digital-product-release-properties.md).

8.  If you selected the out-of-band option, then select a release calendar from the **Release calendar** to tag the release and use its release target.

9.  Select **Confirm**.


## Result

-   The readiness target date of the release is updated to the new date.
-   For timeline-oriented releases, the key dates impacted are adjusted based on the retargeted date. This adjustment is made after recalculating the number of days that have changed from the original schedule.

    **Note:** If a holiday schedule is attached to the release and the revised key dates fall on a holiday, the last workday before the holiday is considered as the revised key date.


## What to do next

Update the planned dates on the associated change requests manually because they are not automatically updated when you retarget the release.

**Parent Topic:**[Manage releases for digital products and services](dpr-manage-releases.md)

