---
title: Activate OAuth email authentication
description: You can activate the Email:OAUTH support for IMAP, Microsoft Graph \(Receiving\), and SMTP plugin \(com.glide.email.oauth\) for Notifications if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OAuth email authentication, Advanced email setup, Configure, Email Administration, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate OAuth email authentication

You can activate the Email:OAUTH support for IMAP, Microsoft Graph \(Receiving\), and SMTP plugin \(com.glide.email.oauth\) for Notifications if you have the admin role.

## Before you begin

Role required: admin

## About this task

The following items are installed with Email:OAUTH support for IMAP, Microsoft Graph \(Receiving\), and SMTP:

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Email:OAUTH support for IMAP, Microsoft Graph \(Receiving\), and SMTP plugin \(com.glide.email.oauth\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


**Parent Topic:**[OAuth email authentication](../concept/c_OAuthEmailAuthentication.md)

