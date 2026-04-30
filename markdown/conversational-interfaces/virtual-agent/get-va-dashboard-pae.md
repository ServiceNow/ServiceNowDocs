---
title: Install Conversational Analytics Dashboard
description: Get updates to the Conversational Analytics dashboard from the ServiceNow Store.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Setting up the Conversational Analytics dashboard, Conversational Analytics dashboard in Platform Analytics experience, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Install Conversational Analytics Dashboard

Get updates to the Conversational Analytics dashboard from the ServiceNow Store.

## Before you begin

**Note:** Starting with the San Diego release, the Conversational Analytics app is automatically installed when you initially activate the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin. Subsequent updates for this app must be downloaded and installed from the ServiceNow Store.

Role required: Chat Analytics Admin

## Procedure

1.  Confirm that your instance has the Glide Virtual Agent plugin \[com.glide.cs.chatbot\] activated.

    Starting with the San Diego release, the Conversational Analytics Dashboard app is automatically installed when you activate the Glide Virtual Agent plugin \[com.glide.cs.chatbot\].

2.  Go to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home?release=e041f740db9d1c18231df3251d961919), and search for analytics.

3.  Select the latest version of Conversational Analytics app.

    The store installs the updates to the Conversational Analytics app and the analytics data configuration tools. The plugin name is com.sn.conversational.analytics and the scope name is sn\_ci\_analytics. Some of the main tables for the Conversational Analytics dashboard include:

    |Table|Description|
    |-----|-----------|
    |sn\_ci\_analytics\_conversation|The main table for conversations. It lists Virtual Agent conversations.|
    |sn\_ci\_analytics\_event|List of events. An event is something that happens, for example, an actionable notification. The dashboard can display analytics about default events or ones you create. For more information, see [Set up custom events](set-up-custom-events-pae.md).|
    |sn\_ci\_analytics\_event\_prop|List of values used in events.|
    |sn\_ci\_analytics\_formula\_override|Lists formula overrides for properties used by the dashboard. For more information, see [Set up custom definitions](set-up-custom-definitions-pae.md).|

    **Note:** You do not need a license or a plugin for Performance Analytics.


**Parent Topic:**[Setting up the Conversational Analytics dashboard](../concept/setting-up-va-dashboard-overview1-pae.md)

