---
title: Update execution URLs for planning item demands
description: Run this scheduled job after upgrading to update execution URLs on existing demand planning items so they redirect correctly to the Demands module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/update-execution-url-for-demand-spw.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-08-04"
reading_time_minutes: 1
breadcrumb: [Prioritization display settings in Strategic Planning, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Update execution URLs for planning item demands

Run this scheduled job after upgrading to update execution URLs on existing demand planning items so they redirect correctly to the Demands module.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Scheduler** &gt; **Scheduled Jobs**.

2.  Enter `Update Demand Planning Item Execution URL` in the **Name** search field.

3.  Select **Update Demand Planning Item Execution URL** from the scheduled job search list.

4.  Review the scheduled job details to check that the name and run settings are correct.

5.  Select **Execute Now**.


## Result

The execution URL for planning item demands is updated to redirect to the execution demands in the Demands module.

**Parent Topic:**[Prioritization display settings in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/configuring-prioritization-and-roadmap-settings-strategic-planning.md)

