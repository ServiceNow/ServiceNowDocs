---
title: Create an OData connection in Zero Copy Connector for ERP
description: Create an OData v2 connection to link to SAP via HTTP so data can be extracted for use in remote tables and extraction tables.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Connect Zero Copy Connector for ERP to SAP using OData and HTTP, Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Create an OData connection in Zero Copy Connector for ERP

Create an OData v2 connection to link to SAP via HTTP so data can be extracted for use in remote tables and extraction tables.

## Before you begin

Role required: sn\_erp\_integration.erp\_admin

For information about OData connections in Zero Copy Connector for ERP, see [Connect Zero Copy Connector for ERP to SAP using OData and HTTP](../concept/erp-canvas-use-odata-and-http-connection.md) and [OData capabilities supported by Zero Copy Connector for ERP](../reference/erp-data-hub-odata-query-capabilities.md).

## About this task

An admin or a user with the sn\_erp\_integration.erp\_admin role must enable the **sn\_erp\_integration.enableModelModification** property for you to edit, customize, and clone ERP models and tables. After enabling the **sn\_erp\_integration.enableModelModification** property, Zero Copy Connector for ERP retrieves all tables and BAPIs \(Business Application Programming Interface\) to use when managing models.The property must be configured for either a non-production or production state. System properties are maintained in the System Property table \[sys\_properties\], which you can access using the module navigator, or directly typing `sys_properties.list` in the Navigator Filter.

**Note:** You must enable the **sn\_erp\_integration.enableModelModification** property on the correct scope. Enabling the **sn\_erp\_integration.enableModelModification** on a production instance can create new metadata records when new models and fields are added in Zero Copy Connector for ERP.

## Procedure

1.  Confirm that you have an SAP system that has been enabled to make an OData connection.

2.  Create a connection and credential alias, specifying HTTP as the **Connection type**.

    For more information, see [Create a Connection &amp; Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US).

3.  Create an HTTP connection and associate it with the new alias.

    **Note:** For more information, see [Create an HTTP\(s\) connection](https://www.servicenow.com/docs/access?context=create-https-connection&version=yokohama&pubname=yokohama-platform-security&ft:locale=en-US). If you choose to use a MID Server, users with access to the services can use the same credential for RFC and HTTP.

4.  Create a system with the HTTP connection.

    For more information, see [Create an ERP system in Zero Copy Connector for ERP](create-an-erp-system.md).

5.  On the system record, confirm that the heartbeats are successful and the retrieval status is complete.

    If any have failed, select **Restart data retrieval**. Any data retrieval that failed \(BAPI, OData, or tables\) is fetched again.

6.  Create a model and, after saving, open the model record.

    For more information, see [Add a new ERP model](erpc-add-new-data-model.md).

7.  Select **Manage model**.

8.  Select **Add model operation**.

    1.  Choose a **Select type**.

    2.  Select **Save and Continue**.

9.  Select the new operation.

10. Select **Select entity**.

    1.  In **Select type**, choose **OData**.

    2.  In **Select service**, search for and select a service, for example **API\_BUSINESS\_PARTNER \(Remote API for business partner\)** in the OData service catalog.

        When you specify the service, a call is made to the SAP service to read its metadata. The default service is /sap/opu/odata/iwfnd/CATALOGSERVICE;v=2/ServiceCollection. If you must change the service, create a property named sn\_erp\_integration.odata\_service\_path and set the value.

    3.  In **Select the endpoints**, search for and select an endpoint, for example **A\_BusinessPartnerType**.

    4.  Select **Add entity**.

        ![Add entity screen with type, service, and endpoint specified.](../image/erpc-odata-create-connection1.png)

        The flow named **GET SAP BAPIs and tables when system becomes active** runs to retrieve the data. The BAPI, table, and catalog tables are populated.

11. Select **Specify inputs** to check the information and edit as needed.

    ![Specify inputs screen for the entity.](../image/erpc-odata-create-connection2.png)

    For more information, see [Manage input parameters for an Zero Copy Connector for ERP model operation](erpc-manage-model-inputs.md).

12. Select **Choose output** to check the information and edit as needed.

    For more information, see [Choose output parameters for an ERP model](erp-canvas-manage-outputs.md).

13. Open the ERP systems list by selecting the systems icon \(![ERP systems icon](../image/erp-systems-icon-sidebar.png)\) in the side panel.

14. Select the system.

15. Check the heartbeat and retrieval status until they are successful.

    ![System page with heartbeat and retrieval status highlighted.](../image/erpc-odata-create-connection3.png)

16. Create a model.

    1.  Open the ERP models page by selecting the ERP models icon \(![ERP model icon](../image/erpc-data-model-icon.png)\) in the side panel.

    2.  Select **New**.

    3.  Add an **ERP model name**, **ERP module**, and **ERP system**, and select **Save**.

    4.  Select the new model in the list.

    5.  Select **Manage model**.

    6.  Select **Add model operation**.

    7.  Select a **Select type**.

    8.  Select **Save and Continue**.

17. Select the new operation.

18. Select **Select entity**.

    1.  In **Select type**, select **OData**.

    2.  Select a **Select entity**, select an entity, for example **API\_BUSINESS\_PARTNER \(Remote API for Business Partner\) OData service catalog**.

    3.  In **Select the endpoints**, search for and select an endpoint, for example **A\_BusinessPartnerType Entity Name: Business Partner --- Return Type: Business Partner**.

    4.  Select **Add entity** and wait for retrieval to complete.

        ![Add entity screen with type, service, and endpoint specified.](../image/erpc-odata-create-connection4.png)

19. Select **Specify inputs** to check the information and edit as needed.

    1.  If there are required fields, select **Select mandatory fields**.

    2.  Select any mandatory inputs listed and select **OK**.

    3.  Select **Save**.

20. Select **Choose output**.

    1.  Select **+ New output**.

    2.  Select fields, for example **BusinessPartnerName** and **Full Name**.

    3.  Select **Save**.

21. Test with Workflow Studio.

    1.  Navigate to **All** &gt; **Workflow Studio**.

    2.  On the homepage, select **Actions**.

    3.  In the **Name** column, filter for **contains Value** and type `Use ERP`.

    4.  Select **Apply**.

    5.  Select **Use ERP data**.

    6.  Select **Test**.

    7.  Specify the **ModelName**, **ModelOperation**, **Mandatory fields** \(provide a value for the mandatory field if necessary\), select a **System**, and select **Run Test**.

    8.  When complete, select the link **Your test has finished running. View the Action execution details**.

    9.  View and check the output, for example, in **Output Data**, select the **Response** to view the output.


**Parent Topic:**[Connect Zero Copy Connector for ERP to SAP using OData and HTTP](../concept/erp-canvas-use-odata-and-http-connection.md)

