---
title: Integrating with Coupa
description: Integrating Coupa with Software Asset Management helps you create software requisitions directly on Coupa. Software Asset Management tracks these requisitions and automatically generates entitlements or entitlement import errors after these requisitions are received on Coupa.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Integrating with external procurement applications, Procurement, Asset Management, IT Service Management]
---

# Integrating with Coupa

Integrating Coupa with Software Asset Management helps you create software requisitions directly on Coupa. Software Asset Management tracks these requisitions and automatically generates entitlements or entitlement import errors after these requisitions are received on Coupa.

**Note:** This integration doesn't pull requisitions created on Coupa to Software Asset Management.

## Before you begin

-   Install the Asset Management - Procurement Integration \(app-itam-procurement-integration\) store application from ServiceNow Store. For more information, see [Install Asset Management - Procurement Integration](../task/install-proc-int.md).
-   You must have the Software Asset Management Enterprise license.
-   Activate the Coupa spoke. For more information, see [Coupa Spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/coupa-spoke.md).
-   Activate the Procurement plugin \(com.snc.procurement\). For more information, see [Activate Procurement](../task/t_ActivateProcurement.md).

## Synchronize reference data

Both ServiceNow Procurement and Coupa have theirs own set of tables and reference data types. For a smooth and successful integration, you must synchronize the data you would refer. For more information, see [Reference data synchronization](../reference/ref-data-coupa.md).

**Warning:** If you don't synchronize data, you might encounter a few issues while creating a requisition on Coupa.

