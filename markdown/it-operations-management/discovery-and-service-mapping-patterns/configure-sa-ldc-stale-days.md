---
title: Set the Populate Service Account and LDC job stale threshold
description: Configure the number of days before a running Populate Service Account and LDC IN CMDB job is considered stale and canceled. Increase this value if a large configuration item \(CI\) dataset causes the job to be canceled before a full run completes.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/configure-sa-ldc-stale-days.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-07-19"
reading_time_minutes: 2
keywords: [PopulateSALDC, stale job threshold, system property, service account, logical data center, CI tables]
breadcrumb: [Improved query performance with direct field population in CI tables, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Set the Populate Service Account and LDC job stale threshold

Configure the number of days before a running **Populate Service Account and LDC IN CMDB** job is considered stale and canceled. Increase this value if a large configuration item \(CI\) dataset causes the job to be canceled before a full run completes.

## Before you begin

Verify that you have at least version 1.30.2 of Discovery and Service Mapping Patterns.

Role required: admin

## About this task

The **sn\_itom\_pattern.populate\_saldc.stale\_job\_threshold\_days** system property controls how long the **Populate Service Account and LDC IN CMDB** scheduled job can run before the system considers it stale. If the job exceeds this threshold, the system automatically cancels it and starts a new run. The default value is two days. If your instance has many CI records, you can increase this value to give the job more time to complete.

## Procedure

1.  In the navigation filter, enter `sys_properties.list`.

2.  In the **Name** field, search for `sn_itom_pattern.populate_saldc.stale_job_threshold_days`.

3.  Select the **sn\_itom\_pattern.populate\_saldc.stale\_job\_threshold\_days** property.

4.  In the **Value** field, enter the number of days after which the job is considered stale.

5.  Select **Update**.


## What to do next

Wait for the next scheduled run of the **Populate Service Account and LDC IN CMDB** job, or execute it immediately. For more information, see [Enable direct field population for query performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/populate-service-account-ldc-fields.md).

**Parent Topic:**[Improved query performance with direct field population in CI tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/query-service-account-ldc-fields.md)

**Related topics**  


[Improved query performance with direct field population in CI tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/query-service-account-ldc-fields.md)

[Enable direct field population for query performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/populate-service-account-ldc-fields.md)

[Trigger a full CI table resync for direct field population](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/configure-sa-ldc-full-resync.md)

