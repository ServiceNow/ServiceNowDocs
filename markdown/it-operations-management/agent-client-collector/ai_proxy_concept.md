---
title: AI Proxy
description: AI Proxy gives customers visibility and control over AI traffic leaving managed endpoints. It intercepts outbound calls to AI providers, attributes each call to the originating process, and streams structured events to the AI Control Tower \(AICT\) on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/agent-client-collector/ai\_proxy\_concept.html
release: brazil
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2026-10-08"
reading_time_minutes: 1
breadcrumb: [AI Control Tower, Agent Client Collector, IT Operations Management]
---

# AI Proxy

AI Proxy gives customers visibility and control over AI traffic leaving managed endpoints. It intercepts outbound calls to AI providers, attributes each call to the originating process, and streams structured events to the AI Control Tower \(AICT\) on your ServiceNow instance.

## AI Proxy - Overview

AI Proxy operates as a lightweight HTTPS proxy embedded inside your existing Agent Client Collector \(ACC\). You activate AI Proxy through a configuration flag during installation. AI Proxy intercepts outbound calls to AI providers and attributes each call to the originating process. The proxy streams structured events to AICT on your ServiceNow instance. Non-AI traffic flows through without inspection.

## AI provider classification

After detecting AI traffic, the AI Proxy enforces policies based on your organization's classification of AI providers.

-   **Authorized LLM providers**

    These providers your organization approves for use under organizational policies. AI Proxy forwards traffic to these providers after policy inspection and enforcement.

-   **Unauthorized LLM providers**

    These providers your organization does not approve. AI Proxy blocks traffic to unauthorized providers when it detects their use.


## Policy enforcement and monitoring

AI Proxy tracks AI activities by intercepting and monitoring AI-related traffic. The system detects policy violations in real time. Your ServiceNow instance syncs governance policies for applicable devices and users. AI Proxy then sends this data to ServiceNow, where the system maps the data to users, devices, and departments to provide comprehensive insights into AI usage across your organization.

