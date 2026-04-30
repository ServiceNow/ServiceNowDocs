---
title: Use Live Feed to work on records
description: A record feed is associated with a record, such as an incident or change.
locale: en-US
release: xanadu
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Using Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Use Live Feed to work on records

A record feed is associated with a record, such as an incident or change.

Record feeds help users collaborate on records by providing a place for anyone who can access the record to share messages and post attachments specific to that record.

With record feeds, users can:

-   Follow record feeds and post messages in Live Feed. These messages can also be automatically maintained in the comments or work notes journal fields on records.
-   View Live Feed from records.
-   Work on multiple records from **My Feed**.
-   Access Live Feed team functions, such as sending invitations and subscribing to email notifications.

Any users with access to the record can also use the record feed. By default, record feeds are available on the incident, change, and problem tables. Administrators can configure record feeds for additional tables.

![Live Feed Document](../image/LiveFeedDocumentFuji.png "Live Feed Document")

## How Document Feeds Work

The Live Feed application creates a document group for each document feed. The document group:

-   Automatically approves membership for every user who can access the record.
-   Uses the record number as the group name.
-   Uses the record short description as a group description.
-   Maintains all messages posted on the record in Live Feed \(if the record has a journal field for comments\). When the group is created, existing messages are added to the document feed.
-   Lists the group when users select **View all groups** on their Live Feed interface, unless the record associated with the document feed has been closed. When the state of the record is closed, the Live Feed group becomes inactive and unlisted.
-   Automatically adds users to the document group when they view the record.

## Document Group Creation

When a user follows or shows a record on Live Feed, a Live Feed group is automatically created and associated to the record \(if one does not already exist\). The user becomes a member of the group and can use Live Feed to work on the record. If the user can access work notes on the record, the user also becomes a group administrator.

A Live Feed group is also automatically created when a user creates a record on a table that uses document feeds, such as the Incident table. The user who creates the record becomes the administrator of the group, and any other user who modifies the same record automatically joins the group.

