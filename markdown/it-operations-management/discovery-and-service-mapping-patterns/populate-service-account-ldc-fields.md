---
title: Enable direct field population for query performance
description: Populate Service Account, Logical Datacenter, and Virtual Machine Object fields in configuration item \(CI\) tables to improve query performance.
locale: en-US
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [Service Account and Logical Datacenter fields, Denormalization, cloud CI query performance, Cloud discovery]
breadcrumb: [Improved query performance with direct field population in CI tables, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Enable direct field population for query performance

Populate Service Account, Logical Datacenter, and Virtual Machine Object fields in configuration item \(CI\) tables to improve query performance.

## Before you begin

Verify that you have at least version 1.30.2 of Discovery and Service Mapping Patterns.

Role required: discovery\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  In the **Name** column, search for `Populate Service Account and LDC IN CMDB`.

3.  Select the **Populate Service Account and LDC IN CMDB** job.

4.  Select the **Active** check box.

5.  Select an option to run the job:

    -   Select **Update** to enable the job to run on its configured schedule.
    -   Select **Execute Now** to run the batch job immediately.

**Parent Topic:**[Improved query performance with direct field population in CI tables](../concept/query-service-account-ldc-fields.md)

**Related topics**  


[Improved query performance with direct field population in CI tables](../concept/query-service-account-ldc-fields.md)

[Available cloud discovery patterns](../concept/available-patterns-cloud.md)

