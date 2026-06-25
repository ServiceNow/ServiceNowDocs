---
title: Activate Communities plugins
description: Activate the Customer Communities plugin to use the Communities application.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/communities/activate-communities.html
release: australia
product: Communities
classification: communities
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configuring communities, Communities, Customer Service Management]
---

# Activate Communities plugins

Activate the Customer Communities plugin to use the Communities application.

## Before you begin

Role required: sn\_communities.admin

## About this task

Communities is available for customers who are:

-   Licensed for the Customer Service Management application.
-   Licensed for HR Service Delivery.

To activate Communities, activate the Customer Communities plugin \(com.sn\_customer\_communities\). This plugin is not active by default.

When you activate the Customer Communities plugin, the following plugins automatically activate:

-   External User Registration plugin \(com.sn\_external\_user\_register\)
-   Communities plugin \(com.sn\_communities\)
-   Gamification plugin \(com.snc.gamification\)
-   Subscriptions and Activity Feed Framework plugin \(com.snc.activity\_subscriptions\)

To activate Communities demo data, activate the Communities Demo Data plugin \(com.sn\_communities\_demo\).

To activate the Communities dashboard, activate the Performance Analytics — Content Pack — Communities plugin \(com.snc.pa.communities\).

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Plugins**.

2.  Search for the plugin com.sn\_communities.

3.  Click **Install**.

4.  Click **Activate** on the Activate Plugin pop-up window.


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

[Community setup guide for admins]()

[Configure community content types]()

[Configure video sources for a community]()

[Configure community forums]()

[Forum and user permissions management]()

[Configure the community profile]()

[Create community Terms and Conditions]()

[Enable users to self-register to a community]()

[Moderate a community]()

[Administer gamification]()

[Community Service Portal]()

