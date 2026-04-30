---
title: Upgrade Monitor schedule states
description: When an upgrade is scheduled, the Upgrade Monitor displays information about the next scheduled upgrade. It displays the date and time when the next scheduled upgrade will start. If there is no upgrade scheduled, the Upgrade Monitor displays Status: No upgrade detected.
locale: en-US
release: yokohama
product: Upgrade Center
classification: upgrade-center
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Upgrade Monitor module, Exploring Upgrade Center, Upgrade Center, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Monitor schedule states

When an upgrade is scheduled, the Upgrade Monitor displays information about the next scheduled upgrade. It displays the date and time when the next scheduled upgrade will start. If there is no upgrade scheduled, the Upgrade Monitor displays **Status: No upgrade detected**.

## No upgrade scheduled

There is no upgrade that has been scheduled currently.

![Image showing no scheduled upgrade over monitor view](../image/uc-monitor-no-upgrade1.png)

You can also schedule an upgrade by selecting **Schedule upgrade**. To check for an immediately available upgrade, select **Check for upgrade**. It also shows the current version of your upgrade and the date it was upgraded on.

## Upgrade scheduled

There is an upgrade that has been scheduled to start at a given time.![Image showing a scheduled upgrade over monitor view](../image/uc-monitor-scheduled-upgrade.png)

You can also reschedule the upgrade by selecting **Reschedule upgrade**. To check for an immediately available upgrade, select **Check for upgrade**. By selecting either **Reschedule upgrade** or **Schedule upgrade**, you will be directed to [HI Upgrade Wizard](https://support.servicenow.com/kb_view.do?sysparm_article=KB0792425).

## Upgrade monitor with issue detected

If one or both of the triggers for upgrading the system \('Check distribution for possible upgrade' and 'Check database for possible upgrade'\) have been customized or are missing, the Upgrade Monitor displays a warning and provides a button for resolving the issues.

**Note:** If your instance is self-hosted \(not hosted by ServiceNow\) this message may not necessarily indicate a problem. If you have customized or disabled the upgrade job and want to keep that customization or disabled state, do not select the button to fix the upgrade issue.

![Image showing the error message "Detected an issue with one or more upgrade jobs. Your next upgrade might not run. Click here to fix the upgrade jobs."](../image/uc-monitor-issue.png)

To resolve the issues with the upgrade jobs, select the link in the message. This action reverts both upgrade triggers \('Check distribution for possible upgrade' and 'Check database for possible upgrade'\) to their base versions.

**Note:** 'Upgrade' job has been renamed to 'Check distribution for possible upgrade' starting Paris. 'Check Upgrade Script' job has been renamed to 'Check database for possible upgrade' starting Paris.

