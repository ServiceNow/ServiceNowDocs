---
title: Configure Triage legal requests agentic workflow
description: You can configure the Triage legal requests agentic workflow in the ServiceNow Otto for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer when a legal fulfiller or group manager confirms the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/now-assist-for-legal-service-delivery/conf-transfer-legal-request-agent.html
release: zurich
product: Now Assist for Legal Service Delivery
classification: now-assist-for-legal-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Now Assist, ServiceNow Otto, generative AI, Configure AI Agents]
breadcrumb: [Configure, ServiceNow Otto for Legal Service Delivery \(LSD\), Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure Triage legal requests agentic workflow

You can configure the Triage legal requests agentic workflow in the ServiceNow Otto for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer when a legal fulfiller or group manager confirms the request.

You must complete the following tasks to activate and use the Triage legal requests agentic workflow:

1.  Install the Legal Service Delivery - Prime plugin \(sn\_lg\_ai\_prime\).
2.  Confirm the ServiceNow Otto panel is turned on. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/intelligent-experiences/activate-now-assist-panel.md).
3.  Confirm the **ServiceNow Otto Panel - Platform \(default\)** assistant in the CI Admin Experience is turned on. For more information, see .
4.  Configure AI Search. For more information, see [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/configuring-ais.md).
5.  Activate the Triage Legal request use case business rule to activate the Triage legal requests agentic workflow. For more information, see [Activate the business rule for the Triage legal requests agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-legal-service-delivery/lsd-agentic-config-BR.md).
6.  Include the legal practice application tables for AI Search indexing. For more information, see [Add legal request tables for data indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/employee-service-management/now-assist-for-legal-service-delivery/add-tables-legal-requests.md).

**Important:** The ServiceNow Otto panel lists the following skills that are required for the Triage legal requests agentic workflow:

-   Get category of the legal request
-   Triage Legal Request Capability
-   Triage Legal Request AI search

You can access the ServiceNow Otto panel by navigating to **All** &gt; **Admin Center** &gt; **AI Admin Hub** &gt; **AI Skills** &gt; **Employee** &gt; **LSD**.

The skills are available in an active state in the base system and should not be modified.

