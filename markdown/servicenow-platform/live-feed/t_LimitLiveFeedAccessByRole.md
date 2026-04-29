---
title: Limit Live Feed access by role
description: All active users in the instance have access to Live Feed by default.
locale: en-US
release: australia
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Live Feed security and table access, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Limit Live Feed access by role

All active users in the instance have access to Live Feed by default.

## Before you begin

Role required: live\_feed\_admin and admin

## Procedure

1.  Complete the following steps to define the roles that allow users to see the Live Feed module.

    1.  Perform the appropriate action for your version of the UI:

        -   Core UI: Navigate to **System Definition** &gt; **Application Menus**, and then select **Live Feed**.
        -   UI15: Right-click the icon beside the Live Feed module and select **Edit Module**.
    2.  Enter the roles that have access in the **Roles** field.

    3.  Click **Update**.

2.  Complete the following steps to define the roles that allow users to see live feed from a mobile device.

    1.  Navigate to **System Definition** &gt; **Applications \(Mobile\)**.

    2.  Click **Live Feed**.

    3.  Enter the roles that have access in the **Roles** field.

    4.  Click **Update**.

3.  Use the following settings in the Access Control form to create access control rules to limit who can view the live\_feed pages.

    -   **Type**: ui page
    -   **Operation**: read
    -   **Name**: create one access control rule record for each of the following pages
        -   live\_feed
        -   live\_feed\_small
        -   $live\_feed
        -   $live\_feed\_small
    -   **Requires role**: in this related list, add roles to define who can access the Live Feed pages. Users who do not have these roles cannot access Live Feed.

**Parent Topic:**[Live Feed security and table access](../reference/r_LiveFeedTableAccessRules.md)

