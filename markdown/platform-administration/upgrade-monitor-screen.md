---
title: Upgrade Monitor
description: When an upgrade is not running, the Upgrade Monitor displays information about the next check for an available upgrade.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
keywords: [upgrade, monitor]
breadcrumb: [Upgrade Monitor module: Upgrade an individual instance, Upgrades and conversions, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Monitor

When an upgrade is not running, the Upgrade Monitor displays information about the next check for an available upgrade.

The Upgrade Monitor displays the next date and time when the system will check for an available upgrade.

![Upgrade Monitor Check Now Screenshot](../image/upgrade-mon-check-now.png "Upgrade Monitor")

To check immediately for an available upgrade, click **Check Now**.

If one or both of the triggers for upgrading the system \('Check distribution for possible upgrade' and 'Check database for possible upgrade'\) have been customized or are missing, the Upgrade Monitor displays a warning and provides a button for resolving the issues.

**Note:** If your instance is self-hosted \(not hosted by ServiceNow\) this message may not necessarily indicate a problem. If you have customized or disabled the upgrade job and want to keep that customization or disabled state, do not click the button to fix the upgrade issue.

![Upgrade Monitor with issue detected](../image/upgrade-mon-fix.png "Upgrade Monitor with Issue Detected")

To resolve the issues with the upgrade jobs, click **Fix Upgrade Jobs**. This action reverts both upgrade triggers \('Check distribution for possible upgrade' and 'Check database for possible upgrade'\) to their base versions.

**Note:** 'Upgrade' job has been renamed to 'Check distribution for possible upgrade' starting Paris. 'Check Upgrade Script' job has been renamed to 'Check database for possible upgrade' starting Paris.

