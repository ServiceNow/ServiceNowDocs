---
title: Retarget a release
description: Change the release readiness target to reschedule the release period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-product-release/dpr-work-release-readiness-target.html
release: australia
product: Digital Product Release
classification: digital-product-release
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Manage releases for digital products and services, Use, Digital Product Release, IT Service Management]
---

# Retarget a release

Change the release readiness target to reschedule the release period.

## Before you begin

Role required: sn\_dpr\_model.product\_manager or sn\_dpr\_model.release\_admin

## About this task

The available release targets and the **Out of band** check box depend on the following conditions:

The **Release readiness target** lists target dates based on the product-level release setting.

|Condition|Filtered targets|All targets|
|---------|----------------|-----------|
|Product has release calendars defined in the release settings and targets are linked to those calendars.|✓|✗|
|Product has release calendars defined in the release settings but no targets are linked to those calendars.|✗|✓|
|Product doesn't have release settings configured.|✗|✓|

The visibility of the **Out of band** check box depends on product-level release settings or two system properties.

|Condition|Visible|Hidden|
|---------|-------|------|
|**Release readiness dates** is toggled on in product-level release settings.|✓|✗|
|**Release readiness dates** is toggled off in product-level release settings.|✗|✓|
|Product doesn't have release settings configured and the **sn\_dpr.out\_of\_band\_release\_allowed** system property is **true**.|✓|✗|
|Product doesn't have release settings configured and the **sn\_dpr.out\_of\_band\_release\_allowed** system property is **false**.|✗|✓|
|You don't have any of the roles defined in the **sn\_dpr.out\_of\_band\_release\_roles** system property.|✗|✓|

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Product Release Workspace**.

2.  Select the releases icon \(\[Omitted image "dpr-icon-release.png"\] Alt text: Releases icon.\).

3.  Select a release from the list to open.

4.  On the Release form, select **Overview**.

5.  Select the release action icon \(\[Omitted image "icon-actions-menu.png"\] Alt text: Release action icon.\) and then select **Retarget release**.

    **Note:** Release readiness target and Release target are used interchangeably. Both terms refer to the same concept - release readiness target date.

6.  On the Retarget release dialog box, select a different release readiness target from **Release readiness target**.

    **Note:** The new release readiness target date must be within the defined schedule of the release.

7.  You can also make the release as an out-of-band release by selecting **Out of band**.

8.  If you selected the out-of-band option, then select a release calendar from the **Release calendar** to tag the release and use its release target.

9.  Select **Confirm**.


## Result

-   The readiness target date of the release is updated to the new date.
-   For timeline-oriented releases, the key dates impacted are adjusted based on the retargeted date. This adjustment is made after recalculating the number of days that have changed from the original schedule.

    **Note:** If a holiday schedule is attached to the release and the revised key dates fall on a holiday, the last workday before the holiday is considered as the revised key date.


## What to do next

Update the planned dates on the associated change requests manually because they are not automatically updated when you retarget the release.

**Parent Topic:**[Manage releases for digital products and services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-product-release/dpr-manage-releases.md)

**Related topics**  


[Digital Product Release - PUT /sn\_dpr/digital\_product\_release/release/\{sysId\}/retarget](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/api-reference/rest-apis/digital-product-release-api.md)

