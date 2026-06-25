---
title: Create a safety incident from an ICW task
description: Create a safety incident directly from an existing ICW task when the task reveals a safety-related issue.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/icw-create-safety-incident-from-task.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [ICW Health and Safety Integration, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Create a safety incident from an ICW task

Create a safety incident directly from an existing ICW task when the task reveals a safety-related issue.

## Before you begin

Role required: sn\_icw.safety\_incident\_user

## About this task

You may discover a safety issue while working on an action, deviation, or Industrial Guided Task. The safety incident requires formal reporting. Creating a safety incident from the task automatically links the two records through the origin field that provides context for investigation.

## Procedure

1.  Navigate to **Workspaces** &gt; **Digital Factory Workspace**.

2.  Select the task from which you want to create a safety incident.

    You can create safety incidents from the following task types:

    -   Actions
    -   Deviations
    -   Root Cause Analysis
3.  Select More Actions \(\[Omitted image "more-actions.png"\] Alt text:\) in the top corner.

4.  Select **Report safety incident**.

5.  On the Safety Incident form, review the pre-populated fields.

    The following fields are automatically populated from the originating task:

    -   Short description
    -   Opened by
    -   Assigned to
    -   Functional location
6.  Complete the remaining required fields, including the incident summary.

7.  Add attachments to provide additional context.

8.  Select **Submit**.


## Result

The safety incident is created and linked to the originating task through the origin field. The incident appears in the safety incidents list and in the Related tab of the originating task.

**Parent Topic:**[Using ICW Health and Safety Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/using-icw-health-and-safety-integration.md)

**Related topics**  


[Exploring Industrial Connected Workforce Integration with Health and Safety Incident Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/icw-health-and-security-integraton.md)

[View safety incidents in the Digital Factory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/icw-view-safety-incident.md)

