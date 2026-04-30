---
title: Integration settings on Source-to-Pay side
description: Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to automatically post purchase order, receipt, invoice, and download primary data from the ERP.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Source-to-Pay integration framework, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# Integration settings on Source-to-Pay side

Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to automatically post purchase order, receipt, invoice, and download primary data from the ERP.

Before you start the integration configuration, you must complete the following tasks.

-   Add the following roles to the Integration user:
    -   Import\_transformer
    -   Soap
-   Get the following information from the ERP team:
    -   ERP integration user credentials.
    -   SOAP or REST API details based on your ERP system and the type of web services you are using for the integration.

**Note:** If the application needs to support multiple ERP instances, configure S2P to integrate with each ERP instance separately.

1.  Define an ERP source.

    Define the ERP source that you want to integrate with Procurement Service Management. This information is required for any primary data. For more information, see [ERP source](erp-source.md) and [Primary data integration](master-data-integration.md).

2.  Set up the authentication profile.

    Create a basic authentication profile that can be used for web service integration with ERP. Register the ERP integration username and password to create the authentication profile and associate it to service maps. For more information, see [Set up the authentication profile](../task/setup-authentication-profile-erp-intg.md).

3.  Define source configuration for ERP.

    ERP source configuration determines the ERP source to which your ERP system connects. For more information, see [ERP source configuration](erp-source-configuration.md) and [Define ERP source configuration for Source-to-Pay](../task/define-erp-source-config-psm.md).

4.  Configure service maps for the following entities:

    -   Post purchase order.

        Set up web services for the source configuration to post purchase orders to ERP.

    -   Post receipt.

        Set up web services for the source configuration to post receipts to ERP.

    -   Post invoice.

        Set up web services for the source configuration to post invoices to ERP.

    -   Fetch supplier.

        Set up web services for the source configuration to fetch supplier updates from ERP.

    -   Fetch cost center.

        Set up web services for the source configuration to fetch cost center updates from ERP.

    -   Fetch purchasing entity.

        Set up web services for the source configuration to fetch purchasing entity updates from ERP.

    -   Fetch general ledger account.

        Set up web services for the source configuration to fetch general ledger account updates from ERP.

    -   Fetch asset category.

        Set up web services for the source configuration to fetch asset category updates from ERP.

    -   Fetch material group.

        Set up web services for the source configuration to fetch material group updates from ERP.

    **Note:** For configuring each of these service maps, provide the connection end point and the ERP credentials that you set up for your authentication profile. Also, create a separate web service record for each service request that you want to customize.

    For more information, see [Configure service maps for Source-to-Pay](../task/configure-service-maps-psm-erp.md).

5.  Configure scheduled job to synchronize primary data updates from ERP.

    Set up the interval in the Fetch Spend Primary Data scheduled job to periodically synchronize primary data updates from the ERP, for posting services to work.

6.  Load data to ERP user mapping table.

    Set up S2P and ERP User ID mapping for the integration to work. The mapping is maintained for all active users who have the procurement buyer role in ERP. These users should be used in the requisition assignment rule. For more information, see [Load data to ERP user mapping table for Source-to-Pay](../task/load-data-erp-user-mapping-psm.md).

7.  Map the following entities:
    -   Purchasing entity.

        Map legal entity to the downloaded purchasing entity in the purchasing entity table.

    -   Asset category.

        Map capitalization policy to the downloaded asset category in the asset category mapping table.

    -   Material group.

        Map model category to the downloaded material group in the material group mapping table.

    -   Delivery address.

        Map location reference in the delivery location table to ERP address code in the address mapping table.

    -   ERP plant.

        Map ERP plant id to the corresponding ERP location in the address mapping table. Use the **ERP address identifier 1** field for this mapping.


