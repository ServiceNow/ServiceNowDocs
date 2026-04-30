---
title: ERP Source Configuration for SAP
description: Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to automatically post purchase order, receipt, invoice, and download primary data from the ERP.
locale: en-US
release: australia
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Configure, Source-to-Pay integration with SAP, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# ERP Source Configuration for SAP

Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to automatically post purchase order, receipt, invoice, and download primary data from the ERP.

ERP source configuration enables the implementation of specific logic to populate values pertinent to third-party ERP systems. It includes all integration services defined between Source-to-Pay \(S2P\) and the third-party ERP system. In cases where multiple ERP sources exist, they’re stored as distinct ERP source entries with their corresponding integration services.

To meet specific requirements, you can modify the service-mapping logic by updating the relevant service element map entry within the integration service record. For organizations using multiple ERP systems, an ERP Source field has been incorporated into the tables to ensure accurate identification of the respective integrated ERP system.

## Prerequisites

Before you start the integration configuration, you must complete the following tasks.

-   Add the following roles to the Integration user:
    -   Import\_transformer
    -   SOAP
-   Get the following details from the ERP team:
    -   ERP integration user credentials.
    -   SOAP or REST API details based on your ERP system and the type of web services you are using for the integration.

**Note:** If the application needs to support multiple ERP instances, configure Source-to-Pay to integrate with each ERP instance separately.

## ERP Source Configuration

To perform the ERP Source configuration for SAP, follow these steps:

1.  Define the ERP source that you want to integrate with SAP integration.
2.  Create a basic authentication profile that can be used for web service integration with SAP.
3.  Define source configuration for ERP source. The ERP source configuration determines the ERP source to which your ERP system connects. For more information, see [Define ERP source configuration for SAP](../task/define-erp-source-sap.md).
4.  The integration services are preconfigured with the base system for the following entities:

    -   **Currencies**

        Set up subflows for the source configuration to lookup currencies from SAP.

    -   **Legal Entities**

        Set up subflows for the source configuration to lookup legal entities or company code details from SAP.

    -   **FX Currency Rates**

        Set up subflows for the source configuration to lookup FX rates from SAP.

    -   **Cost Centers**

        Set up subflows for the source configuration to lookup cost centers from SAP.

    -   **Departments**

        Set up subflows for the source configuration to lookup departments from SAP.

    -   **Payment Terms**

        Set up subflows for the source configuration to lookup payment terms from SAP.

    -   **Purchasing Orgs**

        Set up subflows for the source configuration to lookup purchasing orgs from SAP.

    -   **GL Accounts**

        Set up subflows for the source configuration to lookup GL accounts from SAP.

    -   **Plant Addresses**

        Set up subflows for the source configuration to lookup plant addresses from SAP.

    -   **Suppliers**

        Set up subflows for the source configuration to lookup suppliers from SAP.

    -   **Product Models**

        Set up subflows for the source configuration to lookup product models from SAP.

    -   **Invoices**

        Set up subflows for the source configuration to lookup invoices from SAP.

    -   **Unit of Measure**

        Set up subflows for the source configuration to lookup the base unit of measure details from SAP.

    -   **Product Categories**

        Set up subflows for the source configuration to lookup material group details from SAP.

    ![ERP Source Configuration of S4 HANA](../image/sap-integration-source-config.png "ERP Source Configuration of S4 HANA")

    **Note:** Similarly, you can select SAP ECC configuration to view the list of services.

5.  Configure a scheduled job to synchronize primary data updates from SAP.
6.  Set the time interval in the lookup Cost Center scheduled job to periodically synchronize primary data updates from the ERP, for posting services to work.

    **Note:** Similarly, you can configure schedule jobs for the other integrations services.

    You have configured the ERP source for SAP.


**Parent Topic:**[Configure the Source-to-Pay integration with SAP](configuring-source-to-pay-sap-integration.md)

**Related topics**  


[Define ERP source configuration for SAP](../task/define-erp-source-sap.md)

[Configure integration services for SAP](../task/configure-service-maps-sap.md)

[Look up primary data in SAP](look-up-primary-data-sap.md)

[Manually execute flows or subflows in SAP \(Inbound\)](../task/manually-trigger-subflows-sap.md)

[Scheduled jobs to look up primary data in SAP](scheduled-jobs-to-primary-data-sap.md)

