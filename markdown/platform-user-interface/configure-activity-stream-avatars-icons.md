---
title: Display avatars on Activity stream tiles
description: Configure Activity stream tiles to display avatars instead of icons, or both avatars and icons.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Administering Activity stream for Configurable Workspace, Administering Configurable Workspace, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Display avatars on Activity stream tiles

Configure Activity stream tiles to display avatars instead of icons, or both avatars and icons.

## Before you begin

Role required: admin

## Procedure

1.  Display avatars on Activity stream tiles.

    1.  In the Filter navigator, enter `glide.activity.show_tile_icons`.

    2.  Select the property and in the value field enter `true`.

    3.  Set the property to **true**.

        This property is set to **false** by default.

    4.  Select **Update**.

2.  Disable icons on Activity stream tiles.

    1.  In the Filter navigator, enter `glide.asys`.

    2.  Select the property and in the value field enter `false`.

        This property is set to **true** by default. Leaving this field **true** displays both avatars and icons.

    3.  Select **Update**.


