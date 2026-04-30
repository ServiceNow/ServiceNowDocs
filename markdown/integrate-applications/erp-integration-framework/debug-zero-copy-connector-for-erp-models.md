---
title: Debug Zero Copy Connector for ERP models
description: Use the debug models option in Zero Copy Connector for ERP to see a log capturing the probe payload, payload response, status, and other information.
locale: en-US
release: zurich
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, debug, model, log, payload, status]
breadcrumb: [Building models, Use, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Debug Zero Copy Connector for ERP models

Use the debug models option in Zero Copy Connector for ERP to see a log capturing the probe payload, payload response, status, and other information.

## Before you begin

This feature is available starting with the Zurich Patch 4 release.

Role required: sn\_erp\_integration.erp\_admin

## About this task

View debug logs from within Zero Copy Connector for ERP to obtain information about requests, responses, and payloads without having to open Workflow Studio.

Keep the following guidance in mind when debugging Zero Copy Connector for ERP models:

-   Turn debugging on and off as needed.
-   Debug logs are stored and accessible for the current session only.
-   Debug logs are cleared on a daily basis automatically.
-   When probe executions happen outside of "Use ERP Data" flows, only transaction IDs are stored. Flow context IDs are not stored.
-   For probe executions triggered via "Use ERP" flows, flow context IDs are stored.

## Procedure

1.  To turn on debugging, navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Enable Data Product Debugging**.

2.  Select **Confirm**.

3.  To view the logs, navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Open Debug Logs**.

    Debug logs enable you to see information about flow engine context, probe communication, probe payload, payload response, status, and more.

    For details about the columns in debug logs, see [Zero Copy Connector for ERP debug logs field descriptions](../reference/erp-canvas-debug-logs-columns.md).

4.  To turn off debugging, navigate to **All** &gt; **Zero Copy Connector for ERP** &gt; **Disable ERP Models Debugging**.

5.  Select **Confirm**.


**Parent Topic:**[Building and managing models to work with ERP data](../concept/work-with-erp-data-models.md)

