---
title: Add a WADL service manually in Zero Copy Connector for ERP
description: Add an Oracle E-Business Suite \(EBS\) service to a model by supplying its Integrated SOA Gateway alias, when the service you need isn't listed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-add-a-wadl-service-manually.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-08-24"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, zero, copy, connector, oracle, ebs, wadl, service, entity]
breadcrumb: [Connecting to Oracle EBS, Configuring, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add a WADL service manually in Zero Copy Connector for ERP

Add an Oracle E-Business Suite \(EBS\) service to a model by supplying its Integrated SOA Gateway alias, when the service you need isn't listed.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Complete the following before adding a service manually:

-   Enable the **sn\_erp\_integration.enableModelModification** property. For more information, see [Install Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/install-erp-integration.md).
-   Create an Oracle EBS connection for the system. For more information, see [Create an Oracle E-Business Suite connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-create-an-oracle-ebs-connection.md).
-   Obtain the Integrated SOA Gateway \(ISG\) alias for the service you want to add. The alias is the identifier Oracle EBS uses for the deployed service.

## About this task

Services are normally discovered automatically from the ERP system. Add a service manually when discovery doesn't return the service you need. For background on how WADL services are discovered, see [WADL service support for Oracle E-Business Suite](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erp-canvas-oracle-ebs-wadl-support.md).

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the model page by selecting the models icon \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model to which you want to add an operation entity.

4.  In the **ERP system** field, verify that the correct Oracle EBS system is selected.

5.  Select **Manage model**.

6.  Select an operation.

    If you don't have an operation, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

7.  Select **Select entity** on the **Manage entities** tab.

8.  In **Select type**, select **REST**.

    WADL services are added through the same modal as REST services.

9.  Select **+ Add service manually**.

10. In **How do you want to locate the service?**, select **Use WADL**.

11. In the **ISG alias** field, enter the Integrated SOA Gateway alias for the service, for example, `FndUser`.

12. In the **Service name** field, enter a name for the service, for example, `FND_USER_PKG`.

    Both the alias and the service name are required.

    \[Omitted image "erp-add-oracle-rest-service-manually1.jpg"\] Alt text: Add rest service manually modal with use wadl option selected, ISG alias specified, and service name added.

13. Select **Add service**.

    Zero Copy Connector for ERP fetches the WADL document and its schema files, then creates the catalog and endpoint records for the service.

    **Note:** If the service can't be reached, or if a service with the same alias already exists for this system, the service isn't added. Verify the alias and the connection, then try again.

14. In **Select the endpoints**, select an endpoint.

    Read operations show GET endpoints.

15. Select **Add entity**.


## Result

The service is added and its entities and fields are generated from the schema definitions, ready for mapping in Model Manager.

## What to do next

Map the generated input and output fields for the operation. For more information, see [Manage input parameters for model operation with a REST entity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-model-inputs-rest.md).

