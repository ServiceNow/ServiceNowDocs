---
title: Connect Zero Copy Connector for ERP to SAP using OData and HTTP
description: Extract data securely from ERP OData v2 APIs using ETL for use in remote tables and extraction tables. OData connects to SAP via HTTP.
locale: en-US
release: yokohama
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Using ERP models, extraction tables, and remote tables, Zero Copy Connector for ERP, Building low-code applications, Developing your application, Building applications]
---

# Connect Zero Copy Connector for ERP to SAP using OData and HTTP

Extract data securely from ERP OData v2 APIs using ETL for use in remote tables and extraction tables. OData connects to SAP via HTTP.

**Important:**

OData v2 does not use snapshot isolation so you might experience some data consistency issues when retrieving data from an external ERP source.

## Providing OData access to users

You must have an SAP system that has been enabled to make an OData connection.

Extract data using OData and an HTTP connection. To give users OData access, see the following instructions on the SAP help site [Back-End Server: Assign OData Service Authorization to Users](https://help.sap.com/doc/saphelp_ssb/1.0/en-US/6f/0e415370107d77e10000000a441470/content.htm?no_cache=true).

## Allowing download of XML files

The glide.attachment.extensions system property restricts the file types that can be downloaded. This property is empty by default. Check that the xml file extension has not been added to this property. For more information, see [Restrict attachment file extensions](https://www.servicenow.com/docs/access?context=t_DisablingTheDragAndDropFeature&version=yokohama&pubname=yokohama-platform-administration&section=t_RestrictingFileExtensions&ft:locale=en-US).

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

sn\_erp\_integration.catalog\_service\_path

</td><td>

string

</td><td>

After the hostname and port, this is the path to connect with any SAP catalog service. The default is: /sap/opu/odata/iwfnd/CATALOGSERVICE;v=2/ServiceCollection. After creating the property and setting it to true, a list of all services is retrieved from SAP. The information is stored in an XML file and attached to the system record. The XML can be used later. For example, parse the XML while offline with no connection to SAP. **Note:** If there is an update in the catalog service and you want to update the catalog information in the table, first remove the attachment displayed on the ERP Systems page and then run the retrieval process again to refresh the list.

</td><td>

Yes

</td><td>

admin

</td></tr><tr><td>

sn\_erp\_integration.odata\_service\_path

</td><td>

string

</td><td>

After the hostname and port, this is the path to connect with any SAP OData service. Add a URL in **Value** to specify the OData service. The default is: /sap/opu/odata/sap.

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

![Zero Copy Connector for ERP systems page with RFC and HTTP heartbeat status.](../image/erpc-system-heartbeats.png)

## More information

For more information about using OData in Zero Copy Connector for ERP, see [Create an OData connection in Zero Copy Connector for ERP](../task/create-an-odata-connection.md) and [OData capabilities supported by Zero Copy Connector for ERP](../reference/erp-data-hub-odata-query-capabilities.md).

-   **[OData capabilities supported by Zero Copy Connector for ERP](../reference/erp-data-hub-odata-query-capabilities.md)**  
Details about the OData v2 query capabilities supported in Zero Copy Connector for ERP.
-   **[Create an OData connection in Zero Copy Connector for ERP](../task/create-an-odata-connection.md)**  
Create an OData v2 connection to link to SAP via HTTP so data can be extracted for use in remote tables and extraction tables.

**Parent Topic:**[Using ERP models, extraction tables, and remote tables](work-with-erp-systems-connections-and-remote-tables.md)

