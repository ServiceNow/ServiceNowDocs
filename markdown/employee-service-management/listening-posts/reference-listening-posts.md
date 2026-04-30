---
title: Reference for Listening Posts
description: Reference topics provide additional information about Listening Posts.Several types of components are installed with activation of the Listening Posts \(sn\_lp\) plugin, including tables, user roles, and scheduled jobs.
locale: en-US
release: yokohama
product: Listening Posts
classification: listening-posts
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Listening Posts, Employee Journey Management, HR Service Delivery, Employee Service Management]
---

# Reference for Listening Posts

Reference topics provide additional information about Listening Posts.

**Parent Topic:**[Listening Posts](../concept/listening-posts-1.md)

## Components installed with Listening Posts

Several types of components are installed with activation of the Listening Posts \(sn\_lp\) plugin, including tables, user roles, and scheduled jobs.

Demo data is available for this feature.

### Roles installed

<table id="table_u1t_gb1_wdb"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Listening Posts Admin

 \[sn\_lp.admin\]

</td><td>

Can create, read, and delete all the records in Listening Posts.

</td><td>

sn\_lp.manager

</td></tr><tr><td>

Creator\[sn\_lp.creator\]

</td><td>

-   Can create pulse surveys.
-   Can access the dashboard view.

</td><td>

-   survey\_admin
-   sn\_lp.dashboard\_view

</td></tr><tr><td>

Manager\[sn\_lp.manager\]

</td><td>

-   Can create pulse surveys.
-   Can access the dashboard view.

</td><td>

sn\_lp.creator

</td></tr><tr><td>

Dashboard viewer\[sn\_lp.dashboard\_view\]

</td><td>

Can access the dashboard view.

</td><td>

None

</td></tr></tbody>
</table>### Scheduled jobs installed

<table id="table_dx3_gb1_wdb"><thead><tr><th>

Scheduled job

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Content Automation: Create LP Pulse survey

</td><td>

-   Creates pulse surveys for campaigns that are in published state with Content Type **Pulse Survey**.
-   Verifies if the **Re-evaluate campaign** check box is enabled. Based on **Re-evaluate frequency**, the scheduled job creates or cancels instances for the users who are added or removed from the campaign.

**Note:** When you refine the audience in a campaign, the intersection of the users at campaign and campaign content level are considered for delivering pulse surveys.


</td></tr><tr><td>

Listening Posts: Create Group Pulse Instance

</td><td>

-   Creates instances for surveys that are in published state. If the end date of a survey has passed, the schedule job changes the state of the pulse survey to closed.
-   Creates instances for surveys that are in ready state. If the start date of a pulse survey has passed, the scheduled job creates instances for that pulse survey. If the end date of a pulse survey has passed, the schedule job changes the state of the pulse survey to closed.

</td></tr></tbody>
</table>### Tables installed

<table id="table_fbz_45z_vdb"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Pulse Content \[sn\_lp\_cd\_pulse\_survey\_content\]

</td><td>

Store records of Content Type **Pulse Survey**.

</td></tr><tr><td>

Pulse Content Question\[sn\_lp\_m2m\_pulse\_content\_question\]

</td><td>

Links questions to pulse content.

</td></tr><tr><td>

Pulse Survey\[sn\_lp\_pulse\_survey\]

</td><td>

Stores details of pulse surveys.

</td></tr><tr><td>

Pulse Theme\[sn\_lp\_pulse\_theme\]

</td><td>

Store details of themes. Theme is a group of pulse surveys.

</td></tr><tr><td>

Response Sharing Rule\[sn\_lp\_response\_sharing\_rule\]

</td><td>

Stores details of response sharing rules. A response sharing rule defines groups with which pulse survey responses are shared.

</td></tr><tr><td>

User Demographic\[sn\_lp\_user\_demographic\]

</td><td>

Stores user profile data along with the user's response for a pulse question.

</td></tr></tbody>
</table>