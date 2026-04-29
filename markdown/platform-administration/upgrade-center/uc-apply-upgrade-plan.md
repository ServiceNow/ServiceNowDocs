---
title: Apply Upgrade Plan on your upgrade
description: Apply the selected upgrade plan to your instance upgrade.
locale: en-US
release: australia
product: Upgrade Center
classification: upgrade-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Preparing your upgrade plan, Using Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Apply Upgrade Plan on your upgrade

Apply the selected upgrade plan to your instance upgrade.

## Before you begin

Role required: admin

## Procedure

1.  Go to the Upgrade Monitor page to ensure that the selected upgrade plan is being implemented in your upgrade.

    If the upgrade plan has been implemented on the ongoing upgrade, the Review upgrade plan link shows up on the Target version card.

    See Upgrade Plan background operations section in [Upgrade Plan overview](../concept/uc-upgrade-plan.md) for more information.

2.  Check on the date and time of the implemented upgrade plan in the Upgrade duration card once the upgrade completes.

    You can select the Review upgrade plan link on the Upgrade duration card to know the history of the upgrade plan. It shows all the installed applications and plugins and the failed items.

3.  Scroll down to see the skipped records with upgrade plan.

    -   Total: Total number of skipped records
    -   Resolved: Total records from the upgrade plan that have been auto-resolved
    -   To review: Total records left to be reviewed manually
    **Note:** This step is applicable only if you have enabled the GLIDE\_UPGRADE\_PLAN\_INCLUDE\_SKIPS property.

4.  Click **Review upgrade plan** on the Upgrade duration card if you want to check the summary of your upgrade plan history.

    ![Upgrade Plan History screen.](../image/uc-upgrade-plan-history.png)


-   **[Review skipped records with upgrade plan](uc-review-skipped-records-upgrade-plan.md)**  
Review the skipped records after the completion of the upgrade.

**Parent Topic:**[Preparing your upgrade plan](../concept/uc-prepare-up.md)

**Related topics**  


[Building your Upgrade Plan](uc-building-upgrade-plan.md)

[Refreshing your Upgrade Plan](uc-refreshing-upgrade-plan.md)

[Installing your Upgrade Plan](uc-installing-upgrade-plan.md)

[Prepare to upgrade with Upgrade Plan](uc-prepare-upgrade-plan.md)

