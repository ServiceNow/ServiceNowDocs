---
title: Data Stream \(Integration Hub\) data source
description: Enable platform Data Sources to load data from Integration Hub Data Stream actions.
locale: en-US
release: australia
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data sources, Import sets, Imports, Workflow Data Fabric]
---

# Data Stream \(Integration Hub\) data source

Enable platform Data Sources to load data from Integration Hub Data Stream actions.

A Data Stream is a stream of response data larger than 10 MB or data that returns paginated results. Successful execution of the Data Stream action returns a complex data output stream that the Data Source consumes. For more information, see [Data stream actions and pagination](../../integrationhub/concept/data-stream-actions.md).

Complex data allows you to encode and store structured data in a machine-readable format. Based on Data Source configuration, complex objects can be either flattened into an import table or serialized completely as JSON data into a single column.

Complex data includes parent and child objects and nested objects, as shown in the following example:

![Complex object](../image/complex-object.png)

For more information, see [Complex data](https://www.servicenow.com/docs/access?context=complex-data&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

