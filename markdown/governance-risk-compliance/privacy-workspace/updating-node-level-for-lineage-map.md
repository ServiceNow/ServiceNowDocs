---
title: Update the maximum node level for the lineage map
description: Update the sn\_privacy.nodemap.maxLevel system property to control how many node levels are visible on the lineage map.
locale: en-US
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 1
breadcrumb: [Create a lineage for a processing activity, Use, Privacy Management, Governance, Risk, and Compliance]
---

# Update the maximum node level for the lineage map

Update the `sn_privacy.nodemap.maxLevel system` property to control how many node levels are visible on the lineage map.

## Before you begin

Role required: System admin or Privacy admin

## About this task

By default, the lineage map displays nodes up to five levels downstream and one level upstream from the primary processing activity record. If your data lineage spans more than five downstream levels, you can increase this limit by updating the `sn_privacy.nodemap.maxLevel` system property. The upstream display is always limited to one level and is not affected by this property.

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  In the Name field, search for `sn_privacy.nodemap.maxLevel`.

3.  Open the `sn_privacy.nodemap.maxLevel` property record.

4.  In the Value field, enter the maximum number of node levels to display.

5.  Select **Update**.


**Parent Topic:**[Create a lineage for a processing activity](create-a-data-lineage-for-a-processing-activity.md)

