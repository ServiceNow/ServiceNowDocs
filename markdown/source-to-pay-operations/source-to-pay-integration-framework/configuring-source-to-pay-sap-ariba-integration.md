---
title: Configure the Source-to-Pay integration with SAP Ariba
description: Integrate the ServiceNow instance and SAP Ariba using the SSH, Basic Auth, OAuth 2.0, and API Key credentials SAP Ariba to authenticate ServiceNow requests.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Source-to-Pay integration with SAP Ariba, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configure the Source-to-Pay integration with SAP Ariba

Integrate the ServiceNow instance and SAP Ariba using the SSH, Basic Auth, OAuth 2.0, and API Key credentials SAP Ariba to authenticate ServiceNow requests.

## Application set up

-   Activate the Source-to-Pay integration with the SAP Ariba application from the ServiceNow Store. This automatically activates the SAP Ariba Spoke.
-   Set up [SAP Ariba Spoke](https://www.servicenow.com/docs/bundle/yokohama-integrate-applications/page/administer/integrationhub-store-spokes/concept/sap-ariba-spoke.html).
-   Activate the Source-to-Pay integration framework from the ServiceNow Store. Source-to-Pay integration with SAP Ariba uses the Source-to-Pay integration framework to pull tasks from SAP Ariba into ServiceNow. For more information on the Source-to-Pay integration framework, see [Source-to-Pay integration framework](source-to-pay-integration-framework.md).


## Primary Data Integration with SAP Ariba Dependencies

Install the following dependencies of Primary Data integration with SAP Ariba. When you install the plugin \(sn\_ariba\_data\_int\), the dependencies are installed automatically.

|App name|Plugin ID|
|--------|---------|
|ERP Integration Framework|sn\_fcms\_intg|
|Source-to-pay Common Architecture|sn\_shop|
|Supplier Common Architecture|sn\_slm|
|SAP Ariba Spoke|sn\_sap\_ariba\_spoke|

## Supplier Lifecycle Operations Integration Dependencies with SAP Ariba

Install the following dependencies of Supplier Lifecycle Operations integration with SAP Ariba. When you install the plugin, the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with SAP Ariba|sn\_ariba\_data\_int|
|Source-to-Pay Integration Framework|sn\_spend\_intg|
|Primary Data Integration with SAP Ariba|sn\_utility\_spoke|
|Finance Common Architecture|sn\_fin|
|ERP Integration Framework|sn\_fcms\_intg|
|Supplier Common Architecture|sn\_slm|

## Sourcing and Procurement Operations Integration Dependencies with SAP Ariba

Install the following dependencies of Sourcing and Procurement Operations integration with SAP Ariba. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with SAP Ariba|sn\_ariba\_data\_int|
|Sourcing and Purchasing Automation|sn\_pr|
|Source-to-Pay Integration Framework|sn\_spend\_intg|

## Accounts Payable Operations Integration Dependencies with SAP Ariba

Install the following dependencies of Accounts Payable Operations integration with SAP Ariba. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with SAP Ariba|sn\_ariba\_data\_int|
|Accounts Payable Invoice Processing|sn\_ap\_apm|
|Source-to-Pay Integration Framework|sn\_spend\_intg|

-   **[ERP source configuration for SAP Ariba](erp-source-configuration-sap-ariba.md)**  
Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to post purchase order, receipt, invoice, and download primary data automatically from the ERP system.
-   **[Configure integration services for SAP Ariba](configure-service-maps-sap-ariba.md)**  
For configuring integration services, provide the connection end point and the SAP Ariba credentials that you set up for your authentication profile. Also, create a integration service record for each entity you want to customize.
-   **[Look up primary data in SAP Ariba](look-up-primary-data-sap-ariba.md)**  
You can run a job to look up primary data from different ERP sources into ServiceNow.

**Parent Topic:**[Source-to-Pay integration with SAP Ariba](source-to-pay-integration-sap-ariba.md)

