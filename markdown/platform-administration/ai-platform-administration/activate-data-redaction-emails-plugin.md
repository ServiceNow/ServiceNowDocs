---
title: Activate sensitive data redaction for inbound emails plugin
description: You can activate the Sensitive Data Redaction for Inbound Emails plugin \(com.glide.email\_inbound.redaction\) for Notifications if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application installs related plugins if they are not already installed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/ai-platform-administration/activate-data-redaction-emails-plugin.html
release: zurich
product: AI Platform Administration
classification: ai-platform-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sensitive data redaction, Use, Inbound email, Notifications, Configure core features, Administer]
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

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/find-components.md).


## What to do next



**Note:** Data Discovery application does not require a paid subscription when used along with sensitive data redaction for inbound emails plugin.

**Data Discovery patterns**

 are used to filter table entries for further classification. The Data Discovery pattern defines the regular expression used to match data against a target table. For more information, see .

**Parent Topic:**[Sensitive data redaction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/sensitive-data-redaction.md)

