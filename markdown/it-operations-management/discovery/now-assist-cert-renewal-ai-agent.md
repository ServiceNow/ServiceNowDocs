---
title: Certificate renewal AI agent
description: Find certificates that are about to expire and renew them by describing what you want in natural language, or renew a specific certificate directly from its record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery/now-assist-cert-renewal-ai-agent.html
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Automated certificate renewal, Certificate Inventory and Management, ITOM Visibility, IT Operations Management]
---

# Certificate renewal AI agent

Find certificates that are about to expire and renew them by describing what you want in natural language, or renew a specific certificate directly from its record.

The certificate renewal AI agent is part of AI Agents for Discovery. You interact with it from the AI panel in Certificate Management workspace. You can use the agent in two ways:

-   From a certificate record. When you open the AI panel while viewing a certificate, the agent picks up that certificate as context and offers to renew it.
-   From a prompt. Describe the certificates you want to renew, and the agent returns a list of matching certificates for you to confirm before renewal begins. In either case, the agent creates a certificate renewal task and gives you a link to the task record so that you can track progress.

Before you use the agent, configure your system for automatic certificate renewal:

1.  [Configure MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add the required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

