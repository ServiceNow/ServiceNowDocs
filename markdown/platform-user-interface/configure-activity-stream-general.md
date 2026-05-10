---
title: Configure stacked view for the Activity stream
description: Configure a stacked view option for journal fields in the Activity stream.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Activity stream, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Configure stacked view for the Activity stream

Configure a stacked view option for journal fields in the Activity stream.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to `sys_properties.list`.

2.  Add the **glide.ui.activity.journal.stacked** system property.

    For more information on adding a system property, see [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/r_AvailableSystemProperties.md).

3.  Set the Value to **true**.

    **Important:** Ensure there are no mandatory fields. Mandatory fields in the Activity stream prevent the stacked view option from displaying.

4.  To give agents the option of using a rich text editor, search for and set the **glide.ui.journal.use\_html** property to **true** .


