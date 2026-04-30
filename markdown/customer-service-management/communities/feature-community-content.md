---
title: Add featured content in a community
description: Add or edit featured content in a community to appear in the Featured Content section on the community homepage, forum homepage, or both.
locale: en-US
release: yokohama
product: Communities
classification: communities
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Community Service Portal, Configure a community, Communities, Customer Service Management]
---

# Add featured content in a community

Add or edit featured content in a community to appear in the Featured Content section on the community homepage, forum homepage, or both.

## Before you begin

Set the following properties as required.

<table id="table_yxb_5yw_4hb"><thead><tr><th>

Property name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_communities.default\_featured\_days

</td><td>

Default number of days for content to be featured. End date is calculated from the date the content is featured on.

</td></tr><tr><td>

sn\_communities.max\_featured\_limit

</td><td>

Maximum amount of featured content at forum or at global level.

</td></tr><tr><td>

sn\_communities.featured\_global\_notify\_user

</td><td>

Send notifications to community users when content is featured on the community homepage. This property is inactive by default. **Note:** Notifications are always sent to community administrators and moderators.

</td></tr></tbody>
</table>To send out email notifications when featured content expires, set the Featured Content Expire scheduled job to **Active**.

Role required: sn\_communities.admin, sn\_communities.community\_moderator, sn\_communities.forum\_admin, or sn\_communities.forum\_moderator

## Procedure

1.  Navigate to the community homepage.

2.  Click the content you want to feature.

    **Note:** Question and Answer content types are not enabled for featuring by default. To enable Question or Answer content types for featuring, navigate to **Community** &gt; **Administration** &gt; **Content Types**. Click the content type you want to enable and select the **Allow Featuring** check box. In the same way, you can also disable content types for featuring.

3.  Click **...** and **Mark as featured**.

4.  On the Feature Content pop-up window, select whether to feature the content on the community homepage or in a specific forum.

    A notification that content has been featured is sent out to the author of the content, community users who commented on the post, and community users who are subscribed to the post. If featured content has expired or is removed from the featured content list by another user, community and forum administrators are notified.


**Parent Topic:**[Community Service Portal](../concept/community-service-portal.md)

