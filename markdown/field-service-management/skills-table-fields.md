---
title: Skills table fields
description: Field reference for skills management records in Field Service Management, including Task Skills, User Skills, Group Skills, and User Skill History tables.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/field-service-management/skills-table-fields.html
release: brazil
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Reference, Field Service Management]
---

# Skills table fields

Field reference for skills management records in Field Service Management, including Task Skills, User Skills, Group Skills, and User Skill History tables.

## About skill records

This reference topic documents the fields in the four primary skill-related tables in Field Service Management.

-   Task Skills: for work order tasks
-   User Skills: for individual technicians
-   Group Skills: for groups of technicians
-   User Skill History: for tracking skill changes over time

## Task Skills Table

Table name: task\_m2m\_skill

The Task Skills table stores the skills required to complete a work order task. Use this table to specify which skills are mandatory, their required levels, and other skill qualifications for task assignment.

<table id="table_qrf_qwb_jkc"><thead><tr><th>

Field

</th><th>

Type

</th><th>

Default

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Skill**

</td><td>

Reference

</td><td>

None

</td><td>

Yes

</td><td>

The specific skill or qualification required to complete the task. Select from the list of available skills created in your system.

</td></tr><tr><td>

**Mandatory**

</td><td>

Checkbox

</td><td>

Unchecked

</td><td>

No

</td><td>

Indicates whether this skill is required for technicians to be assigned to the task. If checked, technicians must have this skill to be considered for assignment.

If unchecked, the skill is optional. Technicians without it may still be assigned based on other skills or matching criteria.

For requirements about skill level, see Skill level required below.

</td></tr><tr><td>

**Skill level**

</td><td>

Dropdown

</td><td>

None

</td><td>

No

</td><td>

The minimum level or proficiency at which an agent must possess the skill. Choices depend on how skill levels are configured in your system.

For example: Beginner, Intermediate, Advanced, or Level 1–5.

Select a skill level only if you want to enforce a specific proficiency requirement.

When left empty, any technician with the skill at any level meets the requirement.

Example: For electrical repair tasks, you might require Skill = "Electrical Repair" at Skill level = "Level 3" to ensure only qualified technicians are assigned.

</td></tr><tr><td>

**Skill level required**

</td><td>

Checkbox

</td><td>

Unchecked

</td><td>

No

</td><td>

Indicates whether the skill level specified above is mandatory for assignment. When checked, technicians must have both the skill and the specified skill level to be assigned.

When unchecked, technicians must have the skill, but the level is optional. Technicians with the skill at any level, including higher levels, may be assigned. **Note:** This field is only honored by Schedule Optimization.

</td></tr></tbody>
</table>## User Skills Record

Table name: sys\_user\_has\_skill

The User Skills record defines the skills assigned to an individual technician, including proficiency level and validity dates. Use this record to track when technicians acquire and lose skill qualifications.

<table id="table_lbq_vwb_jkc"><thead><tr><th>

Field

</th><th>

Type

</th><th>

Default

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Skill**

</td><td>

Reference

</td><td>

None

</td><td>

Yes

</td><td>

The specific skill or qualification assigned to the user. Select from the list of available skills configured in your system.

</td></tr><tr><td>

**Skill level**

</td><td>

Dropdown

</td><td>

None

</td><td>

No

</td><td>

The level or proficiency at which the user possesses the skill. Choices depend on how skill levels are configured in your system.

For example: Beginner, Intermediate, Advanced, or Level 1–5.

</td></tr><tr><td>

**Active**

</td><td>

Checkbox

</td><td>

Checked

</td><td>

No

</td><td>

Indicates whether this skill assignment is currently active for the user. When unchecked, the skill is inactive and the user is not considered to have this skill for assignment purposes.

</td></tr><tr><td>

**Inherited from**

</td><td>

Reference

</td><td>

None

</td><td>

No

</td><td>

The group from which this skill is inherited, when applicable. If this field is empty, the skill was assigned directly to the user rather than inherited from a group membership.

This is a read-only reference field.

</td></tr><tr><td>

**Skill level inherited**

</td><td>

Checkbox

</td><td>

Unchecked

</td><td>

No

</td><td>

Indicates whether the skill level is inherited from the group-level skill assignment. When checked, the user's skill level matches the group's skill level.

When unchecked, the user has a custom skill level that differs from their group assignment.

This is a read-only field.

</td></tr><tr><td>

**Skill acquisition date**

</td><td>

Date

</td><td>

None

</td><td>

No

</td><td>

The date when the user acquired or obtained this skill or certification. Use this field to track when a skill was first assigned or certified.

Example: If a technician completes electrical certification training on 03/15/2024, set the acquisition date to 03/15/2024.

**Note:** This field is only honored by Schedule Optimization.

User-level dates override group-level dates.

</td></tr><tr><td>

**Skill expiration date**

</td><td>

Date

</td><td>

None

</td><td>

No

</td><td>

The date when the skill expires or is set to invalid for the user. After this date, the user no longer qualifies for tasks requiring this skill.

Schedule Optimization will not assign this user to tasks with this skill if the expiration date has passed.

Use this field for skills or certifications that require periodic renewal.

Example: When electrical certification is valid for 2 years from 03/15/2024, set the expiration date to 03/14/2026.

When the expiration date is null, the skill is considered valid indefinitely. You can also set an acquisition date with no expiration date for skills that don't expire.

**Note:** This field is only honored by Schedule Optimization.

User-level dates override group-level dates.

</td></tr></tbody>
</table>## Group Skills Record

Table name: sys\_group\_has\_skill

The Group Skills record defines skills assigned to a group of technicians. All members of the group inherit the skills and their validity dates unless they have individual user-level overrides.

<table id="table_nxz_ywb_jkc"><thead><tr><th>

Field

</th><th>

Type

</th><th>

Default

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Skill**

</td><td>

Reference

</td><td>

None

</td><td>

Yes

</td><td>

The specific skill or qualification assigned to the group. All members of the group inherit this skill unless they have a user-level override.

Select from the list of available skills created in your system.

</td></tr><tr><td>

**Inherits**

</td><td>

Checkbox

</td><td>

Checked

</td><td>

No

</td><td>

Indicates whether members of this group automatically inherit this skill assignment. When checked, all active members of the group are considered to have this skill.

When unchecked, the skill is assigned to the group record but not inherited by individual members.

</td></tr><tr><td>

**Skill acquisition date**

</td><td>

Date

</td><td>

None

</td><td>

No

</td><td>

The date when group members acquire or obtain this skill or certification. This date applies to all group members unless they have a user-level override.

Use this field to establish a standard acquisition date for all technicians in the group, for example, when the group completes group-level training.

Example: If all technicians in the "NorCal Technicians" group complete HVAC certification training on 01/10/2024, set the expiration date to 01/10/2024.

</td></tr><tr><td>

**Skill expiration date**

</td><td>

Date

</td><td>

None

</td><td>

No

</td><td>

The date when the skill expires or becomes invalid for all group members. After this date, group members no longer qualify for tasks requiring this skill unless they have a user-level override with a different expiration date.

Use this field for skills or certifications that require periodic renewal at the group level.

Example: If all technicians in the "NorCal Technicians" group have HVAC certification valid for 3 years from 01/10/2024, set the expiration date to 01/09/2027.

**Note:** User-level dates override group-level dates.

</td></tr><tr><td>

**Created**

</td><td>

Date/Time

</td><td>

System timestamp

</td><td>

No

</td><td>

The date and time when this group skill assignment was created. This is a system-generated read-only field that provides an audit trail of when the skill was added to the group.

</td></tr></tbody>
</table>## User Skill History Record

Table name: sys\_user\_skill\_history

The User Skill History record maintains a complete historical audit trail of skill assignments and modifications for each user. Each time a skill is added to a user or skill dates are changed, an entry is created in this table to track the change.

<table id="table_qcj_cxb_jkc"><thead><tr><th>

Field

</th><th>

Type

</th><th>

Default

</th><th>

Required

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Skill**

</td><td>

Reference

</td><td>

None

</td><td>

Yes

</td><td>

The skill or qualification for which this history entry is being tracked.

</td></tr><tr><td>

**Description**

</td><td>

Text

</td><td>

None

</td><td>

No

</td><td>

The description of the skill being tracked in this history entry. This field provides context about what the skill is and its purpose.

</td></tr><tr><td>

**User**

</td><td>

Reference

</td><td>

None

</td><td>

Yes

</td><td>

The technician or user associated with this skill history entry.

</td></tr><tr><td>

**Level From**

</td><td>

Text

</td><td>

None

</td><td>

No

</td><td>

The previous or starting skill level before this change. If this is the initial skill assignment, this field may be empty or show "\(empty\)".

Use this field to track skill level progression or demotion over time.

</td></tr><tr><td>

**Level To**

</td><td>

Text

</td><td>

None

</td><td>

No

</td><td>

The new or ending skill level after this change. This field captures what the skill level was set to in this history entry.

Common values include skill level names \(for example: Default, Level 1, Level 2, Intermediate, Advanced\) or may show "\(empty\)" if no skill level is configured.

</td></tr><tr><td>

**Skill acquisition date**

</td><td>

Date

</td><td>

None

</td><td>

No

</td><td>

The start date recorded for the user's skill at the time this history entry was created. If the acquisition date was modified, this field captures the value that was set.

Review this field to verify when skills were originally assigned or certified.

</td></tr><tr><td>

**Skill expiration date**

</td><td>

Date

</td><td>

None

</td><td>

No

</td><td>

The expiration date recorded for the user's skill at the time this history entry was created.If the expiration date was modified or updated, this field captures the value that was set.

Use this field to track skill certification renewals and identify when a technician's skill qualifications changed.

For retrospective analysis, view historical expiration dates to understand skill validity gaps and track recertification patterns.

</td></tr></tbody>
</table>## Cross-References

For configuration guidance on mandatory skills, see [Configuring mandatory skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/workforce-optimization-for-field-service/configure-mandatory-skills-feature.md).

For task procedures, see [Create a work order task](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/work-order-management/t_CreateAWorkOrderTask.md).

For management workflows, see [Manage Field Service and Customer Service skills](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/workforce-optimization-for-field-service/field-service-manager-agent-skills.md).

**Parent Topic:**[Field Service Management reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/field-service-management/fsm-reference.md)

