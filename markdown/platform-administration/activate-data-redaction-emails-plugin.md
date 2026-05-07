---
title: Activate sensitive data redaction for inbound emails plugin
description: You can activate the Sensitive Data Redaction for Inbound Emails plugin \(com.glide.email\_inbound.redaction\) for Notifications if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application installs related plugins if they are not already installed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Sensitive data redaction, Use, Inbound email, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Activate sensitive data redaction for inbound emails plugin

You can activate the Sensitive Data Redaction for Inbound Emails plugin \(com.glide.email\_inbound.redaction\) for Notifications if you have the admin role. The application installs related plugins if they are not already installed.

## Before you begin

Role required: admin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Sensitive Data Redaction for Inbound Emails plugin \(com.glide.email\_inbound.redaction\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

[Activating Data Discovery](https://www.servicenow.com/docs/access?context=activate-data-discovery&version=australia&pubname=australia-platform-security&ft:locale=en-US)

**Note:** Data Discovery application does not require a paid subscription when used along with sensitive data redaction for inbound emails plugin.

**Data Discovery patterns**

[Default regular expression data patterns](https://www.servicenow.com/docs/access?context=default-data-patterns&version=australia&pubname=australia-platform-security&ft:locale=en-US) are used to filter table entries for further classification. The Data Discovery pattern defines the regular expression used to match data against a target table. For more information, see [Configure Data Discovery patterns](https://www.servicenow.com/docs/access?context=configure-data-discovery-patterns&version=australia&pubname=australia-platform-security&ft:locale=en-US).

**Parent Topic:**[Sensitive data redaction](../concept/sensitive-data-redaction.md)

