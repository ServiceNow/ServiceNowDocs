---
title: Activate Email Retention
description: The Email Retention plugin provides archive and destruction rules for email messages. It is active by default for new instances, but must be activated for upgrades.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Email retention, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate Email Retention

The Email Retention plugin provides archive and destruction rules for email messages. It is active by default for new instances, but must be activated for upgrades.

## Before you begin

Role required: admin

## About this task

The Email Retention plugin requires these plugins:

-   [Data archiving](../../database-rotation/concept/c_ArchiveData.md)
-   System Mailboxes

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[Email retention](../concept/email-retention.md)

