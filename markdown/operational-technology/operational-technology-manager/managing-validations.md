---
title: Managing Validations
description: Validation enables you to review and manage the imported data in the staging table.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Managing Validations

Validation enables you to review and manage the imported data in the staging table.

Validations to be executed:

-   Missing correlation id \(Correlation id\)
-   Missing parent correlation id in case the type is Control module \(Control module parent id\)
-   Missing serial number \(Serial number\)
-   Missing transformed name \(Transformed name\)
-   Missing MAC Address \(validation is executed on column MAC Address 1\)
-   Missing type \(Type\)
-   Missing rack number \(Rack number\)
-   Missing slot number \(Slot number\)
-   Equipment model entity path does not exist \(Equipment model entity path\)
-   Site name provided is invalid \(Site name\)
-   Validate duplicates on transformed name \(Transformed name\)

    **Note:** This validation is skipped for control modules.

-   Validate duplicates on MAC Address \(check on all MAC Address 1 columns\)
-   Validate duplicates on Serial number column \(Serial number\)
-   Validate duplicates on Correlation id column \(Correlation id\)
-   Validate duplicates on rack and slot numbers

    **Note:** This validation is only for control modules.

-   Validate Has Module and Control module Parent ID

    **Note:** This validation is only for PLCs and control modules.

-   Validate Invalid types - Compare against the default Excel type to OT device type mapping through the **sn\_otsm\_sgc.SGOTAssetImportExtensionPoint** extension point implementation.

    If you have additional mappings, create an extension point implementation for the base system **sn\_otsm\_sgc.SGOTAssetImportExtensionPoint** extension point.


For more information about adding a custom implementation for device classification, see [Add a custom implementation for device classification](../task/adding-custom-implementation-for-asset-classification.md).

-   **[Run Validations](../task/run-validations.md)**  
Run validations on records to find missing, duplicate, and invalid data.
-   **[Use OT staging tasks to remediate invalid records](../task/using-tasks-to-remediate-invalid-records.md)**  
Remediate invalid records in the SG OT Excel Stagings table by using Operational Technology \(OT\) staging tasks. Using OT staging tasks can help you track the invalid records that you need to fix.

**Parent Topic:**[Service Graph Connector for Microsoft Excel](service-graph-connector-for-OT-excel.md)

