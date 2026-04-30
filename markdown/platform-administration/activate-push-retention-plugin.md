---
title: Activate the Push Retention plugin
description: The Push Retention plugin \(com.glide.push\_retention\) provides the retention policy for push notifications, so that you can specify when the system archives and destroys push notification records.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Push notification retention, Push notifications, System notifications, Notifications, Configure core features, Administer]
---

# Activate the Push Retention plugin

The Push Retention plugin \(com.glide.push\_retention\) provides the retention policy for push notifications, so that you can specify when the system archives and destroys push notification records.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Push notification retention](../concept/push-notification-retention.md)

**Related topics**  


[List of plugins \(Zurich\)](../../plugins/reference/list-of-plugins.md#)

