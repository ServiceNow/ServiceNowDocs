---
title: ERP Source Configuration for Coupa
description: Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to post purchase order, receipt, invoice, and download primary data from the ERP automatically.
locale: en-US
release: yokohama
product: Source-to-Pay Integration Framework
classification: source-to-pay-integration-framework
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Source-to-Pay integration with Coupa, Integration with third-party applications, Integrations, Source-to-Pay Operations, Finance and Supply Chain]
---

# ERP Source Configuration for Coupa

Configure your Source-to-Pay \(S2P\) instance to support inbound and outbound integration with your ERP system. This integration configuration enables you to post purchase order, receipt, invoice, and download primary data from the ERP automatically.

ERP source configuration includes all service mappings defined between Source-to-Pay \(S2P\) and the third-party ERP system. In cases where multiple ERP sources exist, they’re stored as distinct ERP source entries with their corresponding service mappings.

To meet specific requirements, you can modify the service-mapping logic by updating the relevant service element map entry within the service map record. For organizations using multiple ERP systems, an ERP Source field has been incorporated into the tables to ensure accurate identification of the respective integrated ERP system.

The ERP source configuration for Coupa enables customers to establish multiple Coupa instances. Each instance is identified by a distinct source, and the connection alias for each instance must be unique.

## Prerequisites

Before you start the integration configuration, you must get the following details from the ERP team:

-   ERP integration user credentials.
-   SOAP or REST API details based on your ERP system and the type of web services you’re using for the integration.
-   Roles to be added for the Integration users.

## ERP Source Configuration

To perform the ERP Source configuration for Coupa, perform the following steps:

1.  Define the ERP source that you want to integrate with Coupa integration. For more information, see [Define an ERP source configuration for Coupa](../task/define-erp-source-coupa.md).
2.  Create a basic authentication profile that can be used for web service integration with Coupa.
3.  Register the Coupa integration username and password to create the authentication profile and associate it to service maps.
4.  Define source configuration for ERP source.

    The ERP source configuration determines the ERP source to which your ERP system connects. For more information, see [Define an ERP source configuration for Coupa](../task/define-erp-source-coupa.md).

5.  Configure service maps for the required entities. For more information, see [Configure integration services for Coupa](../task/configure-service-maps-coupa.md).

    ![ERP Source Configuration of Coupa](../image/coupa-source-config.png "ERP Source Configuration of Coupa")


You have configured the ERP source for Coupa.

**Parent Topic:**[Configure Source-to-Pay integration with Coupa](configuring-source-to-pay-coupa-integration.md)

**Related topics**  


[Define an ERP source configuration for Coupa](../task/define-erp-source-coupa.md)

[Configure integration services for Coupa](../task/configure-service-maps-coupa.md)

[Activate the schedule flows](../task/activate-schedule-flows-coupa.md)

[Looking up primary data in Coupa](look-up-primary-data-coupa.md)

