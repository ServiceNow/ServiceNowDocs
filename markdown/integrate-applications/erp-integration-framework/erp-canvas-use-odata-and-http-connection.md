---
title: Connect Zero Copy Connector for ERP to SAP using OData and HTTP
description: Extract data securely from ERP OData v2 APIs for use in remote tables and extraction tables. OData connects to SAP via HTTP.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
keywords: [erp, canvas, erp canvas, model, integration, data hub, zero, copy, connector, sap, odata, http, connection]
breadcrumb: [Configure, Zero Copy Connector for ERP, Workflow Data Fabric]
---

# Connect Zero Copy Connector for ERP to SAP using OData and HTTP

Extract data securely from ERP OData v2 APIs for use in remote tables and extraction tables. OData connects to SAP via HTTP.

**Important:**

OData v2 does not use snapshot isolation so you might experience some data consistency issues when retrieving data from an external ERP source.

## Providing OData access to users

You must have an SAP system that has been enabled to make an OData connection.

Extract data using OData and an HTTP connection. To give users OData access, see the following instructions on the SAP help site: [Back-End Server: Assign OData Service Authorization to Users](https://help.sap.com/doc/saphelp_ssb/1.0/en-US/6f/0e415370107d77e10000000a441470/content.htm?no_cache=true).

## Enabling download of XML files

The glide.attachment.extensions system property restricts the file types that can be downloaded. This property is empty by default. Check that the xml file extension hasn't been added to this property. For more information, see Security settings properties.

## New properties

The following are properties related to OData.

<table id="table_qkj_xs4_bdc"><thead><tr><th>

Property

</th><th>

Type

</th><th>

Description

</th><th>

Create manually?

</th><th>

Role needed to edit property

</th></tr></thead><tbody><tr><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td><td>

 

</td></tr><tr><td>

sn\_erp\_integration.catalog\_service\_path

</td><td>

string

</td><td>

After the hostname and port, this path is used to connect with any SAP catalog service. The default is: /sap/opu/odata/iwfnd/CATALOGSERVICE;v=2/ServiceCollection. After creating the property and setting it to true, a list of all services is retrieved from SAP. The information is stored in an XML file and attached to the system record. The XML can be used later. For example, parse the XML while offline with no connection to SAP. **Note:** If there's an update in the catalog service and you want to update the table catalog information, first remove the attachment displayed on the ERP Systems page. Then, run the retrieval process again to refresh the list.

</td><td>

Yes

</td><td>

admin

</td></tr><tr><td>

sn\_erp\_integration.odata\_max\_record\_fetch\_limit

</td><td>

integer

</td><td>

Limits the number of records fetched for GET calls by adding the $top parameter to the OData calls to reduce the number of records read from the Odata endpoint.

</td><td>

No

</td><td>

 

</td></tr><tr><td>

sn\_erp\_integration.odata\_service\_path

</td><td>

string

</td><td>

After the hostname and port, this path is used to connect with any SAP OData service. Add a URL in **Value** to specify the OData service. The default is: /sap/opu/odata/sap.

</td><td>

Yes

</td><td>

admin

</td></tr><tr><td>

sn\_erp\_integration.response\_timeout

</td><td>

integer

</td><td>

Specifies the timeout value for OData response. If OData calls are timed out frequently, increase the timeout value. Specify the value in seconds. The default is 100 seconds. This value is used for responses both from external web and from a MID Server.

</td><td>

No

</td><td>

admin or sn\_erp\_integration.erp\_admin

</td></tr><tr><td>

sn\_erp\_integration.use\_cookies

</td><td>

true \| false

</td><td>

Specifies if cookies must be used for OData connection.

</td><td>

No

</td><td>

admin or sn\_erp\_integration.erp\_admin

</td></tr><tr><td>

sn\_erp\_integration.use\_csrf\_token

</td><td>

true \| false

</td><td>

Indicates if CSRF token should be sent for OData calls in Zero Copy Connector for ERP operations.

</td><td>

No

</td><td>

admin or sn\_erp\_integration.erp\_admin

</td></tr></tbody>
</table>**Note:** To add a new property manually, verify that your scope is set to Zero Copy Connector for ERP, then navigate to sys\_properties.list and select **New**.

## Heartbeat information

For an ERP system, there are separate heartbeat indicators for RFC and HTTP. When a system is established, the heartbeats become active and the status is updated, including any errors. If the heartbeat calls are successful, BAPI and OData retrieval is triggered in parallel and the status can be seen on the system record. BAPI and table list retrieval is done via RFC. OData retrieval is done via HTTP.

![System record with ODATA retrieval status of completed.](../image/erpc-system-heartbeats.png)

## More information

For more information about using OData in Zero Copy Connector for ERP, see [Create an OData connection in Zero Copy Connector for ERP](../task/create-an-odata-connection.md) and [OData capabilities supported by Zero Copy Connector for ERP](../reference/erp-data-hub-odata-query-capabilities.md).

-   **[OData capabilities supported by Zero Copy Connector for ERP](../reference/erp-data-hub-odata-query-capabilities.md)**  
Details about the OData v2 query capabilities supported in Zero Copy Connector for ERP \(Enterprise Resource Planning\).
-   **[Create an OData connection in Zero Copy Connector for ERP](../task/create-an-odata-connection.md)**  
Create an OData v2 connection to link to SAP via HTTP so data can be extracted for use in remote tables and extraction tables in Zero Copy Connector for ERP \(Enterprise Resource Planning\).
-   **[Add an OData service manually in Zero Copy Connector for ERP](../task/erp-add-a-service-manually.md)**  
When adding an entity to a model using OData, if the service you need isn't listed, add the service manually in Zero Copy Connector for ERP \(Enterprise Resource Planning\).
-   **[Obtain data from SAP SuccessFactors using OData v2 APIs](obtain-data-from-successfactors-using-odata-v2-apis.md)**  
Access talent management data from SAP SuccessFactors using OData V2 APIs.
-   **[Configure OAuth authorization code flow to use in Zero Copy Connector for ERP](../task/configure-oauth-authorization-code-flow-to-use-in-zero-copy-connector-for-erp.md)**  
Configure OAuth authorization code flow for SAP and use OAuth to authenticate and authorize users for OData endpoints.

**Parent Topic:**[Configuring Zero Copy Connector for ERP](erp-integration-configuration-overview.md)

