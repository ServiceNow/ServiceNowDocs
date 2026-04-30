---
title: Business rules installed with Live Feed
description: The Live Feed plugin includes the following business rules.
locale: en-US
release: zurich
product: Live Feed
classification: live-feed
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Components installed with Live Feed, Live Feed reference, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Business rules installed with Live Feed

The Live Feed plugin includes the following business rules.

<table id="table_gpd_nmb_fr"><thead><tr><th>

Business rule

</th><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Feed Group Creator Becomes Admin

</td><td>

Live Group Profile \[live\_group\_profile\]

</td><td>

Designates the group creator as the group administrator.

</td></tr><tr><td>

Live Feed events

</td><td>

Task \[task\]

</td><td>

Runs on task insert, update, and delete. Triggers event associated with the Live Feed Update Script action that processes Live Table Notifications to auto-generate Live Feed messages.

</td></tr><tr><td>

Live feed member update events

</td><td>

Live Group Member\[live\_group\_member\]

</td><td>

Generates a notification event when member state changes \(invited, accepted, declined, left, rejected, request, request\_accepted\).

</td></tr><tr><td>

Live feed integration

</td><td>

Journal Entry \[sys\_journal\_field\]

</td><td>

Writes journal comments to the Live Feed if there is a group for this record.

</td></tr><tr><td>

Live feed new member events

</td><td>

Live Group Member \[live\_group\_member\]

</td><td>

Generates a notification event when new members are added.

</td></tr><tr><td>

Live Feed profile events

</td><td>

Live Profile \[live\_profile\]

</td><td>

Runs on live\_profile insert/update/delete, triggers event associated with the Live Feed Update script action that processes Live Table Notifications to auto-generate Live Feed messages.

</td></tr><tr><td>

Live Feed message events

</td><td>

Live Feed Message \[live\_message\]

</td><td>

Runs on live\_message, notification event trigger for new live messages.

</td></tr><tr><td>

Live message like events

</td><td>

Message Liked by \[live\_message\_like\]

</td><td>

Runs on live\_message\_like, notification event trigger for new like records.

</td></tr><tr><td>

LiveFeed Group Member Visibility 2.0

</td><td>

Live Group Member \[live\_group\_member\]

</td><td>

Ensures users can only see the members list for public groups and groups they belong to.

</td></tr><tr><td>

LiveFeed Group Profile Validation

</td><td>

Live Group Profile \[live\_group\_profile\]

</td><td>

Ensures that a public group is visible.

</td></tr><tr><td>

LiveFeed Group Profile Visibility 2.0

</td><td>

Live Group Profile \[live\_group\_profile\]

</td><td>

Ensures that the list of all groups only displays public groups, private groups that are visible, and groups the user belongs to.

</td></tr><tr><td>

LiveFeed Membership Changes

</td><td>

Live Group Member \[live\_group\_member\]

</td><td>

Enforces that only the group administrator and users with live\_feed\_admin role can manage membership for a group.

</td></tr><tr><td>

LiveFeed Single Group Membership

</td><td>

Live Group Member \[live\_group\_member\]

</td><td>

Ensures that a user is not added multiple times to the same group.

</td></tr><tr><td>

Live Message Likes

</td><td>

Live Message Like \[live\_message\_like\]

</td><td>

Updates the number of likes for a message.

</td></tr><tr><td>

LiveFeed Join Group Check

</td><td>

Live Group Member \[live\_group\_member\]

</td><td>

Ensures that users can not automatically join private visible groups.

</td></tr><tr><td>

Update Follow/Follower Counts

</td><td>

Live Follow \[live\_follow\]

</td><td>

Updates the following/followers counts.

</td></tr><tr><td>

Live Feed Group

</td><td>

Assessable Record \[asmt\_assessable\_record\]

</td><td>

Creates/Deletes a Live Feed group for an assessable record

</td></tr><tr><td>

Live Feed Message Visibility

</td><td>

Live Feed Message \[live\_message\]

</td><td>

Ensures user's access to Live Feed messages

</td></tr></tbody>
</table>**Parent Topic:**[Components installed with Live Feed](r_InstalledWithLiveFeed.md)

