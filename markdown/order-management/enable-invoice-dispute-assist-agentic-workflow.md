---
title: Make the invoice dispute assist workflow available in the ServiceNow Otto panel
description: Configure the invoice dispute assist agentic workflow in AI Agent Studio to make it available to agents in the ServiceNow Otto panel in the CSM/FSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/order-management/enable-invoice-dispute-assist-agentic-workflow.html
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring the Manage Invoice Operations application, Business Portal, Configure, Sales Customer Relationship Management]
---

# Make the invoice dispute assist workflow available in the ServiceNow Otto panel

Configure the invoice dispute assist agentic workflow in AI Agent Studio to make it available to agents in the ServiceNow Otto panel in the CSM/FSM Configurable Workspace.

## Before you begin

The application scope must be set to Manage Invoice Operations. You can change the application scope using the application picker \[Omitted image "globe-outline-24.svg"\] Alt text: in the Unified Navigation bar.

Role required: sn\_aia.admin

## About this task

Agentic workflows that are installed with ServiceNow Otto applications aren’t automatically activated. You must activate the invoice dispute assist agentic workflow before it can be used in the ServiceNow Otto panel. After you enable the workflow, you can optionally promote it to make it appear as a suggested topic in the ServiceNow Otto panel for faster access.

## Procedure

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.

2.  On the Manage agentic workflows and AI agents page, select the **Agentic workflows** tab.

3.  Select the **Invoice Dispute Assist** agentic workflow.

4.  From the navigation pane, select **Select channels and status**.

    You could leave the settings in the remaining tabs at their default values.

5.  On the Select channels and status page, enable the **Engage via ServiceNow Otto panel** option.

6.  Select **Save and test**.

7.  Promote the agentic workflow to add it to the list of suggested topics in the ServiceNow Otto panel.

    1.  Navigate to **All** &gt; **Conversational Interfaces** &gt; **Virtual Agent** &gt; **Designer**.

    2.  On the Assistant Designer page, select the **Agentic workflows** tab.

    3.  Narrow your search by selecting **ServiceNow Otto Panel - Platform \(default\)** from the **Select assistant** drop-down menu.

    4.  Locate the Invoice Dispute Assist agentic workflow and select **Promoted** from the More actions icon \[Omitted image "ellipsis-vertical-outline-24.svg"\] Alt text:.

    The invoice dispute assist agentic workflow appears as a promoted topic in the ServiceNow Otto panel, making it directly accessible to agents without requiring a search.


## What to do next

Configure Chat Summarization to enable the summarization and recommendation features in Active Chat. For more information, see [Configure chat summarization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-chat-summarization-in-now-assist_0.md).

**Parent Topic:**[Configuring the Manage Invoice Operations application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/configuring-manage-invoice-operations.md)

**Related topics**  


[Activate an agentic workflow template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-aia-use-case.md)

