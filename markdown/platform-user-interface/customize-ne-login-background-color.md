---
title: Customize the Next Experience login background color
description: Customize and change the background color applied to your Next Experience login page.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with themes, Configure, Next Experience UI, Configure UIs and portals, Configure user experiences]
---

# Customize the Next Experience login background color

Customize and change the background color applied to your Next Experience login page.

## Before you begin

Role required: admin

If a background illustration is set, this image overrides any custom background color. Before proceeding, delete the **glide.ui.login.style.background.image** system property if it exists. If you'd prefer to add an illustration to your Next Experience login page, see [Customize the Next Experience login background illustration](customize-login-background.md).

## About this task

This procedure is specific to login pages and does not apply if you are using Single Sign-On \(SSO\).

Set any RGB value for the background color. However, the login modal continues to display the default theme colors. The default theme is the theme that appears first in a user's Theme preference. When multiple themes are published and the user selects a theme other than the default, the login modal displays the default theme colors. For information setting the default theme for your Theme Builder themes, see [Set the default theme](set-the-default-theme.md). For information setting the default theme for Theme Builder and themes created manually using Next Experience, see [Publish multiple themes in Next Experience](configure-presentation-order-of-themes.md).

## Procedure

1.  Navigate to the **All** menu and enter `sys_properties.list` in the filter navigator.

2.  Select **New** to create a system property.

3.  In the **Name** field, enter `glide.ui.polaris.login.style.background`.

4.  In the **Type** drop-down list, select **String**.

5.  In the **Value** field, enter an RGB value.

    An RGB value defines a color by combining red, green, and blue components, each represented by a number from 0 to 255, in the format R, G, B.

6.  Verify that the Ignore cache option is selected.

7.  Select **Submit**.


## What to do next

Log out of your experience to view the new login page background color.

**Parent Topic:**[Working with themes in Next Experience](../concept/next-experience-theming.md)

