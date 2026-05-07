---
title: Create and change SAP business entities with IDoc
description: Work with SAP business entities that can only be created or changed using IDoc.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [erp, integration, canvas, data hub, sap, zero, copy, connector, entity, idoc]
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Create and change SAP business entities with IDoc

Work with SAP business entities that can only be created or changed using IDoc.

SAP still has some business entities that can only be created or changed using IDoc. In Zero Copy Connector for ERP \(Enterprise Resource Planning\), you can add IDoc entities to model operations and configure outbound messages. Monitor the asynchronous processing to obtain information about IDoc status and the business entity created or updated.

**Note:** IDoc can only be used with create or update operations, not read operations.

For details about IDoc, see the [SAP support website IDoc information](https://help.sap.com/docs/SAP_DATA_SERVICES/df959412681b4619a38f03ff90207e6b/577aa1b66d6d1014b3fc9283b0e91070.html).

You must have the sn\_erp\_integration.erp\_admin role to create and edit models.

Complete the following steps to work with IDoc entities in Zero Copy Connector for ERP:

1.  Manage partner profiles. For more information, see [View Zero Copy Connector for ERP partner profile information](../task/view-erp-system-partner-profile-information.md).
2.  Explore the API for interacting with Zero Copy Connector for ERP models. For detailed information and examples for using the API, see [sn\_erp\_integration API - Scoped, Global](https://www.servicenow.com/docs/access?context=sn_erp_integrationBothAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US).
3.  Add an IDoc entity to a model. For more information, see [Add an IDoc entity to a model operation](../task/add-an-idoc-entity-to-a-model-operation.md).
4.  Create an outbound message. For more information, see [Create an IDoc outbound message configuration in Zero Copy Connector for ERP](../task/create-an-idoc-outbound-message-configuration.md).
5.  Manage IDoc outbound messages. For more information, see [View and troubleshoot IDoc messages](../task/view-and-troubleshoot-idoc-messages.md).

**Note:** The Zero Copy Connector for ERP Monitor includes IDoc information on the asynchronous tabs. For more information about the Monitor, see [Monitor Zero Copy Connector for ERP logged extraction and remote lookup transactions](../task/monitor-erp-data-hub-logged-extraction-and-remote-lookup-transactions.md).

-   **[Create an IDoc outbound message configuration in Zero Copy Connector for ERP](../task/create-an-idoc-outbound-message-configuration.md)**  
Use IDoc outbound message configurations to create and change some SAP business entities in Zero Copy Connector for ERP \(Enterprise Resource Planning\).
-   **[View and troubleshoot IDoc messages](../task/view-and-troubleshoot-idoc-messages.md)**  
When working with SAP business entities that can only be created or changed using IDoc, view outbound messages for details and troubleshooting information in Zero Copy Connector for ERP \(Enterprise Resource Planning\).

**Parent Topic:**[Add an entity to a model](add-an-entity-to-model.md)

