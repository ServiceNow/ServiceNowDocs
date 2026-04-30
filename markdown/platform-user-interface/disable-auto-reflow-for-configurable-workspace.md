---
title: Disable reflow for Configurable Workspace
description: Disable reflow for an instance, experience, or page.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Forms, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Disable reflow for Configurable Workspace

Disable reflow for an instance, experience, or page.

## Before you begin

Role required: admin

## About this task

**Important:** Configurable Workspace pages must use the latest layout system for reflow to be available. For more information, see [Upgrading layouts in UI Builder](https://www.servicenow.com/docs/access?context=upgrade-layout-uib&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

Reflow helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations by transforming page layouts into a vertical, stacked view automatically when users increase browser zoom to 400%. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

A width of 320 CSS pixels is equivalent to a starting viewport width of 1280 CSS pixels at 400% zoom. For web content designed to scroll horizontally, a height of 256 CSS pixels is equivalent to a starting viewport height of 1024 CSS pixels at 400% zoom.

Although reflow is available by default, you can disable it for instances, experiences, and pages.

## Procedure

1.  Disable reflow for an instance.

    1.  Navigate to `sys_properties.list`.

        The entire list of properties in the System Properties \[sys\_properties\] table appears.

    2.  From the System Properties list, select the **glide.ux.autoreflow.disable** system property.

        A System Property record opens.

    3.  Set the Value to **true**.

    4.  Select **Update**.

2.  Disable reflow for an experience.

    1.  Navigate to `sys_ux_app_config.list`.

        The entire list of UX app configurations from the UX App Config \[sys\_ux\_app\_config\] table opens.

    2.  From the UX App Configurations list, select an experience.

        A UX App Configuration record opens.

    3.  Select **Disable Auto Reflow**.

    4.  Select **Update**.

3.  Disable reflow for a page within an experience.

    1.  Navigate to `sys_ux_screen.list`.

        The entire list of UX screens from the UX Screen \[sys\_ux\_screen\] table opens.

    2.  From the UX Screens list, select a page.

        A UX Screen record opens.

    3.  Select **Disable Auto Reflow**.

    4.  Select **Update**.


