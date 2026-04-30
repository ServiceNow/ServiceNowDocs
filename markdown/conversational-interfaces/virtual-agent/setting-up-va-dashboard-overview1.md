---
title: Legacy - Setting up the Conversational Analytics Dashboard
description: Set up custom events and formula definitions to create more targeted analytics.
locale: en-US
release: xanadu
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Setting up the Conversational Analytics Dashboard

Set up custom events and formula definitions to create more targeted analytics.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

The Conversational Analytics Dashboard enables you to customize the data you monitor in the following ways:

-   [Date range](../task/use-the-dashboad.md)—Specify the date range for the data displayed on the dashboard.
-   [Custom events](../task/set-up-custom-events.md)—The dashboard can display analytics about custom events you create. All events must relate to conversations. For example, you can store data about every conversation that used a specific channel, such as Slack.
-   [Formula Override](../task/set-up-custom-definitions.md)—Customize parameter definitions used in analytic reports. For example, by default, duration is the total time from the first to the last exchange in a conversation. You might like to override that formula by subtracting inactive times in the conversation.

## Role requirements

For information on roles, see [Legacy - Conversational Analytics dashboard roles](conversational-analytics-dashboard-roles.md#).

## Dependencies

The Conversational Analytics Dashboard requires the Quebec or later version of Virtual Agent.

-   **[Legacy - Install Conversational Analytics Dashboard](../task/get-va-dashboard.md)**  
Get updates to the Conversational Analytics dashboard from the ServiceNow Store. Use this dashboard to gain insights on Virtual Agent \(VA\) chats with customers.
-   **[Legacy - Create custom events to monitor](../task/set-up-custom-events.md)**  
Create custom events and monitor them in the Conversational Analytics Dashboard.
-   **[Legacy - Create custom override definitions](../task/set-up-custom-definitions.md)**  
Use scripts to override the default formulas used to create the analytics on the Conversational Analytics Dashboard.
-   **[Legacy - Formula override example](../reference/formula-override-examples.md)**  
Use the following formula override example to craft your own formula overrides.

**Parent Topic:**[Legacy - Conversational Analytics Dashboard](VA-dashboard-landing-page.md)

