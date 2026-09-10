---
title: Convert a service instance to Lightweight Service Model
description: Convert a Service Mapping service instance to Lightweight to minimize storage footprint and optimize performance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-mapping/convert-service-instance-lightweight.html
release: australia
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2026-08-09"
reading_time_minutes: 1
keywords: [service mapping, lightweight service, convert service, service architecture]
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Convert a service instance to Lightweight Service Model

Convert a Service Mapping service instance to Lightweight to minimize storage footprint and optimize performance.

## Before you begin

-   Verify that the Service Mapping Plus store app is up to date.

Role required: service\_mapping\_admin

## About this task

When you convert a service instance to Lightweight, the system deletes the existing historical snapshot data and reconfigures the service to operate under the Lightweight architecture. The service continues to calculate membership automatically, but only current state data is retained going forward.

**Note:** Converting a service instance to Lightweight is permanent and irreversible.

Supported service types for conversion:

-   Dynamic
-   Tag-based

For detailed information on the Lightweight Service Model, see [Service Mapping Lightweight Service Model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/sm-lightweight-service-model.md).

## Procedure

1.  In the navigation filter, enter: `cmdb_ci_service_calculated_list.do`.

2.  In the **Calculated Application Services** list, select a service instance of type Dynamic or Tag-Based.

3.  On the service record, locate the **Related Links** section and select the **Convert to Lightweight** link.

    \[Omitted image "lightweight-link.png"\] Alt text: Convert to Lightweight link

4.  In the confirmation dialog, review the warning about deleting historical data.

    1.  If you need to preserve historical snapshots, select **Cancel** and complete any required analysis before proceeding.

    2.  If you're ready to proceed, select **Convert**.

    A notification appears: "Converting service to Lightweight. This may take a few minutes." Keep the page open during the conversion process. Don't navigate away or close the page until the conversion is complete.


## Result

The service operates under the Lightweight Service Model.

**Parent Topic:**[Using Service Mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-mapping/using-service-mapping.md)

