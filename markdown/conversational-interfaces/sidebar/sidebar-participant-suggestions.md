---
title: Participant suggestions in Sidebar
description: Activate Participant suggestions to display a list of users and user groups who may be helpful additions to a Sidebar discussion.
locale: en-US
release: yokohama
product: Sidebar
classification: sidebar
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Exploring Sidebar, Sidebar, Conversational Interfaces]
---

# Participant suggestions in Sidebar

Activate Participant suggestions to display a list of users and user groups who may be helpful additions to a Sidebar discussion.

When you add participants to a Sidebar discussion, a drop-down list displays users and user groups that can be added. If Participant suggestions are activated, the top of the list displays "top suggestions." The participant suggestions include users or user groups who may be helpful due to their related expertise and also have access to the record.

![Participant suggestions screenshot](../image/participant-finder-screenshot.png)

## Requirements

Participant suggestions have the following requirements:

-   Plugin requirements: To access the base Participant suggestions service, you must download the Participant suggestions plugin \(com.glide.sn\_participant\_suggestions\). Participant suggestions are optimized only for interactions, tasks, and the task's child tables. If you want to receive participant suggestions for any other table, you have to customize the Participant suggestions service. The Participant suggestions plugin works in conjunction with the Sidebar/Omni-Experience Standard feature Set plugin. Both the Participant suggestions plugin and the Sidebar plugin must be installed before you can view the list of suggested users.
-   Lookup table: The lookup table \(suggestion\_service\_lookup\) for participant suggestions applies only to the base Participant suggestion service and not to any third-party participant suggesting services.

