---
title: Publish a work set standard
description: Create a work set standard, add sub-activities, and request approval to publish it so that line leaders and operators can run it on the shop floor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/publish-work-set-standard.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: task
last_updated: "2026-05-25"
reading_time_minutes: 1
keywords: [publish work set standard, create work set]
breadcrumb: [Standard and task life cycles, Industrial Standards, Use, Digital Factory Workspace, Industrial Connected Workforce]
---

# Publish a work set standard

Create a work set standard, add sub-activities, and request approval to publish it so that line leaders and operators can run it on the shop floor.

## Before you begin

Role required: sn\_icw\_std.work\_set\_standard\_author

## Procedure

1.  Navigate to the **Standards hub**.

2.  Select **New standard**.

3.  On the **Work set** tile, select **New standard**.

4.  On the work set standard form, fill in the fields.

    For field descriptions, see [Work set standard form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-form.md).

5.  Select **Save**.

    The standard is saved in the **Draft** state and appears as a tile in the Standards hub.

6.  Open the **Sub-activities** tab.

7.  For each step in the procedure, select **New** and add a sub-activity.

    Set the sub-activity **Type** to one of the following values.

    -   **Standard**: Select a published Industrial Guided Task standard to run as part of the work set. Work set standards can't reference other work set standards.
    -   **Action**: Enter a short description for an industrial action that the system creates when the work set runs.
    For field descriptions, see [Work set sub-activity form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-sub-activity-form.md).

8.  When the standard is ready for review, select **Request approval**.

    An approval request is sent to active members of the owner group. If the owner group has no active users, the request is blocked and a message appears.

    For the standard state transitions, see [Work set standard and task life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-task-life-cycle.md).


## Result

When an approver in the owner group approves the request, the standard moves to the **Published** state. A published work set standard can be scheduled and run from the Standards hub.

**Parent Topic:**[Work set standard and task life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-task-life-cycle.md)

