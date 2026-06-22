---
title: Add a REST service manually in Zero Copy Connector for ERP
description: When adding an entity to a model using REST, if the service you need isn't listed, add the service manually in Zero Copy Connector for ERP \(Enterprise Resource Planning\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/erp-integration-framework/erp-add-a-rest-service-manually.html
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-04-25"
reading_time_minutes: 3
breadcrumb: [Add an entity to a model, Building models, Use, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Add a REST service manually in Zero Copy Connector for ERP

When adding an entity to a model using REST, if the service you need isn't listed, add the service manually in Zero Copy Connector for ERP \(Enterprise Resource Planning\).

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

Complete the following before adding a service manually:

-   Enable the **sn\_erp\_integration.enableModelModification** property. For more information, see [Install Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/install-erp-integration.md).
-   Create a connection and credential alias, specifying HTTP as the **Connection type**. For more information, see [Create a Connection &amp; Credential alias](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/connection-alias.md).
-   Create an HTTP connection for the service. Add the connection alias that you created and the connection URL. On the **Attributes** tab, select **Patch** or **Put** in **http\_method\_for\_update** and specify the **odata\_ping\_url**.

    For more information, see [Create an HTTP\(s\) connection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/connections-and-credentials/create-https-connection.md).

-   Create a system that uses the HTTP connection. For more information, see [Create an ERP system in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/create-an-erp-system.md). On the system record, confirm that the heartbeats are successful and the retrieval status is complete. If any have failed, select **Restart data retrieval**.
-   If you plan to connect using a URL, copy the metadata URL from the ERP system to which you're linking. Use the relative URL containing only the path following the domain, for example, v2/northwind/northwind.svc/$metadata.

## Procedure

1.  Navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Zero Copy Connector for ERP Home**.

2.  Open the model page by selecting the models icon. \[Omitted image "erpc-data-model-icon.png"\] Alt text: in the side panel.

3.  Select the model to which you want to add an operation entity.

4.  In the **ERP system** field, verify that the correct system is selected.

5.  Select the **Manage model** button.

6.  Select an operation.

    If you don't have an operation, see [Add an operation to a model in Zero Copy Connector for ERP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/erpc-manage-models-read-op.md).

7.  Select **Select entity** on the **Manage entities** tab.

8.  In **Select type**, select **REST**.

9.  Select **+ Add service manually**.

    \[Omitted image "erp-add-rest-service-manually1.jpg"\] Alt text: Add entity options with add service manually link highlighted.

    **Note:** If you have already added the service, but want to select a different endpoint, you can directly search for the service by name. You don't have to add the metadata URL or upload the metadata file again.

10. If using a metadata URL, follow these substeps \(if uploading a metadata file, go to the next step\).

    1.  Select **Use Swagger/OpenAPI URL**.

    2.  In the **Swagger/OpenAPI Version** field, select a version such as 2.0 or 3.0.

    3.  Paste in a **Swagger/OpenAPI URL** and select outside of the field.

    4.  In the **Service name** field, verify that a name is created automatically.

        You can edit the service name as needed.

        \[Omitted image "erp-add-rest-service-manually2.jpg"\] Alt text: Add service manually with URL option selected and fields filled in with details.

11. If uploading a metadata file, follow these substeps.

    1.  Select **Upload Swagger/OpenAPI file**.

    2.  In **Swagger/OpenAPI Version**, select a version such as 2.0 or 3.0.

    3.  Select **Attach File**.

    4.  Select a JSON or YAML file and then select **Open**.

    5.  Enter a **Service name**.

        You can download, edit, or delete the file by selecting an icon.

        \[Omitted image "erp-add-rest-service-manually3.jpg"\] Alt text: Add service manually with upload file option selected and fields filled in with details.

12. When finished, select **Add service**.

    A background job named **Additional Service Handler** runs.

    **Note:** If an issue occurs, an error message appears. Select **Flow context** for more information. You can also view execution details in Workflow Studio.

    \[Omitted image "erp-add-system-manually4.png"\] Alt text: Error message with flow context link highlighted.

    The service is added to the entity record.

13. In **Select the endpoints**, search for and select an endpoint.

    The endpoints available in an operation depend on the HTTP method associated with the operation type:

    -   Read operations display GET endpoints.
    -   Create operations display POST endpoints.
    -   Update operations display PATCH, PUT, and other update endpoints.
    \[Omitted image "erp-add-rest-service-manually4.jpg"\] Alt text: Add entity form with all fields, including endpoint filled in.

14. When finished, select **Add entity**.


**Parent Topic:**[Add an entity to a model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/erp-integration-framework/add-an-entity-to-model.md)

