---
title: Review skipped records with upgrade plan
description: Review the skipped records after the completion of the upgrade.
locale: en-US
release: zurich
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Apply Upgrade Plan on your upgrade, Upgrade Plans tool in Upgrade Console, Upgrade Console tools, Use, Upgrade Console, Upgrade, Administer]
---

# Review skipped records with upgrade plan

Review the skipped records after the completion of the upgrade.

## Before you begin

**Note:** This process is applicable only if you have enabled the GLIDE\_UPGRADE\_PLAN\_INCLUDE\_SKIPS property.

Role required: admin

## Procedure

1.  Once the upgrade completes, scroll down to see the skipped records with upgrade plan.

    -   Total: Total number of skipped records
    -   Resolved: Total records from the upgrade plan that have been auto-resolved
    -   To review: Total records left to be reviewed manually
    **Note:** After using the upgrade plan, the Global Application is created and all the records move to the Global Application. As soon as you create the Global Application, the new update sets show up.

    You won’t be allowed to choose the skipped records that are captured by the upgrade plan, regardless of whether they are being reviewed. If the customizations are coming from different instances, then the skipped records are required to be reviewed.

2.  Select the To review link to look at the records that need to be reviewed manually.


**Parent Topic:**[Apply Upgrade Plan on your upgrade](um-apply-upgrade-plan.md)

