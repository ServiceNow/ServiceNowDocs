---
title: Use Resource Diagnostics to detect corrupt resource data
description: The Resource Diagnostics feature uses the Application Diagnostics Tool to detect corrupt data for a resource, such as duplicate aggregates for users, or dailies without a top task.
locale: en-US
release: australia
product: Resource Management
classification: resource-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Resource Management classic, Project Portfolio Management, Strategic Portfolio Management]
---

# Use Resource Diagnostics to detect corrupt resource data

The Resource Diagnostics feature uses the Application Diagnostics Tool to detect corrupt data for a resource, such as duplicate aggregates for users, or dailies without a top task.

## Before you begin

Role required: pps\_admin

## Procedure

1.  Navigate to **All** &gt; **Resource** &gt; **Resource Diagnostics**.

2.  On the Application Diagnostics Tool page, select **Resource Management**.

3.  Select one or multiple diagnostic scans.

4.  Select **Run Diagnostics**.

5.  View results of the scan.

    It lists the duplicate aggregate for users or project-related resource allocation dailies without a top task, if any.


## What to do next

Add your own [diagnostic scans](create-diagnostic-scan-map-scripts-rm.md) and [fix scripts](add-diagnostic-and-fix-script-rm.md).

-   **[Add diagnostic features for resource](add-diagnostic-feature-rm.md)**  
Create diagnostic features to evaluate an application feature and organize various diagnostic scans for an application. The diagnostic features appear in the target application and list all the diagnostic scans associated with the diagnostic feature for that application.
-   **[Add diagnostics and fix scripts for resource](add-diagnostic-and-fix-script-rm.md)**  
Add existing or new diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.
-   **[Create diagnostic scan and map scripts for resource](create-diagnostic-scan-map-scripts-rm.md)**  
Create a diagnostics scan and map diagnostic feature with diagnostic and fix scripts. You can create a diagnostic scan to execute diagnostic scripts to check the health of data in your application. Use the fix scripts to rectify any corrupt or invalid data that the diagnostic scan identifies.

**Parent Topic:**[Resource Management classic](../concept/c_ResourceManagement.md)

