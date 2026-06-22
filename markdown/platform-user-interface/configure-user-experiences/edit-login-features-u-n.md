---
title: Edit login theming in Next Experience
description: Customize Next Experience login illustrations and welcome text to provide a login experience that reflects your branding.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-user-interface/configure-user-experiences/edit-login-features-u-n.html
release: xanadu
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with themes in Next Experience, Configuring the Next Experience UI, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Edit login theming in Next Experience

Customize Next Experience login illustrations and welcome text to provide a login experience that reflects your branding.

## Before you begin

Role required: admin

## About this task

This procedure is specific to login pages and does not apply if you are using Single Sign-On \(SSO\).

## Procedure

1.  In the filter navigator field, enter `sys_properties.list`.

2.  Prevent the login screen from showing any illustrations by setting the property **glide.ui.polaris.login.show\_illustrations** to **false**.

3.  Show welcome text by set the property **glide.ui.polaris.login.show\_welcome** to **true**.

    If this property doesn't exist, add it as a true/false property. For more information, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/r_AvailableSystemProperties.md).

4.  Edit the welcome page text.

    1.  Navigate to **System UI** &gt; **Welcome Page Content**.

    2.  Add a property that contains the login content you want to display.

        For the syntax of the isLoggedIn\(\) condition, see [GlideSession - Global](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/api-reference/server-api-reference/c_GlideSessionAPI.md).


**Parent Topic:**[Working with themes in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-user-interface/configure-user-experiences/next-experience-theming.md)

