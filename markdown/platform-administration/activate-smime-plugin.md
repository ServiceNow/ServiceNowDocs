---
title: Activate S/MIME Email
description: You can activate the S/MIME Email plugin \(com.glide.email.smime\) for Notifications if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Email encryption - S/MIME protocol, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate S/MIME Email

You can activate the S/MIME Email plugin \(com.glide.email.smime\) for Notifications if you have the admin role.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the S/MIME Email plugin \(com.glide.email.smime\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

[Import an S/MIME key pair](import-smime-key-pair.md)

**Parent Topic:**[Email encryption - S/MIME protocol](../concept/smime-inbound-outbound-mails.md)

**Related topics**  


[Setting up S/MIME for email](../concept/smime-for-email-signing-and-encryption.md)

