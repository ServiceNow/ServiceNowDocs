---
title: OData capabilities supported by ERP Data Hub
description: Details about the OData query capabilities supported in ERP Data Hub.
locale: en-US
release: xanadu
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2024-10-30"
reading_time_minutes: 1
breadcrumb: [Connect ERP Data Hub to SAP using OData and HTTP, Using ERP models, extraction tables, and remote tables, ERP Data Hub, Building low-code applications, Developing your application, Building applications]
---

# OData capabilities supported by ERP Data Hub

Details about the OData query capabilities supported in ERP Data Hub.

For information about OData connections in ERP Data Hub, see [Connect ERP Data Hub to SAP using OData and HTTP](../concept/erp-canvas-use-odata-and-http-connection.md) and [Create an OData connection in ERP Data Hub](../task/create-an-odata-connection.md).

<table id="table_obv_yvk_fdc"><thead><tr><th>

OData query

</th><th>

 

</th></tr></thead><tbody><tr><td>

$select, $filter, $count

</td><td>

Available in the **Use ERP** flow.

 When using the inputs and outputs parameters in the model, $select and $filter are applied.

 Use $count when invoking the **Use ERP** flow.

</td></tr><tr><td>

$orderby

</td><td>

Supported only via encoded query while executing the remote tables or extraction tables.

</td></tr><tr><td>

$top and $skip

</td><td>

When doing the internal operations, $top and $skip are supported only while pagination is done.

 Cannot send $top and $skip via any flow.

</td></tr></tbody>
</table>**Parent Topic:**[Connect ERP Data Hub to SAP using OData and HTTP](../concept/erp-canvas-use-odata-and-http-connection.md)

