---
title: Update execution URLs for planning item demands
description: Run this scheduled job after upgrading to update execution URLs on existing demand planning items so they redirect correctly to the Demands module.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/portfolio-planning/update-execution-urls-for-existing-demands.html
release: zurich
product: Portfolio Planning
classification: portfolio-planning
topic_type: task
last_updated: "2026-07-30"
reading_time_minutes: 1
keywords: [update, execution URL, demand, scheduled job, Demand Workspace]
breadcrumb: [Configuring Prioritization and Roadmap settings in Portfolio Planning, Configure, Portfolio Planning, Strategic Portfolio Management]
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

**Parent Topic:**[Configuring Prioritization and Roadmap settings in Portfolio Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/portfolio-planning/configuring-prioritization-and-roadmap-settings-in-portfolio-planning.md)

