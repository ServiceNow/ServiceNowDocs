---
title: Document feeds
description: A document feed is a Live Feed group that is associated with a record, such as an incident or change.
locale: en-US
release: xanadu
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Document feeds

A document feed is a Live Feed group that is associated with a record, such as an incident or change.

Document feeds allow users to work on tasks and other records through the Live Feed interface. Users can post messages in Live Feed that are automatically maintained as comments or work notes on the record, if the record has these journal fields.

The benefits of using document feeds include the following.

-   Improving communication between users working on the same record.
-   Improving visibility into progress for end users.
-   Providing a single place to see updates on multiple records.
-   Saving conversation history in the record so that knowledge is not lost in an email chain.

To use document feeds, activate the Live Feed Document plugin, which is active by default in new instances. See [Use Live Feed to work on records](c_UsingLiveFeedToWorkOnRecords.md) to learn how to use this feature.

The system automatically creates a document group for the feed when a user follows or shows a record on Live Feed. The system also creates a document group when a user creates a new record on a table that has Live Feed enabled.

The following list describes features of the document feed group.

-   Is unlisted; it does not appear when users view all groups on Live Feed.
-   Automatically approves membership for every user who can access the record.
-   Uses the record number as the group name.
-   Uses the record short description as a group description.
-   Maintains all messages posted to Live Feed on the record, if the record has a journal field for comments. If the record has a standard text field for comments, each live post overwrites the field value.
-   Maintains all messages posted on the record in Live Feed if the record has a journal field for comments. When the group is created, existing messages are added to the document feed.

A user who participates in Live Feed becomes a member of the group.

-   **[Add a Live Feed UI action on a table](../task/t_AddALiveFeedUIActionOnATable.md)**  
You can add UI actions on a table to allow users to follow records in live feed.
-   **[Configure document feeds](../task/t_ConfigureDocumentFeeds.md)**  
You can configure a table to support document feeds.
-   **[Security configuration for document feeds](c_ConfigureFeedSecurity.md)**  
Document feeds honor the access control rules \(ACLs\) for the associated record. Users can only view messages on the document feed if they have access to the same information on the record.
-   **[Disable a record feed](../task/t_DisableARecordFeed.md)**  
You can disable Live Feed functionality from the form of any table.
-   **[Disable a document feed](../task/t_DisableADocumentFeed.md)**  
You can disable a document feed from the form of any table.
-   **[Business rule installed with Live Feed Document](../reference/r_InstalledComponents.md)**  
This business rule is installed with Live Feed Document. There are no tables, roles, or notifications installed with it.

**Parent Topic:**[Administering Live Feed](c_AdministerLiveFeed.md)

**Related topics**  


[Record feeds](c_RecordFeeds.md)

[Live Feed table notifications](c_SetUpLiveFeedTableNotifications.md)

[Live Feed security and table access](../reference/r_LiveFeedTableAccessRules.md)

[Provide access to Live Feed from CMS pages](../task/t_AccessLiveFeedFromCMSPages.md)

[Activate a plugin](https://www.servicenow.com/docs/access?context=t_ActivateAPlugin&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

