---
title: Add a custom validation for devices
description: Customize the validation for your OT devices.
locale: en-US
release: xanadu
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Add a custom validation for devices

Customize the validation for your OT devices.

## Before you begin

The base system for the **sn\_otsm\_sgc.SGOTAssetCustomValidationExtensionPoint** extension point uses the default **sn\_otsm\_sgc.SGOTExcelStagingAssetValidationProcessor** implementation script. You can add a customized validation by creating an implementation for the extension point in the Service Graph Connector for Operational Technology \(Excel\) scope.

Role required: cmdb\_inst\_admin, admin

## Procedure

1.  Navigate to **All** &gt; **System Extensions Point** &gt; **Scripted Extension Points**.

2.  Select **sn\_otsm\_sgc.SGOTAssetCustomValidationExtensionPoint**.

3.  Select the **Create Implementation** related link.

    A script include is created where you can add your custom validation.

4.  To add a custom validation, refer to the following validation scenario.![Validation scenario for creating custom validations.](../image/validation-scenario.png)

5.  Select **Update**.


**Parent Topic:**[Service Graph Connector for Microsoft Excel](../concept/service-graph-connector-for-OT-excel.md)

