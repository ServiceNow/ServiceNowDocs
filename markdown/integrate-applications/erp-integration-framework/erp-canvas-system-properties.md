---
title: Zero Copy Connector for ERP system properties
description: Review the system properties for Zero Copy Connector for ERP.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, system, property, properties]
breadcrumb: [Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP system properties

Review the system properties for Zero Copy Connector for ERP.

These properties are available for Zero Copy Connector for ERP.

**Note:** To open the System Properties \[sys\_properties\] table, enter `sys_properties.list` in the navigation filter.

<table id="table_orv_d3b_2fc"><thead><tr><th>

Property

</th><th>

Type

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.snc.uib.sn\_erp\_integration.debug.level

</td><td>

integer

</td><td>

Debug log level.

-   0 is disabled
-   1 is least level of detail
-   9 is highest level of detail

 Logging is done in class ERPIntegrationLog.

</td></tr><tr><td>

glide.ui.sn\_erp\_integration\_etl\_extraction\_source\_activity.fields

</td><td>

string

</td><td>

Extraction tables activity fields.

</td></tr><tr><td>

glide.ui.sn\_erp\_integration\_model\_activity.fields

</td><td>

string

</td><td>

ERP Model activity formatter fields.

</td></tr><tr><td>

glide.ui.sn\_erp\_integration\_remote\_table\_activity.fields

</td><td>

string

</td><td>

Remote table activity formatter fields.

</td></tr><tr><td>

glide.ui.sn\_erp\_integration\_scheduled\_extraction\_activity.fields

</td><td>

string

</td><td>

ETL Scheduled Extraction formatter fields.

</td></tr><tr><td>

sn\_erp\_integration.catalog\_service\_path \(this property must be created manually\)

</td><td>

string

</td><td>

After the hostname and port, this path is used to connect with any SAP catalog service. The default is: /sap/opu/odata/iwfnd/CATALOGSERVICE;v=2/ServiceCollection. After creating the property and setting it to true, a list of all services is retrieved from SAP. The information is stored in an XML file and attached to the system record. The XML can be used later. For example, parse the XML while offline with no connection to SAP. **Note:** If there's an update in the catalog service and you want to update the table catalog information, first remove the attachment displayed on the ERP Systems page. Then, run the retrieval process again to refresh the list.

</td></tr><tr><td>

sn\_erp\_integration.db\_memory\_limit\_mb

</td><td>

integer

</td><td>

Database memory limit in megabyte per request. When limit is reached, data is written to disc.

</td></tr><tr><td>

sn\_erp\_integration.debug.sapresponse.size

</td><td>

integer

</td><td>

Number of bytes of the reply from SAP probe to output from step that calls SAP.

</td></tr><tr><td>

sn\_erp\_integration.enableModelModification

</td><td>

true \| false

</td><td>

Allows cloning and changes of models in Zero Copy Connector for ERP application.

</td></tr><tr><td>

sn\_erp\_integration.heartbeat\_enabled

</td><td>

true \| false

</td><td>

Turns heartbeat feature on/off.

</td></tr><tr><td>

sn\_erp\_integration.keep\_pages\_on\_mid\_on\_error

</td><td>

true \| false

</td><td>

Do not delete data on mid server when errors occur.

</td></tr><tr><td>

sn\_erp\_integration.max\_in\_loaded\_state

</td><td>

integer

</td><td>

Maximum pages in loaded state per process. When more pages are in loaded state, ETl process waits until less pages are in loaded state before sending next batch.

</td></tr><tr><td>

sn\_erp\_integration.odata\_max\_record\_fetch\_limit

</td><td>

integer

</td><td>

Limits the number of records fetched for GET calls by adding the $top parameter to the OData calls. This reduces the number of records read from the Odata endpoint.

</td></tr><tr><td>

sn\_erp\_integration.odata\_service\_path \(this property must be created manually\)

</td><td>

string

</td><td>

After the hostname and port, this path is used to connect with any SAP OData service. Add a URL in **Value** to specify the OData service. The default is: /sap/opu/odata/sap.

</td></tr><tr><td>

sn\_erp\_integration.probe.paging.tech

</td><td>

choice list

</td><td>

Paging technology.

</td></tr><tr><td>

sn\_erp\_integration.response\_timeout

</td><td>

integer

</td><td>

Specifies the timeout value for OData response. If OData calls are timed out frequently, increase the timeout value. Specify the value in seconds. The default is 100 seconds. This value is used for responses both from external web and from a MID Server.

</td></tr><tr><td>

sn\_erp\_integration.result\_page\_size

</td><td>

integer

</td><td>

Number of records to retrieve from the external system. The default global property for all extractions is set to 50. To override the global property, specify an extraction source specific page size with the sn\_erp\_integration\_result\_page\_size system property.

</td></tr><tr><td>

sn\_erp\_integration.sap\_output\_pagesize

</td><td>

integer

</td><td>

Page size of output from MID Server.

</td></tr><tr><td>

sn\_erp\_integration.sap\_pagesize

</td><td>

integer

</td><td>

Page size for database requests from MID Server to SAP.

</td></tr><tr><td>

sn\_erp\_integration.save\_erp\_attachment

</td><td>

true \| false

</td><td>

Set this property to true to save the latest response from your ERP system as an attachment on the ERP remote table.

 Updating the attachment setting on the ERP remote table to "use attachment" skips the request to the ERP system and shows the data stored in attachment.

 Requires the sn\_erp\_integration.erp\_admin role to change.

</td></tr><tr><td>

sn\_erp\_integration.storage\_pagesize

</td><td>

integer

</td><td>

Size of each batch insert to storage after response from SAP.

</td></tr><tr><td>

sn\_erp\_integration.use\_cookies

</td><td>

true \| false

</td><td>

Specifies if cookies must be used for OData connection.

</td></tr><tr><td>

sn\_erp\_integration.use\_csrf\_token

</td><td>

true \| false

</td><td>

Indicates if CSRF token should be sent for OData calls in Zero Copy Connector for ERP operations.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP reference](erp-integration-reference.md)

