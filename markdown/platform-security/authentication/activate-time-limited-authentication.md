---
title: Activate time limited authentication
description: Time limited authenication activates through the Integration - Multiple Provider Single Sign-On Installer plugin.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Time limited authentication, Token based authentication \(User logins\), Authentication, Access Management]
---

# Activate time limited authentication

Time limited authenication activates through the Integration - Multiple Provider Single Sign-On Installer plugin.

## Before you begin

Role required: admin

**Note:** Time limited authentication is very specific to ServiceNow instance, the customized links for users can only be created within ServiceNow.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Time Limited Authentication \(`com.snc.authenticate.time_limited_authentication`\) plugin using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated Admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/zurich-platform-administration/page/administer/plugins/task/find-components.html).


