---
title: Configure Triage legal requests agentic workflow
description: You can configure the Triage legal requests agentic workflow in the ServiceNow Otto for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer when a legal fulfiller or group manager confirms the request.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-request-management/conf-transfer-legal-request-agent.html
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [Now Assist, ServiceNow Otto, generative AI, Configure AI Agents]
breadcrumb: [Configure AI capabilities for LSD, Configure, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure Triage legal requests agentic workflow

You can configure the Triage legal requests agentic workflow in the ServiceNow Otto for Legal Service Delivery \(LSD\) application to analyze the general legal requests, predict the appropriate legal category, and initiate a transfer when a legal fulfiller or group manager confirms the request.

You must complete the following tasks to activate and use the Triage legal requests agentic workflow:

1.  Install the Legal Service Delivery - Prime plugin \(sn\_lg\_ai\_prime\).
2.  Confirm the ServiceNow Otto panel is turned on. For more information, see [Activate the ServiceNow Otto panel standard chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/activate-now-assist-panel.md).
3.  Confirm the **ServiceNow Otto Panel - Platform \(default\)** assistant in the CI Admin Experience is turned on. For more information, see [Manage LLM virtual agents on the Assistants screen](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/conversational-interfaces/manage-llm-va.md).
4.  Configure AI Search. For more information, see [Configuring AI Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configuring-ais.md).
5.  Activate the Triage Legal request use case business rule to activate the Triage legal requests agentic workflow. For more information, see [Activate the business rule for the Triage legal requests agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/lsd-agentic-config-BR.md).
6.  Include the legal practice application tables for AI Search indexing. For more information, see [Add legal request tables for data indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/add-tables-legal-requests.md).

**Important:** The ServiceNow Otto panel lists the following skills that are required for the Triage legal requests agentic workflow:

-   Get category of the legal request
-   Triage Legal Request Capability
-   Triage Legal Request AI search

You can access the ServiceNow Otto panel by navigating to **All** &gt; **Admin Center** &gt; **AI Admin Hub** &gt; **AI Skills** &gt; **Employee** &gt; **LSD**.

The skills are available in an active state in the base system and should not be modified.

-   **[Activate the business rule for the Triage legal requests agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/lsd-agentic-config-BR.md)**  
Activate the business rules for the Triage legal requests agentic workflow in the ServiceNow Otto for Legal Service Delivery \(LSD\) application.
-   **[Add legal request tables for data indexing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/add-tables-legal-requests.md)**  
Add the legal request tables to be considered for data indexing for AI Search in the ServiceNow Otto for Legal Service Delivery \(LSD\) application. The legal request tables are indexed so that you can get relevant AI Search results for the legal records.
-   **[Configure the semantic index settings for legal request tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/create-record-legal-requests.md)**  
Configure the semantic index settings to define how AI Search indexes the content from the legal request tables in the ServiceNow Otto for Legal Service Delivery \(LSD\) application.
-   **[Add fields to the semantic index for legal records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/add-field-legal-requests.md)**  
Add the description, short description, and legal category field to the semantic index record to be indexed for a semantic search in the ServiceNow Otto for Legal Service Delivery \(LSD\) application. During AI Search, the legal records are retrieved based on the description, short description, and legal category fields that are added in the semantic index.
-   **[Add restricted caller access privileges for accessing the legal request table](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/lsd-agentic-rca-config.md)**  
Create restricted caller access \(RCA\) privileges to ensure authorized access to the legal request table in the ServiceNow Otto for Legal Service Delivery \(LSD\) application.

**Parent Topic:**[Configure ServiceNow Otto for Legal Service Delivery \(LSD\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/now-assist-lsd-configuring.md)

