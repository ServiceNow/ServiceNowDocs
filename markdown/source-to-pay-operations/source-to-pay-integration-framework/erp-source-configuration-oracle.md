---
title: ERP source configuration for Oracle EBS
description: Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to automatically post purchase order, receipt, invoice, and download primary data from the ERP.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Configure, Source-to-Pay integration with Oracle EBS, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# ERP source configuration for Oracle EBS

Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to automatically post purchase order, receipt, invoice, and download primary data from the ERP.

ERP source configuration enables the implementation of specific logic to populate values pertinent to third-party ERP systems. It includes all service mappings defined between Source-to-Pay \(S2P\) and the third-party ERP system. In cases where multiple ERP sources exist, they’re stored as distinct ERP source entries with their corresponding service mappings.

To meet specific requirements, you can modify the service-mapping logic by updating the relevant service element map entry within the service map record. For organizations using multiple ERP systems, an ERP Source field has been incorporated into the tables to ensure accurate identification of the respective integrated ERP system.

The ERP source configuration for Oracle EBS enables customers to establish multiple Oracle instances. Each instance is identified by a distinct source, and the connection alias for each instance must be unique.

## Prerequisites

Before you start the integration configuration, you must complete the following tasks.

-   Add the following roles to the Integration user:
    -   Import\_transformer
    -   SOAP
-   Get the following details from the ERP team:
    -   ERP integration user credentials.
    -   SOAP or REST API details based on your ERP system and the type of web services you’re using for the integration.

**Note:** If the application must support multiple ERP instances, configure Source-to-Pay to integrate with each ERP instance separately.

## ERP Source Configuration

To perform the ERP Source configuration for Oracle EBS, follow these steps:

1.  Define the ERP source that you want to integrate with Oracle EBS integration.
2.  Create a basic authentication profile that can be used for web service integration with Oracle EBS.
3.  Register the Oracle EBS integration username and password to create the authentication profile and associate it to service maps.
4.  Define source configuration for ERP source. The ERP source configuration determines the ERP source to which your ERP system connects. For more information, see [Define ERP source configuration for Oracle EBS](../task/define-erp-source-oracle.md).
5.  Configure service maps for the following entities:

    -   **Cost Centers**

        Set up subflows for the source configuration to lookup cost centers from Oracle EBS.

    -   **Product Models**

        Set up subflows for the source configuration to lookup product models from Oracle EBS.

    -   **Payment Terms**

        Set up subflows for the source configuration to lookup payment terms from Oracle EBS.

    -   **Purchasing Orgs**

        Set up subflows for the source configuration to lookup purchasing orgs from Oracle EBS.

    -   **Departments**

        Set up subflows for the source configuration to lookup departments from Oracle EBS.

    -   **GL Accounts**

        Set up subflows for the source configuration to lookup GL accounts from Oracle EBS.

    -   **Currencies**

        Set up subflows for the source configuration to lookup currencies from Oracle EBS.

    -   **FX Currency Rates**

        Set up subflows for the source configuration to lookup FX rates from Oracle EBS.

    -   **Invoice Payment Details**

        Set up subflows for the source configuration to lookup invoice payment details from Oracle EBS.

    -   **Suppliers**

        Set up subflows for the source configuration to lookup suppliers from Oracle EBS.

    -   **Plant Addresses**

        Set up subflows for the source configuration to lookup plant addresses from Oracle EBS.

    -   **Legal Entities**

        Set up subflows for the source configuration to lookup legal entities or company code details from Oracle EBS.

    -   **Invoices**

        Set up subflows for the source configuration to lookup invoices from Oracle EBS.

    ![ERP Source Configuration of Oracle EBS](../image/oracle-ebs-source-config.png "ERP Source Configuration of Oracle EBS")

6.  Configure a scheduled job to synchronize primary data updates from Oracle EBS.
7.  Set up the interval in the lookup Cost Center scheduled job to periodically synchronize primary data updates from the ERP, for posting services to work.

    **Note:** Similarly, you can configure schedule jobs for the other integrations services.

8.  Load data to the Oracle EBS user-mapping table.
9.  Set up Source-to-Pay and ERP User ID mapping `(sn_fcms_intg_erp_user_map)` for the integration to work.

    The mapping is maintained for all active users who have the procurement buyer role in ERP. These users should be used in the requisition assignment rule.

    You have configured the ERP source for Oracle EBS.


**Parent Topic:**[Configure the Source-to-Pay integration with Oracle EBS](configuring-source-to-pay-oracle-ebs-integration.md)

**Related topics**  


[Define ERP source configuration for Oracle EBS](../task/define-erp-source-oracle.md)

[Configure integration services for Oracle EBS](../task/configure-service-maps-oracle-ebs.md)

[Load data to ERP user-mapping table for Oracle EBS](../task/load-data-erp-user-mapping-oracle-ebs.md)

[Look up primary data in Oracle EBS](look-up-primary-data-oracle-ebs.md)

[Scheduled jobs to look up primary data in Oracle EBS](scheduled-jobs-to-primary-data-oracle-ebs.md)

