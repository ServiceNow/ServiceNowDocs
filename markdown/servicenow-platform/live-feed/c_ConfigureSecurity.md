---
title: Configure security
description: Record feeds honor the access control rules \(ACLs\) for the associated record.
locale: en-US
release: yokohama
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Record feeds, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Configure security

Record feeds honor the access control rules \(ACLs\) for the associated record.

Users can only view messages on the record feed if they have access to the same information on the record. For example:

-   If an ACL allows a user to read and create comments on an incident, then the user can view and add messages posted as comments on the incident feed.
-   If an ACL restricts a user from reading work notes, then the user cannot view messages posted as work notes on the incident feed.

**Note:** Access control rules are only checked when a user first accesses the record feed. After users view the feed, an administrator must remove them manually to change their access.

**Parent Topic:**[Record feeds](c_RecordFeeds.md)

