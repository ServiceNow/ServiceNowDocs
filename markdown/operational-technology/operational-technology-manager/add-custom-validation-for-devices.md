---
title: Add a custom validation for devices
description: Customize the validation for your OT devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/operational-technology/operational-technology-manager/add-custom-validation-for-devices.html
release: zurich
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Add a custom validation for devices

Customize the validation for your OT devices.

## Before you begin

The base system for the **sn\_otsm\_sgc.SGOTAssetCustomValidationExtensionPoint** extension point uses the default **sn\_otsm\_sgc.SGOTExcelStagingAssetValidationProcessor** implementation script. You can add a customized validation by creating an implementation for the extension point in the Service Graph Connector for Operational Technology \(Excel\) scope.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Extensions Point** &gt; **Scripted Extension Points**.

2.  Select **sn\_otsm\_sgc.SGOTAssetCustomValidationExtensionPoint**.

3.  Select the **Create Implementation** related link.

    A script include is created where you can add your custom validation.

4.  To add a custom validation, refer to the following validation scenario.\[Omitted image "validation-scenario.png"\] Alt text: Validation scenario for creating custom validations.

5.  Select **Update**.


**Parent Topic:**[Configuring the Service Graph Connector for Microsoft Excel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/operational-technology/operational-technology-manager/configuring-service-graph-connector-for-excel.md)

