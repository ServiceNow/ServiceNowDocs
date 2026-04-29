---
title: Activate API Key and HMAC Authentication
description: You can activate the plugin API Key and HMAC Authentication \(com.glide.tokenbased\_auth\) in your ServiceNow instance.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [API Key and HMAC Authentication for inbound REST APIs, Token-based authentication, API Authentication, Authentication, Access Management]
---

# Activate API Key and HMAC Authentication

You can activate the plugin API Key and HMAC Authentication \(`com.glide.tokenbased_auth`\) in your ServiceNow® instance.

## Before you begin

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the API Key and HMAC Authentication plugin \(`com.glide.tokenbased_auth`\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


