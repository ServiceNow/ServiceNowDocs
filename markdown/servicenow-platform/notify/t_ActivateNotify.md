---
title: Activate Notify
description: You can activate the Notify \(com.snc.notify\) plugin if you are an administrator. This plugin includes demo data and activates related plugins if they are not already active.
locale: en-US
release: zurich
product: Notify
classification: notify
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configure, Notify, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Activate Notify

You can activate the Notify \(com.snc.notify\) plugin if you are an administrator. This plugin includes demo data and activates related plugins if they are not already active.

## Before you begin

Role required: admin

## About this task

Notify activates these related plugins if they are not already active.

<table id="table_ikq_swb_lt"><thead><tr><th>

Plugin

</th><th>

Description

</th></tr></thead><tbody><tr><td>

E164 Compliant Phone Number\[com.glide.phone\_number\]

</td><td>

Provides E-164 compliant phone number support.

</td></tr><tr><td>

SMS Preferences \[com.snc.sms\_pref\]

</td><td>

Provides ability to set SMS preferences for receiving messages from different providers.

</td></tr></tbody>
</table>**Note:** If you are upgrading from an earlier version of Notify, the Notify-Twilio driver remains active.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


-   **[Differences between Notify and Legacy Notify](../reference/differences-notify-legacy-notify.md)**  
Describes the differences between the Notify and Legacy Notify applications, including architecture, workflows, Twilio support, and task-initiated conference calls.
-   **[Migrating from Legacy Notify](../reference/r_NotifyMigration.md)**  
When migrating to Notify from the Legacy Notify functionality, several changes are made to the instance.

**Parent Topic:**[Configuring Notify](../concept/configuring-notify.md)

**Related topics**  


[List of plugins](https://www.servicenow.com/docs/access?context=list-of-plugins&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

[E.164 phone number field configuration](https://www.servicenow.com/docs/access?context=r_ConfigureE.164PhoneNumberFields&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US)

