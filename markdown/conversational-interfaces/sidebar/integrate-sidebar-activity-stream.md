---
title: Integrating Sidebar and activity stream
description: For agents to post Sidebar discussions in the activity stream, Sidebar must be integrated with the activity stream and Sidebar options must display in the post filters. If the Sidebar options don’t display in the post filters, you must add them.
locale: en-US
release: australia
product: Sidebar
classification: sidebar
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring Sidebar, Sidebar, Conversational Interfaces]
---

# Integrating Sidebar and activity stream

For agents to post Sidebar discussions in the activity stream, Sidebar must be integrated with the activity stream and Sidebar options must display in the post filters. If the Sidebar options don’t display in the post filters, you must add them.

## Before you begin

Role required: admin

**Note:** List of post types without Sidebar options:

![Post types menu without Sidebar options.](../image/post-types-menu-1.png)

## Procedure

1.  If Sidebar was automatically installed in the workspace:

    1.  Check the `sys_properties` file for the record glide.ui.\{table\_name\}\_activity.fields where \{table\_name\} is the parent record table name.
    2.  If the `sys_properties` file record exists for the record table, check whether it includes **Sidebar discussion** and **Sidebar posted message**. If it doesn't, add **Sidebar discussion** and **Sidebar posted message** at the end of the existing value.

        ![sys_properties file record for activity stream post type filter instructions. Sidebar discussion and Sidebar posted message are highlighted in the Value field.](../image/activity-stream-post-type-filter.png)

2.  If Sidebar was manually added for a record in a workspace:

    1.  Check the `sys_properties` file for glide.ui.\{table\_name\}\_activity.fields where \{table\_name\} is the parent record table name.
    2.  If the `sys_properties` file record exists for the record table, check whether it includes **Sidebar discussion** and **Sidebar posted message**. If it doesn't, add **Sidebar discussion** and **Sidebar posted message** at the end of the existing value.

        ![sys_properties file record for activity stream post type filter instructions.](../image/activity-stream-post-type-filter.png)

    3.  If the `sys_properties` file record doesn’t exist for the record table, it loads the default filters which contain Sidebar filters.
    **Note:** List of post types with Sidebar options:

    ![Post types menu with sidebar options highlighted.](../image/sidebar-same-post-type.png)


