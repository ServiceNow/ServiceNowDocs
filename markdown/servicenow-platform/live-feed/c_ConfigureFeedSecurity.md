---
title: Security configuration for document feeds
description: Document feeds honor the access control rules \(ACLs\) for the associated record. Users can only view messages on the document feed if they have access to the same information on the record.
locale: en-US
release: zurich
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Document feeds, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Security configuration for document feeds

Document feeds honor the access control rules \(ACLs\) for the associated record. Users can only view messages on the document feed if they have access to the same information on the record.

Consider the following examples:

-   If an ACL allows a user to read and create comments on an incident, then the user can view and add messages posted as comments on the incident feed.
-   If an ACL restricts a user from reading work notes, then the user cannot view messages posted as work notes on the incident feed.

**Note:** Access control rules are only checked when a user first accesses the document feed. After users view the feed, an administrator must remove them manually to change their access.

**Parent Topic:**[Document feeds](c_DocumentFeeds.md)

**Related topics**  


[Add a Live Feed UI action on a table](../task/t_AddALiveFeedUIActionOnATable.md)

[Configure document feeds](../task/t_ConfigureDocumentFeeds.md)

[Disable a record feed](../task/t_DisableARecordFeed.md)

[Disable a document feed](../task/t_DisableADocumentFeed.md)

[Business rule installed with Live Feed Document](../reference/r_InstalledComponents.md)

