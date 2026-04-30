---
title: ERP source configuration for SAP Ariba
description: Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to post purchase order, receipt, invoice, and download primary data automatically from the ERP system.
locale: en-US
release: xanadu
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-06-23"
reading_time_minutes: 3
breadcrumb: [Configuring the Source-to-Pay integration with SAP Ariba, Source-to-Pay integration with SAP Ariba, Source-to-Pay integration with third-party applications, Source-to-Pay Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# ERP source configuration for SAP Ariba

Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to post purchase order, receipt, invoice, and download primary data automatically from the ERP system.

ERP source configuration enables the implementation of specific logic to populate values pertinent to third-party ERP systems. It includes all service mappings defined between Source-to-Pay \(S2P\) and the third-party ERP system. If multiple ERP sources exist, they’re stored as distinct ERP source entries with their corresponding service mappings.

To meet specific requirements, you can customize the service-mapping logic by modifying the relevant service element map entry within the service map record. For organizations using multiple ERP systems, an ERP Source field has been incorporated into the tables to accurately identify the respective integrated ERP system.

The ERP source configuration for SAP Ariba enables customers to establish multiple SAP Ariba instances. Each instance is identified by a distinct source, and the connection alias for each instance must be unique.

## Prerequisites

Before you start the integration configuration, complete the following tasks.

-   Add the following roles to the Integration user:
    -   sn\_fcms\_intg.admin
    -   sn\_spend\_intg.admin
-   Get the following details from the ERP team:
    -   ERP integration user credentials.
    -   REST API details based on your ERP system you're using for the integration.

**Note:** If the application must support multiple ERP instances, configure Source-to-Pay to integrate with each ERP instance separately.

## ERP Source Configuration

To configure the ERP Source for SAP Ariba, perform the following steps:

1.  Define the ERP source that you want to integrate with the SAP Ariba integration.
2.  Create a basic authentication profile that can be used for the web service integration with SAP Ariba
3.  Register the SAP Ariba integration username and password to create the authentication profile and associate it to service maps.
4.  Define the source configuration for ERP source. The ERP source configuration determines the ERP source to which your ERP system connects. For more information, see [Define ERP source configuration for SAP Ariba](define-erp-source-sap-ariba.md).
5.  Configure service maps for the following entities:
    -   **Legal Entities**

        Set up subflows for the source configuration to lookup legal entities or company code details from SAP Ariba.

    -   **FX Currency Rates**

        Set up subflows for the source configuration to lookup FX rates from SAP Ariba.

    -   **Purchasing Orgs**

        Set up subflows for the source configuration to lookup purchasing organizations from SAP Ariba.

    -   **Currencies**

        Set up subflows for the source configuration to lookup currencies from SAP Ariba.

    -   **Payment Terms**

        Set up subflows for the source configuration to lookup payment terms from SAP Ariba.

    -   **GL Accounts**

        Set up subflows for the source configuration to lookup GL accounts from SAP Ariba.

    -   **Cost Centers**

        Set up subflows for the source configuration to lookup cost centers from SAP Ariba.

    -   **Departments**

        Set up subflows for the source configuration to lookup departments from SAP Ariba.

    -   **Suppliers**

        Set up subflows for the source configuration to lookup suppliers from SAP Ariba

    -   **Invoices**

        Set up subflows for the source configuration to lookup invoices from SAP Ariba.


![ERP Source Configuration for SAP Ariba](../image/sap-ariba-source-config.png "ERP Source Configuration for SAP Ariba")

**Parent Topic:**[Configuring the Source-to-Pay integration with SAP Ariba](configuring-source-to-pay-sap-ariba-integration.md)

**Related topics**  


[Define ERP source configuration for SAP Ariba](define-erp-source-sap-ariba.md)

[Configure service maps for SAP Ariba](configure-service-maps-sap-ariba.md)

[Look up primary data in SAP Ariba](look-up-primary-data-sap-ariba.md)

