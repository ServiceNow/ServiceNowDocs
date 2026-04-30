---
title: Use an SNC connection in Zero Copy Connector for ERP
description: Use Secure Network Communication \(SNC\) for data communications between ServiceNow MID Server and SAP systems.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring Zero Copy Connector for ERP, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Use an SNC connection in Zero Copy Connector for ERP

Use Secure Network Communication \(SNC\) for data communications between ServiceNow MID Server and SAP systems.

Secure Network Communication \(SNC\) is a security feature in SAP systems that ensures that the data transmitted over the network is protected by encryption, authentication, and integrity checks. SNC provides a secure communication pathway between SAP systems and external components, safeguarding sensitive information from unauthorized access, tampering, and eavesdropping.

SNC is used to:

-   Enhance security: By encrypting the data transmitted over the network, SNC prevents unauthorized access and ensures confidentiality.
-   Ensure data integrity: Integrity checks ensure that the data is not altered during transmission, protecting against tampering.
-   Authenticate communication parties: SNC provides strong authentication methods to verify the identities of the entities involved in the communication.

## SNC Architecture

SNC operates within the SAP NetWeaver Application Server \(AS\) environment. It utilizes the GSS-API \(Generic Security Services Application Program Interface\) to integrate with external security libraries and products. Commonly used security libraries include Kerberos-based solutions and SAP's own Secure Login Library \(SLL\).

-   **[Configure an SNC connection in Zero Copy Connector for ERP](../task/erpc-configure-an-snc-connection-in-erp-canvas.md)**  
Learn how to set up SNC, including preparing the environment, configuring the SAP system, and testing the configuration.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](erp-integration-configuration-overview.md)

