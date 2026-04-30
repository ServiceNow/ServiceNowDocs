---
title: Using Enterprise Service Management Integrations Framework
description: Understand how you can use Enterprise Service Management Integrations Framework to connect with a third-party system.
locale: en-US
release: xanadu
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Enterprise Service Management Integrations Framework, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Using Enterprise Service Management Integrations Framework

Understand how you can use Enterprise Service Management Integrations Framework to connect with a third-party system.

## Before you begin

Role required: sn\_hr\_integr\_fw.admin

## Procedure

1.  Create a source.

    For more information, see [Create a source in Enterprise Service Management Integrations Framework](create-source-hrint.md).

2.  Create an integration service for the source.

    For more information, see [Create an integration service in Enterprise Service Management Integrations Framework](create-hr-service-hrint.md).

3.  Create a scheduled job and trigger the run job flow for the source.

    -   Entries are created in the Integration Job Tracker \[sn\_hr\_integr\_fw\_job\_tracker\] table. Entries are created for active Scheduled Pull services in the Integration Service Job Tracker \[sn\_hr\_integr\_fw\_service\_job\_tracker\] table.
    -   Import sets are created and attached to the service job tracker, and load start time is populated. Once data is loaded in the import set tables, the state of the service job tracker changes to loaded and the load end time is populated.
    -   Once data is loaded for all the services, transformation begins based on the service order defined in the Integration Service \[sn\_hr\_integr\_fw\_service\] table. The states of services change to complete, and then the state of the job tracker record changes to complete. For more information, see [View job tracker details](hr-integration-job-tracker.md).

