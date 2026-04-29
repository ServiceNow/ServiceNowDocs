---
title: Invite a new member to a record feed
description: The feed administrator can invite another user or a team to join a record feed.
locale: en-US
release: australia
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use feeds in Live Feed, Using Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Invite a new member to a record feed

The feed administrator can invite another user or a team to join a record feed.

## Before you begin

Role required: none

## About this task

When a team is added, each of the individual members of the team become members of the feed. That is, if Team ABC is added to a feed, the feed does not show that Team ABC is a member. Instead, the feed shows each of the individual members of Team ABC as members of the feed.

When users are invited, their membership state is initially **Invited**. When they accept the invitation, the system checks their access to the **work\_notes** journal field. If they have write access, they become administrator members; otherwise, they become active members.

## Procedure

1.  Navigate to **Live Feed** &gt; **Live Feed**.

2.  Click **Record Feeds** and select the record feed name.

3.  Click the **Pending members** tab.

4.  In the **Add user or team** field, begin entering a user or team name and select a user or team from the suggestion list.

    If you invite a team, the individual members of the team are invited.

    The invited users receive an email notification.


**Parent Topic:**[Use feeds in Live Feed](../concept/c_UseFeedsInLiveFeed.md)

