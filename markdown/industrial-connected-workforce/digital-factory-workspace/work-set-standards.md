---
title: Work set standards
description: Use a work set standard to group related standards and actions into a single procedure that operators can execute as one guided flow on the shop floor.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/work-set-standards.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-05-25"
reading_time_minutes: 2
keywords: [work set standard, grouped standard, sub-activity]
breadcrumb: [Industrial Standards, Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Work set standards

Use a work set standard to group related standards and actions into a single procedure that operators can execute as one guided flow on the shop floor.

Complex shop floor processes such as Clean-Inspect-Lubricate \(CIL\), changeover, and line startup involve multiple sub-activities that have different schedules, dependencies, and triggers. A work set standard organizes these sub-activities into one standard so process engineers can plan the whole process once and operators can execute it as a single flow.

## Components of a work set standard

A work set standard has three components.

-   **Work set standard**

    The grouped standard record that defines scope, ownership, location, and the sub-activities that are part of the procedure.

-   **Sub-activity**

    An individual step in the work set standard. A sub-activity can be of type **Standard** \(links to a published Industrial Guided Task standard\) or **Action** \(creates an industrial action when the work set runs\).

-   **Work set task**

    The execution record that is created when a work set standard runs. When the work set task is created, the system generates a standard task or action for each sub-activity.


## Roles for work set standards

The following roles control who can author, supervise, and execute a work set standard.

|Role|Description|
|----|-----------|
|`sn_icw_std.work_set_standard_author`|Assigned to process engineers. Can create, update, and publish work set standards and sub-activities.|
|`sn_icw_std.work_set_expert`|Assigned to line leaders. Can cancel work set tasks and perform user actions.|
|`sn_icw_std.work_set_user`|Assigned to operators. Can execute work set tasks and the child tasks that they generate.|

**Note:** The standard author role inherits the expert role, and the expert role inherits the user role.

## When to use a work set standard

Use a work set standard when a single shop floor procedure includes several related activities that share scope, schedule, or location. Common examples include daily maintenance routines, line startups, and product changeovers.

Do not use a work set standard for a single, standalone task. For those cases, use an Industrial Guided Task standard.

**Parent Topic:**[Exploring Industrial Standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-standards-landing-page.md)

**Related topics**  


[Work set standard and task life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-task-life-cycle.md)

[Components installed with work set standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/components-installed-with-work-set-standards.md)

[Work set standard form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-form.md)

[Work set sub-activity form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-sub-activity-form.md)

