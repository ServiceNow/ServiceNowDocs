---
title: Discovering AI assets through trace connectors
description: Extend your AI asset inventory to AI agents running on hyperscaler cloud platforms by discovering them through trace connectors.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/disc-discovering-trace-connectors.html
release: zurich
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 1
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Discovering AI assets, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Discovering AI assets through trace connectors

Extend your AI asset inventory to AI agents running on hyperscaler cloud platforms by discovering them through trace connectors.

Trace connectors are primarily an observability capability. A trace connector polls a supported cloud platform, such as AWS, Azure, or Google Cloud, and collects execution-level trace data through a MID Server. AI Control Tower analyzes that data to produce the evaluation scores that appear on the **Monitor** tab of the AI system's asset record, and the security metrics that appear on its **Security** tab.

An established trace connection that gathers trace data for monitoring quality and safety, or security, is discovering AI systems at the same time, filling in assets that connectors and native detection can't reach. Assets detected this way register automatically in your AI asset inventory.

For more information, see [Configuring trace connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-configuring-trace-connections.md).

