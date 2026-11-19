---
title: Certificate renewal AI agent
description: Find certificates that are about to expire and renew them by describing what you want in natural language, or renew a specific certificate directly from its record.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-cert-renewal-ai-agent.html
release: zurich
product: Now Assist for IT Operations Management
classification: now-assist-for-it-operations-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Use agentic AI, ServiceNow Otto for ITOM, IT Operations Management]
---

# Certificate renewal AI agent

Find certificates that are about to expire and renew them by describing what you want in natural language, or renew a specific certificate directly from its record.

The certificate renewal AI agent is part of AI Agents for Discovery. You interact with it from the AI panel in Certificate Management workspace. You can use the agent in two ways:

-   From a certificate record. When you open the AI panel while viewing a certificate, the agent picks up that certificate as context and offers to renew it.
-   From a prompt. Describe the certificates you want to renew, and the agent returns a list of matching certificates for you to confirm before renewal begins. In either case, the agent creates a certificate renewal task and gives you a link to the task record so that you can track progress.

Before you use the agent, configure your system for automatic certificate renewal:

1.  [Configure MID Server for automatic certificate renewal](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/configure-mid-server-automatic-cert-renewal.md)
2.  [Add required applications and capabilities to your MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery/add-req-apps-capabilities-to-mid-server.md)

-   **[Find and renew expiring certificates using the AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/discover-renew-certs-about-to-expire.md)**  
Describe the certificates that you want to renew, and the certificate renewal AI agent finds them and renews them after you confirm.
-   **[Renew certificates using the AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/automatically-renew-cert-now-assist.md)**  
Renew a specific certificate by opening it and asking the certificate renewal AI agent to renew it.
-   **[Use AI to renew certificate set to renew manually](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/renew-cert-set-to-renew-manually.md)**  
Use the certificate renewal AI agent to immediately renew certificates set to renew manually.

**Parent Topic:**[Use agentic AI in ServiceNow Otto for ITOM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/now-assist-for-it-operations-management/now-assist-itom-ai-agent-workflows.md)

