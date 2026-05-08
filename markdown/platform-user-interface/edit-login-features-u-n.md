---
title: Configure login theming in Next Experience
description: Configure Next Experience login illustrations and welcome text to provide a login experience that reflects your branding.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Configure login theming in Next Experience

Configure Next Experience login illustrations and welcome text to provide a login experience that reflects your branding.

## Before you begin

Role required: admin

## About this task

This procedure is specific to login pages and does not apply if you are using Single Sign-On \(SSO\).

## Procedure

1.  In the filter navigator field, enter `sys_properties.list`.

2.  Prevent the login screen from showing any illustrations by setting the property **glide.ui.polaris.login.show\_illustrations** to **false**.

3.  Show welcome text by set the property **glide.ui.polaris.login.show\_welcome** to **true**.

    If this property doesn't exist, add it as a true/false property. For more information, see Add a system property.

4.  Edit the welcome page text.

    1.  Navigate to **System UI** &gt; **Welcome Page Content**.

    2.  Select **New** to create a welcome page content record or open an existing one that you want to display on the login page.

    3.  In the Condition field, enter !gs.getSession\(\).isLoggedIn\(\)the content displays only on the login page before a user signs in

        The content displays only on the login page before a user signs in.

    4.  In the Text field, enter the welcome message or login information you want users to see.

    5.  Select the Active check box.

    6.  Select **Update**.


## Result

The welcome text appears on the Next Experience login page when users are not logged in and is hidden after authentication.

**Parent Topic:**[Working with themes in Next Experience](../concept/next-experience-theming.md)

