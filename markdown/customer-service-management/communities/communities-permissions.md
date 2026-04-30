---
title: Forum and user permissions management
description: Community and forum administrators can give users and groups of users different levels of access to forums and forum content.
locale: en-US
release: zurich
product: Communities
classification: communities
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Configuring communities, Communities, Customer Service Management]
---

# Forum and user permissions management

Community and forum administrators can give users and groups of users different levels of access to forums and forum content.

**Note:** By default, community content is not publicly accessible. A community administrator must enable public access by configuring the appropriate permissions.

There are three components that make up the security settings for forums: forum users, permissions, and forums.

![Forum and user permissions. Refer to the Default Permissions table for a full description of permissions.](../images/forum-user-permissions.png)

-   **Forum users**

    A forum user is a logical group of users, user groups, or both. This group is used to define memberships to a forum.

-   **Permissions**

    A permission is a combination of:

    -   access types for a forum
    -   access types for a given content type
-   **Forums**

    A forum is the container for user-created content. A forum must be configured with content types and permissions before becoming available for users to contribute content.


You can create your own permission or use one of the default permissions that the Communities application delivers.

|Permission|Description|
|----------|-----------|
|Blog Read|Read access to blogs.|
|Blog Read and Comment Write|Read access to blogs and write access to comments.|
|Blog Write|Write access to blogs.|
|Blog Write and Comment Write|Write access to blogs and comments.|
|Default Permission for Memberships|Default permissions for forums that are marked as **Enable Membership for this Forum**.|
|Default permissions for public user|Public access to forums.|
|Default permissions for registered user|Permissions for registered and logged in users.|
|Document Read and Comment Write|Read access to documents and write access to comments.|
|Document Write and Comment Write|Write access to documents and comments.|
|Event Read and Comment Write|Read access to events and write access to comments.|
|Event Write and Comment Write|Write access to events and comments.|
|Forum Admin|Full access to a forum.|
|Forum Moderator|Moderation access to a forum.|
|Forum Name and Description Read|Read access to the name and description of a forum. To access content or topics, other permissions are required.|
|Full Access|Write and read access to all content types.|
|Question and Answer Read|Read access to questions and answers.|
|Question and Answer Write|Write access to questions and answers.|
|Question Write|Write access to questions.|
|Video Read and Comment Write|Read access to videos and write access to comments.|
|Video Write and Comment Write|Write access to videos and comments.|

To assign permissions to users and user groups, create associations between forum users and permissions for a specific forum.

![Steps to assign permissions to users and groups within a forum. Refer to the following list for details on different permission options.](../images/forum-permission-step2.png)

**Note:** Forum permissions are not inherited in the forum hierarchy. Each subforum must be configured with its own set of permissions and content types.

-   You can use forum users and permissions in multiple forums.
-   You can add multiple forum users and permissions to one forum.
-   You can copy permissions from a parent forum to a child forum or from another forum altogether.
-   You can also define user-specific permission exceptions and debug user permissions.

-   **[Create a forum user](../task/add-user.md)**  
You can create forum users, which you then use to define memberships to a forum.
-   **[Create a permission](../task/create-permission.md)**  
Create a permission to use to define a user's access to a forum and the content in the forum.
-   **[Clone a permission](../task/clone-permission.md)**  
Clone a permission if an existing permission record cannot be modified and you require a permission record with similar settings.
-   **[Create a forum permission](../task/create-forum-permission.md)**  
Add a forum user and a permission to a forum to create a forum permission.

**Parent Topic:**[Configuring communities](../reference/configure-communities.md)

**Related topics**  


[Community content types](c_communities-content-types.md)

[Community feedback types](feedback-types.md)

[Community access types](access-types.md)

[Platform Analytics Solutions for Communities](../../../use/dashboards/application-content-packs/communities-content-pack.md)

[Migrate Social Q&amp;A data to Communities](../task/migrate-socialqa.md)

[View community logs](../task/view-community-logs.md)

[View community feedback and bookmarks tables](../task/view-feedback-bookmark-tables.md)

[Create a case from a discussion](case-management-integration.md)

[Enable knowledge harvesting](communities-km-integration-configure.md)

[Activate Communities plugins](../task/activate-communities.md)

[Community setup guide for admins](../reference/r_setup-communities-admin.md)

[Configure community content types](../task/enable-content-types-for-community.md)

[Configure video sources for a community](../../customer-service-management/task/create-video-configuration.md)

[Configure community forums](../task/configure-forums-topics.md)

[Configure the community profile](../task/configure-community-profile.md)

[Create community Terms and Conditions](../task/create-terms-conditions.md)

[Enable users to self-register to a community](configure-registration.md)

[Moderate a community](../task/moderate-communities.md)

[Administer gamification](communities-gamification-administer.md)

[Community Service Portal](community-service-portal.md)

