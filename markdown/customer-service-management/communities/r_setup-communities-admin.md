---
title: Community setup guide for admins
description: Define your requirements with community and forum stakeholders and set up your forums for community users to start creating content.
locale: en-US
release: yokohama
product: Communities
classification: communities
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Communities, Customer Service Management]
---

# Community setup guide for admins

Define your requirements with community and forum stakeholders and set up your forums for community users to start creating content.

## Requirements

The roles required to define requirements and set up forums include sn\_communities.admin or sn\_communities.forum\_admin.

## Before you begin

-   **Meet with the stakeholders**

    |Stakeholder|Responsibilities|
    |-----------|----------------|
    |Forum administrators|Define and oversee the forum processes for day-to-day operations related to topic creation, user management, and moderation.|
    |Community administrators|Configure advanced settings for Communities features.|
    |Community users|Contribute content in the form of questions, answers, blogs, and comments.|

-   **With stakeholders, determine your community requirements**
    -   Who are the consumers of the community content?
    -   Which content types can users contribute?
    -   Who can contribute content and who should have read-only access?
    -   What should the names of the initial forums be?
    -   Within these forums, what should the names of the initial topics be?
    -   Which keywords should be banned?
    -   How should the system moderate content and users?
    -   What should the default notifications that users receive for various community activities be?

## What to do

Use the following steps as guidance to setting up your community.

1.  Create a forum user: [Create a forum user](../task/add-user.md) to use to define memberships to a forum.
2.  Create a permission: [Create a permission](../task/create-permission.md) to use to define a user's access to a forum and its content types.
3.  Add access and content types to your permission: [Add access types to a permission](../task/define-access-type-permission.md) to determine the access that users have to certain forums and content.
4.  Create a forum: [Create a forum](../task/create-forum.md) to provide a place for users to share content and configure the forum to allow registered users to request access to join.
5.  Configure content types for a forum: [Configure content types for a forum](../task/add-content-type-to-forum.md) to define which types of content to use in a particular forum.
6.  Create a forum permission: [Create a forum permission](../task/create-forum-permission.md) by adding a forum user and a permission to a forum.

If required, perform the following actions:

-   **Invite users to join the forum**

    [Invite users to become members of a forum](../task/invite-users-forum.md) to encourage greater community involvement.

-   **Create permission exceptions**

    [Create a permission exception](../task/manage-permission-exceptions.md) for users who require specific permissions for a forum.

-   **Copy permissions**
    -   [Copy permissions from a forum](../task/copy-permissions-from-another-forum.md) to copy all permissions and content types from one forum to another.
    -   [Copy permissions from a parent forum](../task/copy-permissions-from-parent-forum.md).
-   **Debug user permissions**

    [Debug user permissions](../task/debug-user-permissions.md) to investigate and diagnose problems with user access to forums.


## Next steps

[Create a topic](../task/create-topic.md) for users to create and share content.

[Add a topic to a forum](../task/add-topic-to-forum.md) so that users can associate content to that topic.

[Moderate a community](../task/moderate-communities.md) to set up how the system moderates content and users.

## Using guided setup to implement Communities

Communities guided setup provides a sequence of tasks that help you configure Communities on your ServiceNow instance. To open Communities guided setup, navigate to **Community** &gt; **Administration** &gt; **Guided Setup**.

For more information about using the guided setup interface, see [Using guided setup](https://www.servicenow.com/docs/access?context=guided-setup&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

**Parent Topic:**[Communities](servicenow-communities.md)

