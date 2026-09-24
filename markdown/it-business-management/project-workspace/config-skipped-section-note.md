---
title: Configure standard note for a skipped status report section
description: Configure a standard note that ServiceNow Otto appends to an AI status report section when it skips that section.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/project-workspace/config-skipped-section-note.html
release: brazil
product: Project Workspace
classification: project-workspace
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 1
breadcrumb: [Configuring Project Workspace, Project Workspace, Project Portfolio Management, Strategic Portfolio Management]
---

# Configure standard note for a skipped status report section

Configure a standard note that ServiceNow Otto appends to an AI status report section when it skips that section.

## Before you begin

Role required: admin

## About this task

ServiceNow Otto can skip a section of an AI status report and append a standard note that you configure when no data or criteria applies to that section.

## Procedure

1.  Navigate to **All** and type in **sys\_properties.list** in the filter box.

2.  Open the **NAStatusReportCustomConfig** script include.

3.  In the `SKIPPED_SECTIONS_CONFIG` object, locate the entry for the section that you want to configure, such as `resource_rag_health`.

4.  Uncomment the entry if it is commented out, and enter the note text that you want to display.

    The example entries ship commented out, so no note appends unless you opt in.

5.  Select **Update**.


## Result

The next time ServiceNow Otto skips the configured section, the section editor displays your note as a bullet. This note also appends to the overall health rationale.

**Parent Topic:**[Configuring Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-business-management/project-workspace/configure-pw.md)

