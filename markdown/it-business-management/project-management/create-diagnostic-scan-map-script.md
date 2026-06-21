---
title: Create Diagnostic scans and map related scripts
description: Once you have created diagnostic features and scripts, map them to a diagnostic scan to check the health of data in your application. Use fix scripts to rectify any corrupt or invalid data that the diagnostic scan identifies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/it-business-management/project-management/create-diagnostic-scan-map-script.html
release: yokohama
product: Project Management
classification: project-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Project Diagnostics, Use, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Create Diagnostic scans and map related scripts

Once you have created diagnostic features and scripts, map them to a diagnostic scan to check the health of data in your application. Use fix scripts to rectify any corrupt or invalid data that the diagnostic scan identifies.

## Before you begin

In order to create a diagnostic scan, you must have already created diagnostic features and scripts For more information, see [Create and add diagnostic features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-management/add-diagnostic-feature.md) and [Add diagnostic and fix scripts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-management/add-diagnostic-and-fix-script.md).

Role required: adt\_admin

## About this task

You can map multiple scripts with each diagnostic scan and define the order of their execution.

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Diagnostics**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the diagnostic scan. This name appears in the application to which this diagnostic scan belongs.\[Omitted image "diagnostic\_scan\_name.png"\] Alt text: Diagnostic scan name in the application|
    |Active|Option for activating the diagnostic scan.|
    |Order|Order in which this diagnostic scan appears in the application.|
    |Feature|Diagnostic feature with which you want to associate this diagnostic scan.|
    |Roles|Option for adding or removing user roles that can access the diagnostic scan.|
    |Description|Details of the diagnostic scan. The description is displayed in the application to which the diagnostic scan belongs.\[Omitted image "diagonstic\_scan\_description.png"\] Alt text: Diagnostic scan description in application|

4.  Click the Roles icon \(\[Omitted image "edit\_user\_roles\_icon.png"\] Alt text: Edit user roles icon\) and move the desired roles to the Selected list.

    The users with the selected roles can access the diagnostic script.

5.  Search for and select diagnostic scripts to map with the diagnostic scan in the **Diagnostics and Script Mappings** section.

6.  Click **Submit**.


## What to do next

-   Create related link for navigating to the diagnostic features and scans in the application. For more information, see Create a UI action.
-   Run diagnostic scan and view results. For an example of how the diagnostics scan work, see [Use Project Diagnostics to detect corrupt project data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/it-business-management/project-management/project-diagnostics.md).

