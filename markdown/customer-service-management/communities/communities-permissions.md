---
title: Forum and user permissions management
description: Community and forum administrators can give users and groups of users different levels of access to forums and forum content.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/communities-permissions.html
release: australia
product: Communities
classification: communities
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Configuring communities, Communities, Customer Service Management]
---

# Forum and user permissions management

Community and forum administrators can give users and groups of users different levels of access to forums and forum content.

**Note:** By default, community content is not publicly accessible. A community administrator must enable public access by configuring the appropriate permissions.

There are three components that make up the security settings for forums: forum users, permissions, and forums.

\[Omitted image "forum-user-permissions.png"\] Alt text: Forum and user permissions. Refer to the Default Permissions table for a full description of permissions.

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

\[Omitted image "forum-permission-step2.png"\] Alt text: Steps to assign permissions to users and groups within a forum. Refer to the following list for details on different permission options.

**Note:** Forum permissions are not inherited in the forum hierarchy. Each subforum must be configured with its own set of permissions and content types.

-   You can use forum users and permissions in multiple forums.
-   You can add multiple forum users and permissions to one forum.
-   You can copy permissions from a parent forum to a child forum or from another forum altogether.
-   You can also define user-specific permission exceptions and debug user permissions.

-   **[Create a forum user](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/add-user.md)**  
You can create forum users, which you then use to define memberships to a forum.
-   **[Create a permission](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/create-permission.md)**  
Create a permission to use to define a user's access to a forum and the content in the forum.
-   **[Clone a permission](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/clone-permission.md)**  
Clone a permission if an existing permission record cannot be modified and you require a permission record with similar settings.
-   **[Create a forum permission](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/create-forum-permission.md)**  
Add a forum user and a permission to a forum to create a forum permission.

**Parent Topic:**[Configuring communities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/communities/configure-communities.md)

**Related topics**  


[Community content types]()

[Community feedback types]()

[Community access types]()

[Platform Analytics Solutions for Communities]()

[Migrate Social Q&amp;A data to Communities]()

[View community logs]()

[View community feedback and bookmarks tables]()

[Create a case from a discussion]()

[Enable knowledge harvesting]()

[Activate Communities plugins]()

[Community setup guide for admins]()

[Configure community content types]()

[Configure video sources for a community]()

[Configure community forums]()

[Configure the community profile]()

[Create community Terms and Conditions]()

[Enable users to self-register to a community]()

[Moderate a community]()

[Administer gamification]()

[Community Service Portal]()

