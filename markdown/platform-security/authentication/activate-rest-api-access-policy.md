---
title: Activate REST API access policy
description: You can activate the REST API Access Policy plugin \(com.glide.rest.policy\) if you have the admin role. If the application does NOT include demo data or it does NOT install related applications and plugins, delete or revise the following sentence:The application includes demo data and installs related ServiceNow Store applications and plugins if they are not already installed.
locale: en-US
release: yokohama
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [REST API access policies, API access policy, Authentication, Access Management]
---

# Activate REST API access policy

You can activate the REST API Access Policy plugin \(com.glide.rest.policy\) if you have the admin role. The application includes demo data and installs related ServiceNow® Store applications and plugins if they are not already installed.

## Before you begin

Role required: admin.

## About this task

The following items are installed with REST API Access Policy:

-   Plugins: com.gilde.auth.profile, com.snc.adaptive\_authentication, com.snc.platform.security.oauth
-   Tables: sys\_api\_access\_policy, sys\_auth\_profile\_mapping, auth\_policy\_mapping, inbound\_auth\_profile, std\_http\_auth.

For more information, see [Adaptive authentication](../concept/adaptive-authentication.md).

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the REST API Access Policy plugin \(com.glide.rest.policy\) using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


