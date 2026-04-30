---
title: Reflow for Configurable Workspace
description: Reflow enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.Disable reflow for instances, experiences, or pages.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Reflow for Configurable Workspace

Reflow enables pages and content to be zoomed up to 400% through your browser settings without loss of content or functionality.

**Important:** Configurable Workspace pages must use the latest layout system for reflow to be available. For more information, see [Upgrading layouts in UI Builder](https://www.servicenow.com/docs/access?context=upgrade-layout-uib&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

Reflow helps users with low vision or who have trouble seeing web content in a browser due to monitor size, device type, poor lighting, or other situations by transforming page layouts into a vertical, stacked view automatically when users increase browser zoom to 400%. Additionally, content can be enlarged without scrolling in two dimensions at a width equivalent to 320 CSS pixels or a height equivalent to 256 CSS pixels.

A width of 320 CSS pixels is equivalent to a starting viewport width of 1280 CSS pixels at 400% zoom. For web content designed to scroll horizontally, a height of 256 CSS pixels is equivalent to a starting viewport height of 1024 CSS pixels at 400% zoom.

Although reflow is available by default, administrators can turn off reflow for instances, experiences, and pages.

## Disable reflow for Configurable Workspace

Disable reflow for instances, experiences, or pages.

### Before you begin

Role required: admin

### Procedure

1.  Disable reflow for an instance:

    1.  In the navigation filter, enter `sys_properties.list`, and press **Enter**.

        The entire list of properties in the System Properties \[sys\_properties\] table appears.

    2.  Set the glide.ux.autoreflow.disable system property to true.

2.  Disable reflow for an experience:

    1.  Open the **sys\_ux\_app\_config** table.

    2.  Select an experience.

    3.  Select the **Disable Auto Reflow** check box.

3.  Disable reflow for a page within an experience:

    1.  Open the **sys\_ux\_screen** table for the page within the experience.

    2.  Select the **Disable Auto Reflow** check box.


