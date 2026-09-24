---
title: Configure the default AI status report template
description: Configure which template ServiceNow Otto should use by default when it generates an AI status report.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/config-default-ai-status-report-template.html
release: brazil
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Configuring Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure the default AI status report template

Configure which template ServiceNow Otto should use by default when it generates an AI status report.

## Before you begin

Role required: admin

## About this task

ServiceNow Otto generates AI status reports using a default template. You can change the default template using a system property.

## Procedure

1.  Navigate to **All** and type in **sys\_properties.list** in the filter box.

2.  Open the **sn\_pw.ai\_project\_status\_report\_default\_templateId** property.

3.  In the **Value** field, enter the sys\_id of the template that you want to use as the default.

4.  Select **Update**.


## Result

The next AI status report that generates uses the specified template as the default.

**Note:** If you don't set this property, ServiceNow Otto uses the out-of-box default template.

**Parent Topic:**[Configuring Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-workspace/configure-pw.md)

