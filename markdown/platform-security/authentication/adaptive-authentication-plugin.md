---
title: Activate adaptive authentication
description: You can activate the Adaptive Authentication plugin \(com.snc.adaptive\_authentication\) for Adaptive Authentication if you have the admin role.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Adaptive authentication, Authentication, Access Management]
---

# Activate adaptive authentication

You can activate the Adaptive Authentication plugin \(com.snc.adaptive\_authentication\) for Adaptive Authentication if you have the admin role.

## Before you begin

## About this task

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the **Adaptive Authentication** \(com.snc.adaptive\_authentication\) plugin using the filter criteria and search bar.![Adaptive Authentication plugin](../images/adaptive-auth-plugin.png)

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/australia-platform-administration/page/administer/plugins/task/find-components.html).


## What to do next

Configure your authentication policies to enforce contextual authentication controls on your instance.

Once your policies are configured. Enable adaptive authentication using the **Enable Authentication Policy** policy. For details on adaptive authentication properties, see [Configure adaptive authentication properties](configure-adaptive-auth-properties.md).

