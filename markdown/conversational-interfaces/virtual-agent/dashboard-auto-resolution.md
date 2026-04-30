---
title: Legacy - Issue auto-resolution tab
description: The Issue auto-resolution tab helps you understand how well your Virtual Agent \(VA\) chatbot anticipates user needs. It displays information about the number of user issues intercepted by the auto-resolution service and resolved by VA.
locale: en-US
release: yokohama
product: Virtual Agent
classification: virtual-agent
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Legacy - Using the Conversational Analytics Dashboard, Legacy - Conversational Analytics Dashboard, Analyzing Virtual Agent performance, Virtual Agent, Conversational Interfaces]
---

# Legacy - Issue auto-resolution tab

The **Issue auto-resolution** tab helps you understand how well your Virtual Agent \(VA\) chatbot anticipates user needs. It displays information about the number of user issues intercepted by the auto-resolution service and resolved by VA.

**Important:**

Conversational Analytics dashboard is being prepared for future deprecation. It will be supported until deprecation but will no longer be available for installation. A new Conversational Analytics dashboard in Platform Analytics experience, which meets the compliance requirements of Government Community Cloud \(GCC\), and thus FedRAMP authorized, is available. See [Conversational Analytics dashboard in Platform Analytics experience](VA-dashboard-landing-page-pae.md).

For details on the deprecation process, see the [Deprecation Process \[KB0867184\]](https://support.servicenow.com/kb_view.do?sysparm_article=KB0867184) article in the Now Support Knowledge Base.

If you are an existing user of this dashboard and want to migrate analytics data to the new dashboard, see [Migrate data to Conversational Analytics dashboard in Platform Analytics experience \[KB1651556\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1651556).

Issue auto-resolution takes place when a user is diverted to VA from a non-conversational interface. For example, a user might request a new keyboard through a service portal or email. The auto-resolution service can detect the user request and use VA to resolve the user's request in a VA chatbot session. For more information, see [Auto Resolution for Virtual Agent](auto-resolution-va.md).

The data visualizations in the **Issue auto-resolution** tab displays how well the auto-resolution service is working. This tab is available only when Issue Auto Resolution is enabled and the **Auto Resolution Configuration** record is set as active.

To access the **Issue auto-resolution** tab, you must have the chat analytics admin role or the chat analytics viewer role.

![Data visualizations for this tab include intent and topic-matching results, matching and conversational trends, acceptance rate, and top topics.](../images/issue-auto-resolution-tab.png "Issue auto-resolution tab")

Selecting the data or pointing to the data in the visualizations displays additional information about the data.

|Visualization|Description|
|-------------|-----------|
|Intents with Matched Topics|Number of intents that match topics enabled for auto-resolution.|
|Intents without Matched Topics|Number of intents that do not have matching topics.|
|Intents with Auto-resolution Disabled|Number of intents that match topics not enabled for issue auto-resolution.|
|Intent and topic matching results|Breakdown of incidents by intent matching. For example, incidents with matching intents and topics, and incidents without matching intents.|
|Trends in intent and topic matching|Trend showing incidents that have intents with or without matching topics.|
|Auto resolution conversations|Issue auto-resolution conversations that were resolved and unresolved. Resolved means incidents are in the resolved state after the users interacted with VA.|
|Auto resolution conversation trends|Usage trend showing all the issue auto-resolution conversations and how many incidents were successfully resolved.|
|Issue auto-resolution acceptance rate|Shows the issue auto-resolution notifications that were accepted and declined by users.|
|Top topics in auto resolution conversations|Frequently used topics in auto resolution conversations.|

**Parent Topic:**[Legacy - Using the Conversational Analytics Dashboard](use-the-dashboard-overview.md)

