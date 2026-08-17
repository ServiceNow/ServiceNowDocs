---
title: Governing AI asset security
description: Get a snapshot of your AI asset's security posture and visualize how your asset relates to other agentic assets in your enterprise in the AI agent map.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/gov-sec-ai-asset.html
release: zurich
topic_type: concept
last_updated: "2026-06-23"
reading_time_minutes: 3
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Working with AI asset records, Discover and manage AI assets, AI Control Tower, Enable AI experiences]
---

# Governing AI asset security

Get a snapshot of your AI asset's security posture and visualize how your asset relates to other agentic assets in your enterprise in the AI agent map.

When you open an AI asset record, the **Security** tab shows the AI asset security score, access issues, security events, and whether the asset was given elevated privileges or has been dormant \(inactive\) for over 90 days.

It also shows the AI agent map which illustrates how the AI asset relates to other managed AI agents, agentic workflows, providers, and tools across your enterprise.

Get details for each metric area by selecting the arrow in the upper-right corner of each metric.

## AI asset security score

The AI asset security score is a measure of the health of your AI asset in terms of access issues, privileged AI agents, dormant AI systems, output deviation, PII detection, and other criteria. Users should actively manage and review their agent assets and not rely solely on this AI asset security score.

For more information, see [Configure the AI asset security score](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-configure-score.md).

## Access issues

The number of access issues encountered by this AI asset for the last 24 hours, by default. For example, the AI agent couldn't access a database field.

AI agents with access issues may be unable to complete their workflows due to the access issue.

Access issues can also be due to misconfiguration or potentially malicious acts by an agent.

## Security events

The number of security events associated with the AI asset for the last 24 hours, by default.

An AI asset security event is an occurrence that involves a potential threat to your environment's security. For example, if a credit card number is detected in LLM output \(output PII violation\), or if a user replaces an LLM prompt with a malicious prompt designed to obtain a user's password \(prompt injection\). Each AI asset security event has a threat type assigned. For more information, see [Managing AI asset security reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-reference.md).

## AI agent status

Whether the asset was given elevated privileges or has been dormant for the time period shown.

-   **Privileged**

    The AI agent has elevated permissions, such as an agent with admin or security admin permissions that can perform critical actions. Some workflows require that AI agents have elevated permissions to complete.

    An external AI agent is privileged if it has write, modify, or delete access to systems or data. For example, access to cloud infrastructure, IAM configurations, secrets managers, key management services, production databases, or security configurations.

-   **Dormant**

    The AI agent has been inactive for 90 days or longer. Review dormant AI agent permissions to reduce security risk.


## AI agent map

The agent map is an interactive node map showing the relationships of your AI agents, agentic workflows, and tools across your enterprise. You can use the map to review these relationships and AI asset details. When you expand the map, you can filter by agents and agentic workflows.

For more information, see [Discover your agent network with the map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/gov-sec-use-map.md).

**Parent Topic:**[Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-managing-ai-assets.md)

