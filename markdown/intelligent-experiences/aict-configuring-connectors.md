---
title: Configuring connectors
description: Discover AI assets running on external platforms and hyperscaler environments to populate your AI asset inventory, apply consistent governance, and report on usage in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-configuring-connectors.html
release: zurich
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Configuring integrations, Configure, AI Control Tower, Enable AI experiences]
---

# Configuring connectors

Discover AI assets running on external platforms and hyperscaler environments to populate your AI asset inventory, apply consistent governance, and report on usage in AI Control Tower.

## Key benefits

-   Keep asset records current automatically through scheduled import jobs, without manually re-entering details each time an asset changes on the external platform.
-   Track usage volume for imported assets alongside natively created ones, so governance teams can spot high-usage, dormant, or high-risk assets and prioritize oversight.
-   Discover assets across multiple accounts or environments with a single AI connection, so oversight scales with adoption without adding to your team's workload.

## Available connectors

For the complete list of supported service graph connectors, their prerequisites, and connector-specific configuration fields, see the [AI Control Tower- AI Discovery Connectors \[KB2986990\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2986990) article in the Now Support Knowledge Base.

AI Control Tower also provides Shadow AI connectors, such as Armis and Agent Client Collector \(ACC\), which detect unsanctioned AI use across your network and endpoints rather than importing known assets directly. For more information, see [Configuring Shadow AI in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/sh-ai-configuring.md).

## How connectors discover AI assets

When you create an AI connection using a connector, AI Control Tower performs the following:

-   Authenticates with the external platform using the credentials you provide, typically an access key, service account, or OAuth token depending on the platform.
-   Discovers AI assets on the external platform, such as deployed models, agents, knowledge bases, and pipelines.
-   Imports the discovered assets into the AI asset inventory and the Configuration Management Database \(CMDB\), where they can be governed, evaluated, and managed alongside natively created assets.
-   Keeps the inventory updated by re-running discovery on a scheduled import job, so new or changed assets on the external platform are reflected in AI Control Tower.

## How connectors keep data current

Each connector runs two scheduled jobs:

-   Discovery: Finds new or changed AI assets on the external platform and imports them into the AI asset inventory.
-   Execution: Collects usage data, such as run counts by agent, date, and session, for assets the connector has already discovered.

**Note:** Verify that the AI discovery daily data collection job is active. This job is required for connectors to continue collecting new data.

## Discovery connectors and trace connectors

Discovery connectors and trace connectors both discover AI assets and feed the same AI asset inventory, but they serve different primary purposes.

-   A discovery connector authenticates directly to the external platform and queries it for AI assets. It's the more direct path for platforms it supports, and it also collects usage volume, such as run counts by agent, date, and session, which appears in the asset's **Value &amp; engagement** tab and in the portfolio-wide value dashboard under Insights.
-   A trace connector observes agent executions at runtime, primarily to generate evaluation and security metrics. Discovering the AI systems behind those executions is a secondary result, useful for catching assets a discovery connector can't reach. See [Discovering AI assets through trace connectors](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-discovering-trace-connectors.md).

-   **[Create an AI connection for discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-create-ai-connection-discovery.md)**  
Bring AI assets from an external platform into your AI asset inventory by creating an AI connection. AI Control Tower authenticates to the platform using your credentials and imports assets on a schedule, so they're governed and monitored alongside AI systems built natively on ServiceNow.

**Parent Topic:**[Configuring integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-integrations.md)

