---
title: Configuring the Source-to-Pay integration with SAP ECC and SAP S4 HANA
description: Integrate the ServiceNow instance and SAP ECC and SAP S4 HANA by creating a custom OAuth application in SAP ECC and SAP S4 HANA to authenticate ServiceNow requests.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Source-to-Pay integration with SAP ECC and SAP S4 HANA, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Configuring the Source-to-Pay integration with SAP ECC and SAP S4 HANA

Integrate the ServiceNow instance and SAP ECC and SAP S4 HANA by creating a custom OAuth application in SAP ECC and SAP S4 HANA to authenticate ServiceNow requests.

## Application set up

Verify that you have performed the following:

-   Activated the Source-to-Pay integration with the SAP ECC and SAP S4 HANA application from ServiceNow Store. This automatically activates the SAP ECC and SAP S4 HANA Spoke.
-   Set up the Spoke:
    -   [Set up the SAP ECC RFC spoke](https://www.servicenow.com/docs/csh?topicname=setup-sap-ecc-rfc&amp;amp;amp;version=yokohama&amp;amp;amp;pubname=yokohama-integrate-applications)
    -   [Setup the SAP S4 HANA Public Cloud spoke](https://www.servicenow.com/docs/csh?topicname=setup-sap-s4hana-cloud-spk&amp;amp;amp;version=yokohama&amp;amp;amp;pubname=yokohama-integrate-applications)
    -   [Set up SAP S4 HANA OData spoke](https://www.servicenow.com/docs/csh?topicname=set-up-sap-s4-hana-odata-spoke&amp;amp;version=yokohama&amp;amp;pubname=yokohama-integrate-applications)
-   Activated the Source-to-Pay integration framework from ServiceNow Store. The Source-to-Pay integration with SAP ECC and SAP S4 HANA uses the Source-to-Pay integration framework to pull tasks from SAP ECC and SAP S4 HANA into ServiceNow. For more information on the Source-to-Pay integration framework, see [Source-to-Pay integration framework](sap-integration-overview-2.md).


## Primary Data Integration with SAP ECC and SAP S4 HANAs' Dependencies

Install the following dependencies of Primary Data integration with SAP ECC and SAP S4 HANA. When you install the plugin, all the dependencies get installed automatically. All primary data are synchronized based on the configurable scheduled job Fetch Spend Primary Data.

Run the Trigger SAP ECC and SAP S4 HANA Integration that pulls tasks into ServiceNow. For more information, see [Use schedule flows in SAP ECC and SAP S4 HANA](using-schedule-flows-sap.md).

|App name|Plugin ID|
|--------|---------|
|SAP ECC IDOC Spoke|sn\_sap\_ecc\_idoc\_sp|
|Source-to-pay Common Architecture|sn\_shop|
|ERP Integration Framework|sn\_fcms\_intg|
|Utility Spoke|sn\_utility\_spoke|
|SAP ECC RFC Spoke|sn\_sap\_ecc\_rfc\_spo|
|Supplier Common Architecture|sn\_slm|
|SAP S4 HANA Spoke|sn\_hana\_odata\_spk|

## Supplier Lifecycle Operations Integration Dependencies with SAP ECC and SAP S4 HANA

Install the following dependencies of Supplier Lifecycle Operations integration with SAP ECC and SAP S4 HANA. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with SAP ECC and SAP S4 HANA|sn\_sap\_data\_int|
|ERP Integration Framework|sn\_fcms\_intg|
|Finance Common Architecture|sn\_fin|

## Sourcing and Procurement Operations Integration Dependencies with SAP ECC and SAP S4 HANA

Install the following dependencies of Sourcing and Procurement Operations integration with SAP ECC and SAP S4 HANA. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with SAP ECC and SAP S4 HANA|sn\_sap\_data\_int|
|ERP Integration Framework|sn\_fcms\_intg|
|Source-to-pay Common Architecture|sn\_shop|
|SAP S4 HANA RFC Spoke|sn\_sap\_s4\_hana\_rfc|
|SAP ECC IDOC Spoke|sn\_sap\_ecc\_idoc\_sp|

## Accounts Payable Operations Integration Dependencies with SAP ECC and SAP S4 HANA

Install the following dependencies of Accounts Payable Operations integration with SAP ECC and SAP S4 HANA. When you install the plugin, all the dependencies get installed automatically.

|App name|Plugin ID|
|--------|---------|
|Primary Data Integration with SAP ECC and SAP S4 HANA|sn\_sap\_data\_int|
|ERP Integration Framework|sn\_fcms\_intg|
|Source-to-pay Common Architecture|sn\_shop|
|SAP S4 HANA RFC Spoke|sn\_sap\_s4\_hana\_rfc|
|SAP ECC IDOC Spoke|sn\_sap\_ecc\_idoc\_sp|

-   **[ERP Source Configuration for SAP ECC and SAP S4 HANA](erp-source-configuration-sap.md)**  
Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to automatically post purchase order, receipt, invoice, and download primary data from the ERP.
-   **[Define ERP source configuration for SAP ECC and SAP S4 HANA](../task/define-erp-source-sap.md)**  
ERP source configuration determines the ERP source to which your ERP system connects. Map the integration payload with the SAP ECC and SAP S4 HANA tables.
-   **[Configure integration services for SAP ECC and SAP S4 HANA](../task/configure-service-maps-sap.md)**  
For configuring integration services, provide the connection end point and the SAP ECC and SAP S4 HANA ERP credentials that you set up for your authentication profile. Also, create a separate integration service record for each service request that you want to customize.
-   **[Look up primary data in SAP ECC and SAP S4 HANA](look-up-primary-data-sap.md)**  
You can run a job to look up primary data \(for example, Currencies\) from different ERP sources into ServiceNow.
-   **[Manually trigger flows or subflows in SAP ECC and SAP S4 HANA \(Inbound\)](../task/manually-trigger-subflows-sap.md)**  
You can manually trigger flows or subflows in SAP ECC and SAP S4 HANA on demand. Follow these steps to manually trigger a flow or subflow.
-   **[Scheduled jobs to look up primary data in SAP ECC and SAP S4 HANA](scheduled-jobs-to-primary-data-sap.md)**  
You can schedule on-demand jobs to be run at specific intervals of time to fetch primary data from different SAP ECC and SAP S4 HANA ERP sources into ServiceNow.

**Parent Topic:**[Source-to-Pay integration with SAP ECC and SAP S4 HANA](source-to-pay-sap-integration.md)

