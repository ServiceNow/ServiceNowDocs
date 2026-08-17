---
title: Basic concepts for AI asset security
description: Learn more about the AI asset security score, agent map, AI asset security events, and internal and external agents.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-basic-concepts.html
release: zurich
topic_type: concept
last_updated: "2026-05-02"
reading_time_minutes: 2
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, Managing AI asset security, Govern AI assets, AI Control Tower, Enable AI experiences]
---

# Basic concepts for AI asset security

Learn more about the AI asset security score, agent map, AI asset security events, and internal and external agents.

## AI asset security events

An AI asset security event is an occurrence that involves a potential threat to your environment's security. For example, if a credit card number is detected in LLM output \(output PII violation\). Or, if a user replaces an LLM prompt with a malicious prompt designed to obtain a user's password \(prompt injection\). Each AI asset security event has a threat type assigned. For more information, see [Managing AI asset security reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-reference.md) and [Monitor AI asset security events and recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-use-events.md).

On the Post-runtime tab, the top AI asset security events are organized by threat category to help you prioritize areas to focus on and address. Selecting a cell in the heat map shows a corresponding list of AI asset security events below it.

## AI asset security score

The AI asset security score reflects the health of your AI assets in terms of access issues, privileged AI agents, dormant AI systems, output deviation, PII detection, and other criteria. When you view score details, a list view shows the AI assets that are included in your AI asset security score calculation. Your score is the average of all managed AI assets listed. Users should actively manage and review their agent assets and not rely solely on this AI asset security score.

You can exclude an AI asset from your score by muting it. For example, you can mute an AI asset if you determine that remediating the asset’s issue would be a risky change. For more information, see [Managing AI asset security reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-reference.md).

You can also configure the score to remove security categories from the score calculation or change the weights of categories. For more information, see [Configure the AI asset security score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-score.md).

## Agent map

The agent map is an interactive map showing the relationships of your AI providers, AI models, MCP servers, AI agents, agentic workflows, and tools across your enterprise. You can use the map to review these relationships and AI asset details. The map includes filters for both agents and agentic workflows.

## Internal and external agents

Internal agents are agents that are provided by ServiceNow. External agents are those provided by third parties, such as Google or Amazon Web Services. On the Runtime and Post-runtime tabs, filter on internal or external agents to compare the security postures of your ServiceNow and third-party agents.

**Parent Topic:**[Exploring security in AI Control Tower](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-exploring.md)

