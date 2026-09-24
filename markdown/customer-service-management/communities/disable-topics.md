---
title: Disable topics in a community
description: Disable the topics feature so that no topic information is visible in your community.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/disable-topics.html
release: brazil
product: Communities
classification: communities
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure community forums, Configuring communities, Communities, Customer Service Management]
---

# Disable topics in a community

Disable the topics feature so that no topic information is visible in your community.

## Before you begin

Role required: sn\_communities.admin

**Important:**

Starting with the Brazil release, Communities is being prepared for future deprecation. It will be hidden and no longer installed on new instances but will continue to be supported. For details, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

## About this task

The administrator can change the **sn\_communities.enable\_topics** property so that all topic information is hidden in the community. The data is not deleted.

## Procedure

1.  Enter `sys_properties.list` in the filter navigator and search for the **sn\_communities.enable\_topics** property.

2.  In the **Value** field, enter`false`.

3.  Click **Update**.

    -   No topic information is displayed in the **Activity Feed** or **Notifications and Subscriptions**.
    -   No topic information is displayed on the **Forums** or **Topics** landing pages.
    -   No topic information is displayed on Gamification pages and widgets.
    -   Topic fields do not appear when creating, editing, or viewing content.
    -   Topics do not appear in the search results page.

**Parent Topic:**[Configure community forums](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/communities/configure-forums-topics.md)

