---
title: Work set standard form
description: The following table describes the field values for the work set standard form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/industrial-connected-workforce/digital-factory-workspace/work-set-standard-form.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-05-25"
reading_time_minutes: 2
keywords: [work set standard form]
breadcrumb: [Industrial Standards, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Work set standard form

The following table describes the field values for the work set standard form.

<table id="table_work_set_standard_form"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the standard.

</td></tr><tr><td>

Short description

</td><td>

Title for the standard.

</td></tr><tr><td>

Category

</td><td>

Process category that the standard belongs to, used to differentiate between processes in a factory.

</td></tr><tr><td>

State

</td><td>

Current state of the standard. Set to **Draft** when the standard is created. Not editable.

</td></tr><tr><td>

Owner group

</td><td>

Group of users who own the standard. Members of this group receive approval requests for the standard.

</td></tr><tr><td>

Author

</td><td>

User who created the standard. Auto-populated and editable.

</td></tr><tr><td>

Document scope

</td><td>

Scope of the standard. Options are:-   **Local**: The standard applies to a single site.
-   **Global**: The standard applies to all sites.

</td></tr><tr><td>

Location

</td><td>

Factory site that the standard applies to. Required when **Document scope** is **Local**.

</td></tr><tr><td>

Material classifications

</td><td>

Groups of materials based on their properties and applications. Stored in the Enterprise model classification \[sn\_ent\_model\_classification\] table.

</td></tr><tr><td>

Material models

</td><td>

Categories of finished goods based on their materials. Stored in the Enterprise good models \[sn\_ent\_model\] table.

</td></tr><tr><td>

CMDB assignment type

</td><td>

Type of equipment assignment. Options are:-   Equipment models
-   Specific equipment
-   Functional location

</td></tr><tr><td>

Functional locations

</td><td>

Work area where the standard is executed.

</td></tr><tr><td>

Equipment models

</td><td>

Group of equipment items. Required when **CMDB assignment type** is **Equipment models**. Available options depend on the selected functional location.

</td></tr><tr><td>

Equipment

</td><td>

Piece of equipment or machinery used to execute the standard. Required when **CMDB assignment type** is **Specific equipment**. Available options depend on the selected functional location.

</td></tr><tr><td>

Failure modes

</td><td>

Failure mode that the standard relates to. Available options depend on the selected functional location or equipment.

</td></tr><tr><td>

LOTO level

</td><td>

Lockout/Tagout safety level. Possible values are 0 to 3.

</td></tr><tr><td>

Line status

</td><td>

Required status of the production line. Options are:-   None
-   Running
-   Stopped

</td></tr><tr><td>

Knowledge Article

</td><td>

Knowledge articles that provide background for the operator who runs the task.

</td></tr><tr><td>

Attachments

</td><td>

Files that support the standard, such as reference documents or diagrams.

</td></tr></tbody>
</table>## Tabs on the work set standard form

The following tabs appear on the work set standard form.

|Tab|Description|
|---|-----------|
|Sub-activities|Lists the sub-activities that make up the work set. Add and edit sub-activities while the standard is in the **Draft** state. For field descriptions, see [Work set sub-activity form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-sub-activity-form.md).|
|Schedule plan|Calendar view of the schedule plans that generate work set tasks from this standard.|
|Open tasks|Lists the work set tasks generated from this standard. Available only when tasks exist.|
|Approval|Lists approval records for the standard. Available when an approval request has been sent.|
|Versioning|Lists prior versions of the standard. Available when the standard has at least one published version.|

**Parent Topic:**[Industrial Standards reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/industrial-standards-reference.md)

**Related topics**  


[Work set standards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standards.md)

[Work set standard and task life cycles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/industrial-connected-workforce/digital-factory-workspace/work-set-standard-task-life-cycle.md)

