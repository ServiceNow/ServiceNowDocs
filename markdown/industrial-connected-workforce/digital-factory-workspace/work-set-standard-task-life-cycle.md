---
title: Work set standard and task life cycles
description: A life cycle is the list of states that a work set standard or work set task can go through from creation to closure.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/work-set-standard-task-life-cycle.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-05-25"
reading_time_minutes: 3
keywords: [work set life cycle, states]
breadcrumb: [Industrial Standards, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Work set standard and task life cycles

A life cycle is the list of states that a work set standard or work set task can go through from creation to closure.

## Work set standard states

|State|Description|
|-----|-----------|
|Draft|The standard can be edited by users with the work set standard author role.|
|Review|An approval request has been sent to the owner group. The standard can't be edited.|
|Published|The standard is active and can be scheduled or run from the Standards hub. The standard can't be edited.|
|Retired|The standard is inactive and can't be requested. The standard is read-only and can't be edited.|
|Revised|End state for an older version that has been replaced by a newer version. The standard is read-only and can't be edited.|

## Approval states

|State|Description|
|-----|-----------|
|Not yet requested|The standard has not been submitted for approval.|
|Requested|The approval request is awaiting review. Any active user in the owner group can approve the request.|
|Approved|The request has been approved. The state of the standard changes to **Published**.|
|Rejected|The request has been rejected. The state of the standard moves back to **Draft**.|
|Canceled|The request was withdrawn before a decision was made.|

## Work set task states

|State|Description|
|-----|-----------|
|Ready|The work set task is created and waiting to be picked up.|
|Work in Progress|The work set task is being executed. The system records the actual start time on entry to this state and moves the task to this state automatically when a child task starts or a child action closes.|
|On Hold|The work set task is paused. Operators can resume it by setting it back to **Work in Progress**.|
|Closed Complete|All child records are submitted or closed and the operator has submitted the work set task. The system records the actual end time.|
|Closed Skipped|The work set task has expired. Active child tasks move to **Closed Skipped** and active child actions move to **Canceled**.|
|Canceled|The work set task has been canceled by a work set expert. Active child tasks move to **Canceled** and active child actions move to **Canceled**.|

**Important:** A work set task can't be closed while it has active child tasks. Complete or cancel the remaining child records first.

-   **[Create a work set standard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/create-work-set-standard.md)**  
Create and update a work set standard or create a copy of a published or retired work set standard, and use it as a template for a new one.
-   **[Execute a work set task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/execute-work-set-task.md)**  
Run a work set task to complete all sub-activities of the underlying work set standard as part of one guided flow.
-   **[Publish a work set standard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/publish-work-set-standard.md)**  
Create a work set standard, add sub-activities, and request approval to publish it so that line leaders and operators can run it on the shop floor.

**Parent Topic:**[Using Industrial Standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/using-industrial-standards.md)

**Related topics**  


[Create a work set standard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/create-work-set-standard.md)

[Execute a work set task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/execute-work-set-task.md)

[Publish a work set standard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/publish-work-set-standard.md)

[Components installed with work set standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/components-installed-with-work-set-standards.md)

[Work set standard form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-form.md)

[Work set sub-activity form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-sub-activity-form.md)

