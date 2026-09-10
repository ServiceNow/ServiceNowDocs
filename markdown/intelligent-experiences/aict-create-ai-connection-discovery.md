---
title: Create an AI connection for discovery
description: Bring AI assets from an external platform into your AI asset inventory by creating an AI connection. AI Control Tower authenticates to the platform using your credentials and imports assets on a schedule, so they're governed and monitored alongside AI systems built natively on ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/aict-create-ai-connection-discovery.html
release: australia
topic_type: task
last_updated: "2026-08-05"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring connectors, Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Create an AI connection for discovery

Bring AI assets from an external platform into your AI asset inventory by creating an AI connection. AI Control Tower authenticates to the platform using your credentials and imports assets on a schedule, so they're governed and monitored alongside AI systems built natively on ServiceNow.

## Before you begin

Confirm the following are in place:

-   The com.sn\_ai\_disc and sn\_sgc\_central plugins installed on your instance. Without both plugins, the **Connectors** tab doesn't appear.
-   The credentials required to authenticate AI Control Tower to the external platform. Credential requirements vary by connector.

Role required: sn\_ai\_disc.discovery\_admin and sn\_cmdb\_int\_util.sgc\_admin

## About this task

A connector is the mechanism; an AI connection is the configured instance of a connector on your instance. Create a separate AI connection for each account or environment you want AI Control Tower to discover assets from. A single connector type can support multiple AI connections.

## Procedure

1.  Navigate to **All** &gt; **AI Control Tower** &gt; **Home** &gt; **Settings** &gt; **Integrations** &gt; **Connectors**.

2.  On the **Available Connectors** tab, select the connector that you want to use.

3.  On the form, fill in the fields.

    Fields and credential requirements vary by connector. For the complete list of connectors and the fields each one requires, see [AI Control Tower- AI Discovery Connectors \[KB2986990\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2986990).

4.  Select **Save**.


## Result

The connection appears on the **Established connections** tab. After the discovery job runs, discovered AI assets appear in your AI asset inventory.

**Parent Topic:**[Configuring connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/aict-configuring-connectors.md)

