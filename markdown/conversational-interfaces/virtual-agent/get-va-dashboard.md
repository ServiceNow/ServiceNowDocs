---
title: Legacy - Install Conversational Analytics Dashboard
description: Get updates to the Conversational Analytics dashboard from the ServiceNow Store. Use this dashboard to gain insights on Virtual Agent \(VA\) chats with customers.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Legacy - Setting up the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Install Conversational Analytics Dashboard

Get updates to the Conversational Analytics dashboard from the ServiceNow Store. Use this dashboard to gain insights on Virtual Agent \(VA\) chats with customers.

## Before you begin

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](../concept/VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

**Note:** Starting with the San Diego release, the Conversational Analytics app is automatically installed when you initially activate the Glide Virtual Agent \(com.glide.cs.chatbot\) plugin. Subsequent updates for this app must be downloaded and installed from the ServiceNow Store.

Conversational Analytics dashboard is not available for on-premise installation.

Using the Conversational Analytics dashboard may incur Integration Hub transaction costs. This transaction metering was unintended and will be removed in an upcoming release. If the issue persists, please create a case for our Customer Service and Support team.

Role required: Chat Analytics Admin

## Procedure

1.  Confirm that your instance has the Glide Virtual Agent plugin \[com.glide.cs.chatbot\] activated.

    Starting with the San Diego release, the Conversational Analytics Dashboard app is automatically installed when you activate the Glide Virtual Agent plugin \[com.glide.cs.chatbot\].

2.  Go to the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home?release=e041f740db9d1c18231df3251d961919), and search for analytics.

3.  Select the latest version of Conversational Analytics Dashboard.

    The store installs the updates to the Virtual Agent Analytics Dashboard and the Analytics data configuration tools. The plugin name is com.sn.conversational.analytics and the scope name is sn\_ci\_analytics. Some of the main tables for the Conversational Analytics Dashboard include:

    |Table|Description|
    |-----|-----------|
    |sn\_ci\_analytics\_conversation|The main table for conversations. It lists Virtual Agent conversations.|
    |sn\_ci\_analytics\_event|List of events. An event is something that happens, for example, an actionable notification. The dashboard can display analytics about default events or ones you create. For more information, see [Set up custom events](set-up-custom-events.md).|
    |sn\_ci\_analytics\_event\_prop|List of values used in events.|
    |sn\_ci\_analytics\_formula\_override|Lists formula overrides for properties used by the dashboard. For more information, see [Set up custom definitions](set-up-custom-definitions.md).|

    **Note:** You do not need a license or a plugin for Performance Analytics.


**Parent Topic:**[Legacy - Setting up the Conversational Analytics Dashboard](../concept/setting-up-va-dashboard-overview1.md)

