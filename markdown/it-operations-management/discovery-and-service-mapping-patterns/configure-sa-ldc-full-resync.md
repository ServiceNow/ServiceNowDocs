---
title: Trigger a full CI table resync for direct field population
description: Trigger the Populate Service Account and LDC IN CMDB scheduled job to reprocess all configuration item \(CI\) records. Configure the sn\_itom\_pattern.populate\_saldc\_full\_resync system property when service accounts or logical datacenters have incorrect or corrupted values for a CI.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/configure-sa-ldc-full-resync.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-07-19"
reading_time_minutes: 2
keywords: [PopulateSALDC, full resync, system property, service account, logical data center, CI tables, data inconsistency]
breadcrumb: [Improved query performance with direct field population in CI tables, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Trigger a full CI table resync for direct field population

Trigger the **Populate Service Account and LDC IN CMDB** scheduled job to reprocess all configuration item \(CI\) records. Configure the **sn\_itom\_pattern.populate\_saldc\_full\_resync** system property when service accounts or logical datacenters have incorrect or corrupted values for a CI.

## Before you begin

Verify that you have at least version 1.35.0 of Discovery and Service Mapping Patterns.

Role required: admin

## About this task

The scheduled job normally processes only CI records created since its last run. Setting the **sn\_itom\_pattern.populate\_saldc\_full\_resync** property to true configures the next job run to reprocess all CI records. The system automatically resets the property to false after the resync completes.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** field, search for `sn_itom_pattern.populate_saldc_full_resync`.

3.  Select the **sn\_itom\_pattern.populate\_saldc\_full\_resync** property.

4.  In the **Value** field, enter `true`.

5.  Select **Update**.


## What to do next

Wait for the next scheduled run of the **Populate Service Account and LDC IN CMDB** job, or execute it immediately. For more information, see [Enable direct field population for query performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/populate-service-account-ldc-fields.md).

**Parent Topic:**[Improved query performance with direct field population in CI tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/query-service-account-ldc-fields.md)

**Related topics**  


[Improved query performance with direct field population in CI tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/query-service-account-ldc-fields.md)

[Enable direct field population for query performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/populate-service-account-ldc-fields.md)

[Set the Populate Service Account and LDC job stale threshold](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/configure-sa-ldc-stale-days.md)

