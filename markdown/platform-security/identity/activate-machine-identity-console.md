---
title: Activating Machine Identity Console
description: Activate the Machine Identity Management com.glide.identity.machine\_identity\_management to manage your service accounts which are used for integrations with ServiceNow.
locale: en-US
release: australia
product: Identity
classification: identity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Machine Identity Console, Identity]
---

# Activating Machine Identity Console

Activate the **Machine Identity Management** `com.glide.identity.machine_identity_management` to manage your service accounts which are used for integrations with ServiceNow.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the **Machine Identity Management** \(`com.glide.identity.machine_identity_management`\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


