---
title: Review the system properties used by the Service Graph Connector for Microsoft Excel
description: As an OT Admin or CMDB Integration Admin, view system properties related to the Service Graph Connector for Microsoft Excel.
locale: en-US
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Review the system properties used by the Service Graph Connector for Microsoft Excel

As an OT Admin or CMDB Integration Admin, view system properties related to the Service Graph Connector for Microsoft Excel.

## Before you begin

View a filtered list of all the system properties that are used by the Service Graph Connector.

Role required: cmdb\_ot\_admin or cmdb\_inst\_admin

## Procedure

1.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager Admin** &gt; **Import OT Devices - System Properties**.

    The list shows records whose names begin with **sn\_otsm\_sgc.excel**.

2.  Review the following system properties.

<table id="table_p31_wbp_xfc"><thead><tr><th>

System property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_otsm\_sgc.excel.fields.for.transformed.name

</td><td>

-   This property enables the user to provide the fields to construct the transformed name.

-   The field value or column names must be separated by comma.

This transformed name is used as the name of the configuration item \(CI\) instead of the name field directly from the staging table. By default, the name field value is itself used as the transformed name value.

-   This property belongs to the **sn\_otsm\_sgc** scope and is automatically appended to this property name.

-   Requires the admin, cmdb\_ot\_admin, and cmdb\_inst\_admin roles for read and write operations.

</td></tr><tr><td>

sn\_otsm\_sgc.excel.transformed.name.delimiter

</td><td>

-   This property specifies the delimiter to be used when computing the transformed name with more than one field or column value specified in the system property **fields.for.transformed.name**.

-   If only one column name is specified in the **fields.for.transformed.name** property, the delimiter is not used.

-   This property belongs to the **sn\_otsm\_sgc** scope and is automatically appended to this property name.

-   Requires the admin, cmdb\_ot\_admin, and cmdb\_inst\_admin roles for read and write operations.

</td></tr><tr><td>

sn\_otsm\_sgc.excel.fields.for.validation.state.change

</td><td>

-   This property enables you to provide a comma-separated list of attributes so that their validation state is changed to **Pending validation**. The default value is **Empty**.

**Note:** Changes to the identifier fields, such as Mac Address, Serial Number, Transformed Name, and slot number \(for OT control modules\), the validation state is changed to **Pending validation**.

-   This property belongs to the sn\_otsm\_sgc scope and is automatically appended to this property name.
-   Requires the admin, cmdb\_ot\_admin, and cmdb\_inst\_admin roles for read and write operations.


</td></tr><tr><td>

sn\_otsm\_sgc.enable.cmdb.validations

</td><td>

-   This property enables CMDB validations for the staging devices. If set to **True**, staging devices are validated against existing CMDB CIs for reconciliation.
-   This property belongs to the sn\_otsm\_sgc scope and is automatically appended to this property name.
-   Requires the admin, cmdb\_ot\_admin, and cmdb\_inst\_admin roles for read and write operations.


</td></tr></tbody>
</table>
**Parent Topic:**[Configuring the Service Graph Connector for Microsoft Excel](../concept/configuring-service-graph-connector-for-excel.md)

