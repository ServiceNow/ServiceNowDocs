---
title: Display the most recent reply in the Activity stream
description: Configure the Activity stream to reduce visual clutter by displaying the most recent reply first.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Activity stream, Administer, Configurable Workspace UI, Configure UIs and portals, Configure user experiences]
---

# Display the most recent reply in the Activity stream

Configure the Activity stream to reduce visual clutter by displaying the most recent reply first.

## Before you begin

Role required: admin

## About this task

By default, the Activity stream displays all entries including every reply and update. To reduce visual clutter, you can configure the Activity stream to display the most recent reply.

Displaying the most recent reply in the Activity stream relies on two types of configuration:

-   **System properties**

    The **glide.activity.last\_viewed\_timestamp.local\_storage\_limit** and **glide.activity.last\_viewed\_timestamp.local\_storage\_retention\_days** system properties control how many and how long timestamps are stored locally for displaying the most recent reply.

-   **UI Builder properties**

    The properties for the Activity Stream component in UI Builder control whether the Activity stream should show all replies or the most recent one. For information on Activity Stream component properties in UI Builder, see [Activity Stream UIB Setup](https://developer.servicenow.com/dev.do#!/reference/next-experience/yokohama/now-components/now-activity-stream-connected/uib-setup).


## Procedure

1.  Navigate to `sys_properties.list`.

2.  Add a system property named **glide.activity.last\_viewed\_timestamp.local\_storage\_limit**.

    For more information on adding a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

3.  Set the Value to the maximum number of timestamps to store locally for displaying the most recent reply.

4.  Select **Submit**.

5.  Add a system property named **glide.activity.last\_viewed\_timestamp.local\_storage\_retention\_days**.

6.  Set the Value to the number of days to store timestamps locally for displaying the most recent reply.

7.  Select **Submit**.


