---
title: Industrial Guided Task standard form
description: The following table describes the field values for the Industrial Guided Task standard form.
locale: en-US
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Industrial Guided Tasks, Reference, Digital Factory Workspace, Industrial Connected Workforce]
---

# Industrial Guided Task standard form

The following table describes the field values for the Industrial Guided Task standard form.

<table id="table_kq5_bvb_1gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-generated unique number for the standard.

</td></tr><tr><td>

Category

</td><td>

Enables you to differentiate between processes in a factory.

</td></tr><tr><td>

Allow ad-hoc request

</td><td>

When enabled, it enables you to initiate tasks directly from the Standards hub.

</td></tr><tr><td>

State

</td><td>

Automatically set to Draft, not editable.

</td></tr><tr><td>

Task expires after

</td><td>

Can be None or Custom time.

</td></tr><tr><td>

Custom time for expiration

</td><td>

Available if Task expires after is set to Custom. Specifies the custom expiration time for the task.

</td></tr><tr><td>

Enable scoring

</td><td>

When enabled, it enables the score field to be displayed and used on guided tasks.

</td></tr><tr><td>

Target score

</td><td>

A numerical value \(float\), which represents the desired score set as a performance goal.

 If a target score is set, the score status indicates whether the task result is Successful or Unsuccessful. If no target score is set, the score status is set to No target available and only the total score is displayed on the guided task.

</td></tr><tr><td>

Short description

</td><td>

Short description or title for the standard.

</td></tr><tr><td>

Owner group

</td><td>

Group of users who own the standard and can approve it.

</td></tr><tr><td>

Author

</td><td>

Auto-populated with the name of the user who initiated the process of creation, can be edited.

</td></tr><tr><td>

Document scope

</td><td>

Specifies whether the standard applies to a single site \(local\) or across all sites \(global\).

</td></tr><tr><td>

Location

</td><td>

Required for the document scope local. Factory that the standard is used for.

</td></tr><tr><td>

Material classifications

</td><td>

Groups of materials based on their properties and applications. Stored in the Enterprise model classification \[sn\_ent\_model\_classification\] table.

</td></tr><tr><td>

Material models

</td><td>

Categories of finished goods based on the materials they are made from. Stored in the Enterprise good models \[sn\_ent\_model\] table.

</td></tr><tr><td>

CMDB assignment type

</td><td>

Options are: -   Equipment models
-   Specific equipment
-   Functional location

</td></tr><tr><td>

Functional locations

</td><td>

Work area where the standard is executed.

</td></tr><tr><td>

Equipment models

</td><td>

Group of equipment items. This field is required if the CMDB assignment type is set to Equipment models. Available options vary depending on the selected functional location.**Note:**

To make the filtering by equipment model work, make sure that the equipment is related to the equipment model. This connection is established by using the **model ID** reference field to establish the relationship. When you select a functional location, this relationship is then used to filter down the equipment models.

</td></tr><tr><td>

Equipment

</td><td>

Piece of equipment or machinery used to execute the standard. This field is required if the CMDB assignment type is set to **Specific equipment**. Available options vary depending on the selected functional location.

</td></tr><tr><td>

Failure modes

</td><td>

Failure mode to which the standard relates. Available options depend on the selected functional location or equipment.

</td></tr><tr><td>

LOTO level

</td><td>

Lockout/Tagout safety procedures with possible values of 0-3.

</td></tr><tr><td>

Line status

</td><td>

Information about the status of the production line. Options are:-   None
-   Running
-   Stopped

</td></tr><tr><td>

Required skills

</td><td>

Defines the set of skills required for task eligibility. Only operators with these skills can perform the task.

</td></tr><tr><td>

Knowledge Article

</td><td>

Knowledge articles that are related to the standard and provide more information about the standard for the operator who executes the task.

</td></tr><tr><td>

Attachments

</td><td>

Attachment that can be used for descriptive purposes.

</td></tr></tbody>
</table>## Insights Overview tab

The Insights Overview tab displays embedded shopfloor insights for the published standard. This tab is visible on every IGT standard record in the Digital Factory Workspace when the standard is not in Draft or Review state.

**Note:** The Insights Overview tab displays data related to the published standard, showing all execution results across versions.

The following filters are available on the Insights Overview tab:

<table id="table_ccq_1h3_23c"><thead><tr><th>

Filter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Functional location

</td><td>

Filter by functional location. All available functional locations are displayed by default. You can manually select the functional locations, which you want to filter.

</td></tr><tr><td>

Equipment

</td><td>

Filter by equipment. Only equipment relevant to the selected functional location is shown.

</td></tr><tr><td>

Date filter

</td><td>

Filter by time period. Options include: -   Last day
-   Today
-   Last week \(default\)
-   Last 15 days
-   Last month
-   This month
-   Last 6 months

</td></tr><tr><td>

Version

</td><td>

Filter by standard version to compare execution results across versions and track how changes affect performance.

</td></tr></tbody>
</table>**Parent Topic:**[Industrial Guided Tasks reference](industrial-guided-tasks-reference.md)

