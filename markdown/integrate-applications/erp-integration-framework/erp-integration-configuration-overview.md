---
title: Configuring Zero Copy Connector for ERP
description: Install Zero Copy Connector for ERP \(Enterprise Resource Planning\) to configure connections to ERP systems.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-integration-configuration-overview.html
release: brazil
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-08-05"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, configuration, connection]
breadcrumb: [Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Configuring Zero Copy Connector for ERP

Install Zero Copy Connector for ERP \(Enterprise Resource Planning\) to configure connections to ERP systems.

## Connecting to an instance

Zero Copy Connector for ERP uses basic authentication. After you configure a connection, you can read and update the ERP system and create records with Zero Copy Connector for ERP using ERP models. You can also create remote tables and extraction tables.

## Connecting to multiple instances

The number of ERP connections you can have per ServiceNow instance depends on your license.

-   **[Requirements for installing Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-installation.md)**  
Before you install Zero Copy Connector for ERP \(Enterprise Resource Planning\), you must complete several configurations on both the ERP system and the ServiceNow AI Platform.
-   **[Install Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/install-erp-integration.md)**  
Install Zero Copy Connector for ERP from the ServiceNow Store, so that you can connect to SAP and other ERP systems and start building models on the ServiceNow AI Platform.
-   **[Requirements for using AI in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prereqs-for-ai.md)**  
Before you use ServiceNow Otto in Zero Copy Connector for ERP, confirm that your instance has the required license, plugins, and roles.
-   **[Install the ServiceNow Otto for Zero Copy Connector plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-install-the-erp-ai-plugin.md)**  
Install the ServiceNow Otto for Zero Copy Connector plugin \(sn\_erp\_ai\) to add ServiceNow Otto skills, agentic workflows, and AI agents to Zero Copy Connector for ERP.
-   **[Prepare ServiceNow Otto for agentic workflows and AI agents](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-prepare-otto-for-erp-agentic-workflows.md)**  
Turn on ServiceNow Otto for Virtual Agent and activate the required conversational skills. Confirm an active LLM connection before you use the Explore ERP models agentic workflow or the OData Service Recommender AI agent.
-   **[View and deactivate ERP skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-activate-and-manage-erp-skills.md)**  
View the ERP data discovery and ERP data query skills in Otto admin, and deactivate a skill if necessary.
-   **[Set access controls for ERP skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erpc-set-access-for-erp-skills.md)**  
Choose whether any authenticated user or only users with specific roles can use the ERP data discovery and ERP data query skills.
-   **[Connecting Zero Copy Connector for ERP to SAP ECC and SAP S/4HANA](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-connect-to-sap.md)**  
Connect Zero Copy Connector for ERP to an SAP ECC, SAP S/4HANA, or SAP S/4HANA Cloud system so that you can build models that use its data.
-   **[Oracle E-Business Suite support in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-overview.md)**  
Zero Copy Connector for ERP reads business data from Oracle E-Business Suite \(EBS\) through REST services, without copying the data into ServiceNow.
-   **[Obtaining data from SAP SuccessFactors using OData V2 APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/obtain-data-from-successfactors-using-odata-v2-apis.md)**  
Access talent management data from SAP SuccessFactors using OData V2 APIs.
-   **[Obtaining data from Workday using REST APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/obtain-data-from-workday-using-rest-api.md)**  
Access data from Workday using REST APIs.
-   **[Obtaining data from Workday using RaaS reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/obtain-data-from-workday-using-raas.md)**  
Workday Reports as a Service \(RaaS\) exposes a Workday custom report as a callable endpoint, so you can obtain report data that no standard Workday API returns.
-   **[Connecting to other ERP systems using REST](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-use-rest.md)**  
Extract data securely from an ERP with REST for use in remote tables and extraction tables.
-   **[Zero Copy Connector for ERP roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-roles.md)**  
Zero Copy Connector for ERP roles give team members the access they must have to configure ERP systems, build models, or read ERP data.
-   **[Protecting personally identifiable data in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-and-security.md)**  
Learn how Zero Copy Connector for ERP protects personally identifiable data from your ERP systems, beyond role-based security and access control.
-   **[Working with ERP systems in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-work-with-systems.md)**  
A Zero Copy Connector for ERP \(Enterprise Resource Planning\) system represents a connection to a section of your ERP system, such as sales orders or vendor invoices.
-   **[Extracting and transforming ERP data with Zero Copy Connector for ERP extraction tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-canvas-extraction-tables.md)**  
Use ERP extraction tables in Zero Copy Connector for ERP to schedule processes that extract large volumes of ERP data into local tables on the ServiceNow AI Platform. Then the data is transformed with table maps and can be used in ERP models and applications.

**Parent Topic:**[Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/erp-integration-framework/erp-integration-overview.md)

