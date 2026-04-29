---
title: Use an SNC \(Secure Network Communication\) connection in Zero Copy Connector for ERP
description: Use Secure Network Communication \(SNC\) for data communications between ServiceNow MID Server and SAP systems.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, security network communication, snc, security, data, communication, connection]
breadcrumb: [Configure, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Use an SNC \(Secure Network Communication\) connection in Zero Copy Connector for ERP

Use Secure Network Communication \(SNC\) for data communications between ServiceNow MID Server and SAP systems.

Secure Network Communication \(SNC\) is a security feature in SAP systems that confirms that the data transmitted over the network is protected by encryption, authentication, and integrity checks. SNC provides a secure communication pathway between SAP systems and external components, safeguarding sensitive information from unauthorized access, tampering, and eavesdropping.

SNC is used to:

-   Enhance security: By encrypting the data transmitted over the network, SNC helps prevent unauthorized access and confirms confidentiality.
-   Check data integrity: Integrity checks confirm that the data isn't altered during transmission, protecting against tampering.
-   Authenticate communication parties: SNC provides strong authentication methods to verify the identities of the entities involved in the communication.

## SNC Architecture

SNC operates within the SAP NetWeaver Application Server \(AS\) environment. It uses the GSS-API \(Generic Security Services Application Program Interface\) to integrate with external security libraries and products. Commonly used security libraries include Kerberos-based solutions and SAP's own Secure Login Library \(SLL\).

-   **[Configure an SNC connection in Zero Copy Connector for ERP](../task/erpc-configure-an-snc-connection-in-erp-canvas.md)**  
Learn how to set up SNC, including preparing the environment, configuring the SAP system, and testing the configuration.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](erp-integration-configuration-overview.md)

