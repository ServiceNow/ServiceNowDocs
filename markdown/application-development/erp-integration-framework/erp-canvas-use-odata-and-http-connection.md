---
title: Connect ERP Data Hub to SAP using OData and HTTP
description: Extract data securely from ERP OData APIs using ETL for use in remote tables and extraction tables. OData connects to SAP via HTTP.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: concept
last_updated: "2024-10-16"
reading_time_minutes: 2
breadcrumb: [Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# Connect ERP Data Hub to SAP using OData and HTTP

Extract data securely from ERP OData APIs using ETL for use in remote tables and extraction tables. OData connects to SAP via HTTP.

**Important:**

OData v2 does not use snapshot isolation so you might experience some data consistency issues when retrieving data from an external ERP source.

## Providing OData access to users

You must have an SAP system that has been enabled to make an OData connection.

As of Xanadu Store Release 2, extract data using OData and an HTTP connection. To give users OData access, see the following instructions on the SAP help site [Back-End Server: Assign OData Service Authorization to Users](https://help.sap.com/doc/saphelp_ssb/1.0/en-US/6f/0e415370107d77e10000000a441470/content.htm?no_cache=true).

## New properties

The following are properties related to OData available for ERP in Xanadu Store Release 2.

|Property|Type|Description|Create manually?|
|--------|----|-----------|----------------|
|sn\_erp\_integration.response\_timeout|integer|Specifies the timeout value for OData response. If OData calls are timed out frequently, increase the timeout value. Specify the value in seconds. The default is 100 seconds. This value is used for responses both from external web and from a MID Server.|No|
|sn\_erp\_integration.use\_csrf\_token|true \| false|Indicates if CSRF token should be sent for OData calls in ERP Data Hub operations.|No|
|sn\_erp\_integration.catalog\_service\_path|string|After the hostname and port, this is the path to connect with any SAP catalog service. The default is: /sap/opu/odata/iwfnd/CATALOGSERVICE;v=2/ServiceCollection. After creating the property and setting it to true, a list of all services are retrieved from SAP. The information is stored in an XML file and attached to the system record. The XML can be used later. For example, parse the XML while offline with no connection to SAP.|Yes|
|sn\_erp\_integration.odata\_service\_path|string|After the hostname and port, this is the path to connect with any SAP OData service. Add a URL in **Value** to specify the OData service. The default is: /sap/opu/odata/sap.|Yes|

**Note:** To add a new property manually, verify that your scope is set to ERP Data Hub, then navigate to sys\_properties.list and select **New**.

## Heartbeat information

For an ERP system, there are separate heartbeat indicators for RFC and HTTP. When a system is established, the heartbeats become active and the status is updated, including any errors. If the heartbeat calls are successful, BAPI and OData retrieval is triggered in parallel and the status can be seen on the system record. BAPI and table list retrieval is done via RFC. OData retrieval is done via HTTP.

![ERP Data Hub systems page with RFC and HTTP heartbeat status.](../image/erpc-system-heartbeats.png)

## More information

For more information about using OData in ERP Data Hub, see [Create an OData connection in ERP Data Hub](../task/create-an-odata-connection.md) and [OData capabilities supported by ERP Data Hub](../reference/erp-data-hub-odata-query-capabilities.md).

-   **[OData capabilities supported by ERP Data Hub](../reference/erp-data-hub-odata-query-capabilities.md)**  
Details about the OData query capabilities supported in ERP Data Hub.
-   **[Create an OData connection in ERP Data Hub](../task/create-an-odata-connection.md)**  
Create an OData v2 connection to link to SAP via HTTP so data can be extracted for use in remote tables and extraction tables.

**Parent Topic:**[Using ERP models, extraction tables, and remote tables](work-with-erp-systems-connections-and-remote-tables.md)

