---
title: Live Feed security and table access
description: By default, administrators and users with the live\_feed\_admin role can configure live feed security and view all Live Feed tables.
locale: en-US
release: australia
product: Live Feed
classification: live-feed
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Live Feed security and table access

By default, administrators and users with the live\_feed\_admin role can configure live feed security and view all Live Feed tables.

You can also modify the following Live Feed tables:

-   Live Table Notification \[live\_table\_notification\]: Set up automatic messages that are generated when specific records are updated throughout the system.
-   Live Feed Message \[live\_message\]: Modify only if necessary, such as to delete an inappropriate message or restore a message that a user accidentally deleted. This table is typically managed by system functionality.

Extending or modifying data in any Live Feed chat table is not recommended.

-   **[Limit Live Feed access by role](../task/t_LimitLiveFeedAccessByRole.md)**  
All active users in the instance have access to Live Feed by default.
-   **[Manage Live Feed message content](../task/t_ManageLiveFeedMessageContent.md)**  
Users can remove their own messages from feeds. If necessary, administrators can remove inappropriate messages that are posted by any user.
-   **[Live Feed team security](r_LiveFeedTeamSecurity.md)**  
You can restrict who can create teams by modifying an access control rule.
-   **[Restrict hashtag renaming](r_RestrictHashtagRenaming.md)**  
You can restrict who can rename hashtags.

**Parent Topic:**[Administering Live Feed](../concept/c_AdministerLiveFeed.md)

**Related topics**  


[Document feeds](../concept/c_DocumentFeeds.md)

[Record feeds](../concept/c_RecordFeeds.md)

[Live Feed table notifications](../concept/c_SetUpLiveFeedTableNotifications.md)

[Provide access to Live Feed from CMS pages](../task/t_AccessLiveFeedFromCMSPages.md)

