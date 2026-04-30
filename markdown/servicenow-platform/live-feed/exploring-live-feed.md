---
title: Exploring Live Feed Core UI
description: Live Feed content forms a searchable knowledge source for sharing information within an organization.
locale: en-US
release: zurich
product: Live Feed
classification: live-feed
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Exploring Live Feed Core UI

Live Feed content forms a searchable knowledge source for sharing information within an organization.

## Live Feed overview

**Important:**

Core UI is required to use Live Feed. Live Feed is not supported in Next Experience. If you turn on Next Experience, Live Feed is automatically disabled and will no longer work. See [Next Experience UI](https://www.servicenow.com/docs/access?context=next-experience-landing-page&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US) for more information.

While Live Feed has been discontinued, we are always exploring new ways to enhance our services. Stay tuned for future updates and improvements.

Live Feed content forms a searchable knowledge source for sharing information within an organization. Main features include the following:

-   Users can post, reply to, and rate messages, including links and images.
-   Administrators can set up automatic messages that are generated when specific records are updated throughout the system.
-   Users can subscribe to receive email notifications when new messages are posted.
-   Users who take advantage of the accessibility options in the platform can tab through a Live Feed to navigate.

Live Feed includes different types of feeds, including company feeds, group feeds, individual feeds, and record feeds.

**Note:** Live Feed v2 is active for all new instances by default. If you are upgrading from an earlier version of ServiceNow®, you need to activate Live Feed v2 to use these features.

Live feed can be domain separated at the data level only. For more information on Live Feed and domain separation, see [Domain separation in Live Feed](../reference/r_DomainSeparationInLiveFeed.md).

## Live Feed users

<table id="table_hc2_2tr_rbc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Admins

</td><td>

Admins activate and administer Live feed in the following ways:-   Add and configure document feeds
-   Activate and configure record feeds
-   Set up notifications
-   Manage Live Feed security

</td></tr><tr><td>

Users

</td><td>

Users can subscribe to feeds, post content, work on records, and use hashtags.

</td></tr></tbody>
</table>## Live Feed benefits

<table id="table_kc2_2tr_rbc"><thead><tr><th>

Benefit

</th><th>

Feature

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Document feeds allow users to work on tasks and other records through the Live Feed interface. Users can post messages in Live Feed that are automatically maintained as comments or work notes on the record, if the record has these journal fields.

</td><td>

[Document feeds](c_DocumentFeeds.md)

</td><td>

Configuration: AdminsUsers: anyone

</td></tr><tr><td>

Record feeds allow users to work on tasks and other records through the Live Feed interface. Users can post messages in Live Feed that are automatically maintained as comments or work notes on the record if the record has these journal fields.

</td><td>

[Record feeds](c_RecordFeeds.md)

</td><td>

Configuration: AdminsUsers: anyone

</td></tr><tr><td>

When a record is inserted or updated on a specific task table and the notification conditions are met, a message is generated and posted to the specified group or to the company feed.

</td><td>

[Live Feed table notifications](c_SetUpLiveFeedTableNotifications.md)

</td><td>

Configuration: AdminsUsers: anyone

</td></tr><tr><td>

Users can be combined into teams for the purpose of subscribing to specifically-focused feeds.

</td><td>

[Teams in Live Feed](c_UseTeamsInLiveFeed.md)

</td><td>

Configuration: AdminsUsers: anyone

</td></tr><tr><td>

Hashtags are words marked with a hash symbol \(\#\) in messages. Hashtags are a way to categorize messages by keyword or topic for improved search results.

</td><td>

[Hashtags in Live Feed](c_UseHashtagsInLiveFeed.md)

</td><td>

Anyone

</td></tr></tbody>
</table>## What to explore next

To learn more about configuring and using Live Feed, see:

-   [Activating Live Feed](../task/t_ActivateLiveFeed.md)
-   [Administering Live Feed](c_AdministerLiveFeed.md)
-   [Using Live Feed](c_UseLiveFeed.md)
-   [Live Feed reference](../reference/live-feed-reference.md)

