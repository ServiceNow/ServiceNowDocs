---
title: Create diagnostic scan and map scripts for resource
description: Create a diagnostics scan and map diagnostic feature with diagnostic and fix scripts. You can create a diagnostic scan to execute diagnostic scripts to check the health of data in your application. Use the fix scripts to rectify any corrupt or invalid data that the diagnostic scan identifies.
locale: en-US
release: yokohama
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Use Resource Diagnostics to detect corrupt resource data, Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Create diagnostic scan and map scripts for resource

Create a diagnostics scan and map diagnostic feature with diagnostic and fix scripts. You can create a diagnostic scan to execute diagnostic scripts to check the health of data in your application. Use the fix scripts to rectify any corrupt or invalid data that the diagnostic scan identifies.

## Before you begin

-   Role required: adt\_admin
-   Create diagnostic features. For more information, see [Add diagnostics features for resource](add-diagnostic-feature-rm.md).
-   Create diagnostic and fix scripts. For more information, see [Add diagnostics and fix scripts](add-diagnostic-and-fix-script-rm.md).

## About this task

After creating diagnostic features, diagnostic scripts, and fix scripts, map the diagnostic features and scripts to create a diagnostic scan. You can map multiple scripts with each diagnostic scan and define the order of their execution.

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Diagnostics**.

2.  Select **New**.

3.  On the Diagnostics form, fill the fields.

    For a description of the field names, see [Diagnostics form](../reference/diagnostics-form.md).

4.  Search for and select diagnostic scripts to map with the diagnostic scan in the **Diagnostics and Script Mappings** section.

5.  Select **Submit**.


**Parent Topic:**[Use Resource Diagnostics to detect corrupt resource data](use-resource-diagnostics.md)

