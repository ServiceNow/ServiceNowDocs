---
title: Apply Upgrade Plan on your upgrade
description: Apply the selected upgrade plan to your instance upgrade.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/upgrade-management/um-apply-upgrade-plan.html
release: australia
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Upgrade Plans tool in Upgrade Console, Upgrade Console tools, Use, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Apply Upgrade Plan on your upgrade

Apply the selected upgrade plan to your instance upgrade.

## Before you begin

Role required: admin

## Procedure

1.  Go to the Upgrade Monitor page to ensure that the selected upgrade plan is being implemented in your upgrade.

    If the upgrade plan has been implemented on the ongoing upgrade, the Review upgrade plan link shows up on the Target version card.

    See Upgrade Plan background operations section in [Upgrade Plans tool in Upgrade Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-upgrade-plans-tool.md) for more information.

2.  Check on the date and time of the implemented upgrade plan in the Upgrade duration card once the upgrade completes.

    You can select the Review upgrade plan link on the Upgrade duration card to know the history of the upgrade plan. It shows all the installed applications and plugins and the failed items.

3.  Scroll down to see the skipped records with upgrade plan.

    -   Total: Total number of skipped records
    -   Resolved: Total records from the upgrade plan that have been auto-resolved
    -   To review: Total records left to be reviewed manually
    **Note:** This step is applicable only if you have enabled the GLIDE\_UPGRADE\_PLAN\_INCLUDE\_SKIPS property.

4.  Click **Review upgrade plan** on the Upgrade duration card if you want to check the summary of your upgrade plan history.

    \[Omitted image "uc-upgrade-plan-history.png"\] Alt text: Upgrade Plan History screen.


-   **[Review skipped records with upgrade plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-review-skipped-records-upgrade-plan.md)**  
Review the skipped records after the completion of the upgrade.

**Parent Topic:**[Upgrade Plans tool in Upgrade Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/upgrade-management/um-upgrade-plans-tool.md)

**Related topics**  


[Building your Upgrade Plan]()

[Refreshing your Upgrade Plan]()

[Installing your Upgrade Plan]()

[Prepare to upgrade with Upgrade Plan]()

