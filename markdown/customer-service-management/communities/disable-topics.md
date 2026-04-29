---
title: Disable topics in a community
description: Disable the topics feature so that no topic information is visible in your community.
locale: en-US
release: australia
product: Communities
classification: communities
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure community forums, Configuring communities, Communities, Customer Service Management]
---

# Disable topics in a community

Disable the topics feature so that no topic information is visible in your community.

## Before you begin

Role required: sn\_communities.admin

## About this task

The administrator can change the **sn\_communities.enable\_topics** property so that all topic information is hidden in the community. The data is not deleted.

## Procedure

1.  Enter `sys_properties.list` in the filter navigator and search for the **sn\_communities.enable\_topics** property.

2.  In the **Value** field, enter`false`.

3.  Click **Update**.

    -   No topic information is displayed in the **Activity Feed** or **Notifications and Subscriptions**.
    -   No topic information is displayed on the **Forums** or **Topics** landing pages.
    -   No topic information is displayed on Gamification pages and widgets.
    -   Topic fields do not appear when creating, editing, or viewing content.
    -   Topics do not appear in the search results page.

**Parent Topic:**[Configure community forums](configure-forums-topics.md)

