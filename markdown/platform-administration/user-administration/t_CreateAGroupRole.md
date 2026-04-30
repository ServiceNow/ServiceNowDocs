---
title: Create a group role
description: Create a group role to control access to features and capabilities in applications for all members in a group.
locale: en-US
release: xanadu
product: User Administration
classification: user-administration
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create a role, Managing roles, User administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a group role

Create a group role to control access to features and capabilities in applications for all members in a group.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to **All** &gt; **User Administration** &gt; **Group Roles**.

2.  Select **New**.

3.  Fill in the fields on the form and then select **Submit**.

    |Field|Description|
    |-----|-----------|
    |Group|Select a group.|
    |Role|Select the role to apply to the group.|
    |Inherits|Select this option to have all members of the group inherit the role. This option is selected by default.|

    **Note:** To move this action to the background so you aren’t waiting when adding a number of group members, add the system property **glide.ui.schedule\_slushbucket\_save\_for\_group\_roles** and set it to true.


**Parent Topic:**[Create a role](t_CreateARole.md)

