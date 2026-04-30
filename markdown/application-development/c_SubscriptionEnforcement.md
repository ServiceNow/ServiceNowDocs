---
title: Access enforcement for ServiceNow Store apps
description: All production instances monitor and generate reports on usage patterns for ServiceNow Store apps. When subscription enforcement is enabled, users who are not subscribed to the app are blocked from performing fulfiller actions in the app.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Contextual development environment, Learning about developing on the ServiceNow AI Platform, Building applications]
---

# Access enforcement for ServiceNow Store apps

All production instances monitor and generate reports on usage patterns for ServiceNow Store apps. When subscription enforcement is enabled, users who are not subscribed to the app are blocked from performing fulfiller actions in the app.

## Overview of ServiceNow Store access

The following actions are required to enable a production instance to enforce entitled usage of your ServiceNow Store App:

1.  The usage admin at your organization uses the Subscription Management application to allocate fulfiller users to the subscription.
2.  You decide on the enforcement mode, either:
    -   Monitor and report usage with no enforcement \(default\)
    -   In addition to monitoring and reporting usage, enforce that all usage must be by subscribed fulfiller users.
3.  To enforce usage only by subscribed users, you configure the tables where only record owners or subscribed fulfiller users can make updates as fulfillment tables.

