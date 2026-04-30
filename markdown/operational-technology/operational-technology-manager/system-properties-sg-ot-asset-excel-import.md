---
title: System properties that impact SG-OT Device Excel Import processing
description: The SG-OT Device Excel Import process depends on the following system properties for successful completion.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Easy import, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# System properties that impact SG-OT Device Excel Import processing

The SG-OT Device Excel Import process depends on the following system properties for successful completion.

## sn\_otsm\_sgc.excel.fields.for.transformed.name

-   This property enables the user to provide the fields to construct the transformed name.

-   The field value or column names must be separated by comma.

    This transformed name is used as the name of the configuration item \(CI\) instead of the name field directly from the staging table. By default, the name field value is itself used as the transformed name value.

-   This property belongs to the **sn\_otsm\_sgc** scope and is automatically appended to this property name.

-   Requires the admin, cmdb\_ot\_admin, and cmdb\_inst\_admin roles for read and write operations.


## sn\_otsm\_sgc.excel.transformed.name.delimiter

-   This property specifies the delimiter to be used when computing the transformed name with more than one field or column value specified in the system property **fields.for.transformed.name**.

-   If only one column name is specified in the **fields.for.transformed.name** property, the delimiter is not used.

-   This property belongs to the **sn\_otsm\_sgc** scope and is automatically appended to this property name.

-   Requires the admin, cmdb\_ot\_admin, and cmdb\_inst\_admin roles for read and write operations.


## sn\_otsm\_sgc.excel.fields.for.validation.state.change

-   This property enables you to provide a comma-separated list of attributes so that their validation state is changed to **Pending validation**. The default value is **Empty**.

    **Note:** Changes to the identifier fields, such as Mac Address, Serial Number, Transformed Name, and slot number \(for OT control modules\), the validation state is changed to **Pending validation**.

-   This property belongs to the sn\_otsm\_sgc scope and is automatically appended to this property name.
-   Requires the admin, cmdb\_ot\_admin, and cmdb\_inst\_admin roles for read and write operations.

## sn\_otsm\_sgc.enable.cmdb.validations

-   This property enables CMDB validations for the staging devices. If set to **True**, staging devices are validated against existing CMDB CIs for reconciliation.
-   This property belongs to the sn\_otsm\_sgc scope and is automatically appended to this property name.
-   Requires the admin, cmdb\_ot\_admin, and cmdb\_inst\_admin roles for read and write operations.

**Parent Topic:**[Easy import](../concept/easy-import.md)

