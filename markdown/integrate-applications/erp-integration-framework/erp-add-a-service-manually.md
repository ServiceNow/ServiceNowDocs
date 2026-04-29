---
title: Add an OData service manually in Zero Copy Connector for ERP
description: When adding an entity to a model using OData, if the service you need isn't listed, add the service manually.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, odata, service, manually, metadata, url, file, xml]
breadcrumb: [Connect to SAP with OData and HTTP, Configure, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Add an OData service manually in Zero Copy Connector for ERP

When adding an entity to a model using OData, if the service you need isn't listed, add the service manually.

## Before you begin

Role required: admin

You can connect to an ERP system based on a metadata URL or an uploaded metadata file \(xml\). The file option enables you to, for example, access data from SuccessFactors. For more information, see [Obtain data from SAP SuccessFactors using OData v2 APIs](../concept/obtain-data-from-successfactors-using-odata-v2-apis.md).

Before you can add a service manually, you must do the following:

-   Confirm that you have an SAP system that has been enabled to make an OData connection.
-   Enable the **sn\_erp\_integration.enableModelModification** property. For more information, see [Install Zero Copy Connector for ERP](install-erp-integration.md).
-   Create a connection and credential alias, specifying HTTP as the **Connection type**. For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=australia&pubname=australia-platform-security&ft:locale=en-US).
-   Create an HTTP connection for the service. Add the connection alias that you created, the connection URL, and the odata\_ping\_url.

    ![Http connection record with key fields highlighted.](../image/erp-add-system-manually1.png)

    For more information, see [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   Create a system that uses the HTTP connection. For more information, see [Create an ERP system in Zero Copy Connector for ERP](create-an-erp-system.md). On the system record, confirm that the heartbeats are successful and the retrieval status is complete. If any have failed, select **Restart data retrieval**.
-   If you're going to connect using a URL, copy the metadata URL from the ERP system to which you're linking. Use the relative URL containing only the path following the domain, for example, v2/northwind/northwind.svc/$metadata.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the model page by selecting the models icon ![](../image/erpc-data-model-icon.png) in the side panel.

3.  Select the model to which you want to add an operation entity.

4.  Check that the correct system is selected in **ERP system**.

5.  Select the **Manage model** button.

6.  Select an operation.

    If you don't have an operation, see [Add an operation to a model in Zero Copy Connector for ERP](erpc-manage-models-read-op.md).

7.  Select **Select entity** on the **Manage entities** tab.

8.  In **Select type**, select **OData**.

    The drop-down list in the **Select type** field only displays the types supported by the ERP system's software version specified on the model record. For example, if **SAP SuccessFactors Cloud** is set in the **ERP software** field for the model, the only entity type available is OData.

9.  Select **+ Add service manually**.

    ![Add entity options with add service manually link highlighted.](../image/erp-add-system-manually2.png)

10. If you're using a metadata URL, follow these substeps \(if you're uploading a metadata file, go to the next step\).

    1.  Select **Use metadata URL**.

        The **Connection URL** is added automatically based on the ERP system specified for the model. If no URL is listed or the listed URL is incorrect, edit the ERP system field on the model record.

    2.  Paste in the **Metadata URL** and click outside of the field.

    3.  Check that a **Service base URL** is filled in automatically and a **Service name** is created automatically.

        **Note:** If a **Service name** is not created, you have two options:

        -   Provide a different **Metadata URL**.
        -   In the **All** menu, enter `sn_erp_integration_odata_service_catalog.list` and delete the previous entry of service from the table.
        ![Add service manually fields filled in with details.](../image/erp-add-system-manually3.png)

11. If you're uploading a metadata file, follow these substeps.

    1.  Select **Upload metadata file**.

    2.  Select **Attach File**.

    3.  Select an xml file and then select **Open**.

    4.  Enter a **Service base URL**.

    5.  Check that a **Service name** based on the URL you entered is added automatically.

        You can download, edit, or delete the xml file by selecting an icon.

        ![Add service manually modal with three icons highlighted.](../image/erp-add-system-manually6.png)

12. When you're finished, select **Add service**.

    A background job named **Additional Service Handler** runs.

    **Note:** If there's an issue, an error message appears. Select **Flow context** for more information. You can also view execution details in Workflow Studio.

    ![Error message with flow context link highlighted.](../image/erp-add-system-manually4.png)

    The service is added to the entity record.

13. In **Select the endpoints**, search for and select an endpoint.

14. When you're finished, select **Add entity**.


**Parent Topic:**[Connect Zero Copy Connector for ERP to SAP using OData and HTTP](../concept/erp-canvas-use-odata-and-http-connection.md)

