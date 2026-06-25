---
title: Add diagnostic and fix scripts
description: Add diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-management/add-diagnostic-and-fix-script.html
release: australia
product: Project Management
classification: project-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Project Diagnostics, Using Project Management, Project Management, Project Portfolio Management, Strategic Portfolio Management]
---

# Add diagnostic and fix scripts

Add diagnostic scripts to scan the data in your application for any corruption. You can also attach fix scripts to rectify the corrupt or invalid data identified by the diagnostic script.

## Before you begin

Role required: adt\_admin

## About this task

The results of the filter conditions that you specify in a [diagnostic feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/add-diagnostic-feature.md) are used as an input for the diagnostic script while executing. You can also use the result of one script in subsequent scripts.

## Procedure

1.  Navigate to **All** &gt; **Application Diagnostics Tool** &gt; **Scripts**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For more information, see [Diagnostic Scripts form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/diagnostic-scripts-form.md).

4.  Include a script for fixing the corrupt or invalid data identified by the diagnostic script.

    1.  Select the **Has Fix script** check box.

    2.  Select the Edit User Roles icon \(\[Omitted image "edit\_user\_roles\_icon.png"\] Alt text: Edit User Roles icon\) and choose the roles that can access the diagnostic script.

    3.  In the **Fix script** section, add the code for the fix script.

5.  Select **Submit**.


**Related topics**  


[Project Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/project-management/project-diagnostics-overview.md)

