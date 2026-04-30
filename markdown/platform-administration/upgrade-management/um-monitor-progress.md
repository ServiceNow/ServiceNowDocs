---
title: Upgrade Progress
description: When an upgrade is underway, Upgrade Progress displays progress bars and other information to help you monitor the process.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Monitor an upgrade to an instance, Upgrade Monitor tool in Upgrade Console, Upgrade Console tools, Using Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# Upgrade Progress

When an upgrade is underway, Upgrade Progress displays progress bars and other information to help you monitor the process.

You can view the status of each of the stages during an upgrade process. It helps you to know exactly which stage you are in at any point of the upgrade process.

![Image showing ATF store app advertisement banner](../../upgrade-center/image/uc-atf-app.png)

If you have the ATF Test Generator and Cloud Runner store application installed, you can schedule test generation runs from the Upgrade Monitor page. The above message shows up during an upgrade process when the following conditions are met.

-   The SN\_ATF\_TG plugin is not active.
-   The instance is not a fed instance.
-   The instance is not a self-hosted instance.

**Note:** You can now confidently upgrade your instance by using the [ATF Test Generator and Cloud Runner](https://store.servicenow.com/sn_appstore_store.do#!/store/application/db1676d7421441106f046193880e0b37) store app. See [Exploring ATF Test Generator and Cloud Runner](https://www.servicenow.com/docs/access?context=atf-tg-cr-landing&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US) for more information.

Once the database upgrade starts, the following details show up. ![Image showing the status of an in-progress upgrade](../../upgrade-center/image/uc-upgrade-progress.png)

|Field|Input Value|
|-----|-----------|
|Current version|Current version of the instance|
|Target version|Target upgrade version of the instance|
|Upgrade Progress|A progress bar depicting where the upgrade is in the overall process. The length of a section in the bar does not indicate the relative duration of that process.|
|Upgrade Progress: Upgrading Platform|The system is applying upgrades to elements that form the foundation of the platform.|
|Upgrade Progress: Updating Schema|The system is scanning the plugins to create a list of tables that require upgrading. This prevents the system from upgrading the same table multiple times.|
|Upgrade Progress: Loading Plugins|The system is loading both core and optional plugins. Some features require more than one plugin, so the number of plugins listed may not match the number of optional features installed.|
|Upgrade Progress: Completing|The system is upgrading components that need to be completed after the previous three stages are done.|
|Details|Shows the current activity, a progress bar for the current activity, and the file currently being updated.|
|Node Upgrades|The color of the icons represents the status of each node during this upgrade: Pending, Running, Successful, Failed, or Down.|
|Node|The selected node indicated by the arrow. To change the selection, position the mouse cursor over the icon for the node to select.|
|Running time|How long the selected node \(indicated by the arrow\) has been running. If the selected node is offline, this value stops updating and shows how long a node was online before going offline.|
|Version|The current build for the selected node \(indicated by the arrow\).|
|Successful upgrade|When the selected node is online, shows how long the node has been online. If the selected node is offline, shows how long the node has been offline.|

**Parent Topic:**[Monitor an upgrade to an instance](../task/um-monitor-instance-upgrade.md)

