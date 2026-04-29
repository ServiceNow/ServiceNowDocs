---
title: Add featured content in a community
description: Add or edit featured content in a community to appear in the Featured Content section on the community homepage, forum homepage, or both.
locale: en-US
release: australia
product: Communities
classification: communities
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using communities, Communities, Customer Service Management]
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


**Parent Topic:**[Using communities](../concept/using-communities.md)

**Related topics**  


[Community homepage features for logged in users](../concept/c_communities-service-portal.md)

[Navigating the activity feed](../concept/navigating-activity-feed.md)

[Navigating the forum homepage](../concept/forum-homepage.md)

[Community homepage features for non-logged in users](../concept/community-homepage-non-logged.md)

[Self-register to a community](register-community.md)

[Search the community](search.md)

[Use a community profile](community-profile.md)

[Community subscriptions](../concept/c_communities-subscriptions.md)

[Request membership to a forum](request-membership-forum.md)

[Accept an invitation to join a forum](accept-invitation-forum.md)

[Post and respond to content in the community](post-respond-content.md)

[Report inappropriate community content](report-content.md)

[Email a community user](private-message-community-user.md)

[View a list of questions and create a case](case-mgmt-integration-view-list.md)

[Gamification](../concept/communities-gamification.md)

