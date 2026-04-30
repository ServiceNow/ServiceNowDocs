---
title: Legacy - System parameter configuration
description: Use system parameters to configure the functionality of the Conversational Analytics dashboard.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Legacy - Conversational Analytics dashboard reference, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - System parameter configuration

Use system parameters to configure the functionality of the Conversational Analytics dashboard.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

Use the following system parameters to configure the functionality of the Conversational Analytics dashboard. You must have the Chat Analytics Admin \[chat\_analytics\_admin\] role.

|Functionality|System parameter|Description|
|-------------|----------------|-----------|
|Debug|sn\_ci\_analytics.logging.verbosity|Set this parameter to "debug" to see the debug logs for conversational analytics. The setting makes the logs verbose with debug information.|
|Reasons|sn\_ci\_analytics.ca.reason\_max|Sets the maximum length of reason strings. The default is 1000 characters.|
|Hash|sn\_ci\_analytics.show\_hashed\_user\_id|Set this parameter to true to display hashed User Ids on the Conversations and Users pages in the dashboard. The default is false.|

**Parent Topic:**[Legacy - Conversational Analytics dashboard reference](conversational-analytics-dashboard-reference.md)

