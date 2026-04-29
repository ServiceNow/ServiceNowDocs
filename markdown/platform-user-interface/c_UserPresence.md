---
title: User presence
description: User presence is a Core UI feature that lets you see who is online when you are working in an instance.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# User presence

User presence is a Core UI feature that lets you see who is online when you are working in an instance.

Your avatar appears in the form header next to your name, and in multiple other places such as in activity streams, Visual Task Boards, live feeds, and Connect conversations. A dot on the avatar of the user represents online status.

-   Green dot if the user is logged in.
-   No dot if the user is not logged in.
-   Orange dot if the user recently logged out.

Users can add an avatar image to their live feed profile. If no image is uploaded to the live feed profile, the avatar is the user's initials.

**Note:** Live Feed does not use images uploaded to User \(sys\_user\) records.

When you are viewing a record in a form, such as an incident, you can see if other users are viewing the same record.

![User presence in a form.](../image/UserPresenceViewingRecord.png "User presence in a form")

If multiple users are viewing the record, the avatar is represented by the number of users. Point your cursor to the number to see the names and avatars of the users.

When you are in a Connect conversation or entering comments in an activity stream, you can see information about the activity of the other participant, for example if they are viewing or typing.

![Connect window highlighting the fact that you can see when another user is typing.](../image/UserPresenceChatActivity.png "User presence in a conversation")

An administrator can disable user presence globally.

-   **[Disable user presence](../task/t_DisableUserPresence.md)**  
You can disable user presence globally by enabling a system property.
-   **[Disable live form features](../task/configure-live-form-feat.md)**  
User presence includes several new live form features for Core UI. You can show or hide these features using the **glide.ui16.live\_forms.enabled** property.
-   **[Configure time intervals for user presence](../task/configure-time-interval-user-presence.md)**  
User presence shows that users are viewing a record sometimes after they have already left. The system only checks for user presence every two minutes by default. You can allow the system to check more frequently by configuring some system properties.

**Parent Topic:**[Common UI elements](../../common-ui-elements/topic/p_CommonUIElements.md)

