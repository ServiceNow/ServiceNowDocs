---
title: Managing Validations
description: Validation enables you to review and manage the imported data in the staging table.
locale: en-US
release: australia
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Validate imported staging records, Using the Service Graph Connector for Microsoft Excel through import tasks, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
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

**Parent Topic:**[Validate imported staging records](../task/run-validations.md)

