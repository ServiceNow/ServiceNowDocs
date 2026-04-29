---
title: Inserting multiple records using insertMultiple
description: You can insert multiple records in one SOAP request by using the insertMultiple operation.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Web service import sets, Import sets, Imports, Workflow Data Fabric]
---

# Inserting multiple records using insertMultiple

You can insert multiple records in one SOAP request by using the insertMultiple operation.

By default, insertMultiple operations create new import sets in **Synchronous** mode. To process new import sets asynchronously, activate the business rule Insert multiple asynchronous mode.

The insertMultiple operation is available for the Direct Web Service API and Web Service Import Sets. To enable insertMultiple, activate the Insert Multiple Web Service plugin.

**Note:** Activating this plugin adds a new operation to the SOAP WSDL. After this plugin is activated, consume a new WSDL to update your web services client.

**Parent Topic:**[Web service import sets](../concept/c_WebServiceImportSets.md)

