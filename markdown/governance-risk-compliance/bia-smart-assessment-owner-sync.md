---
title: BIA owner field reference and validation rules
description: Detailed field definitions, validation rules, filtering logic, and technical specifications for group ownership in Business Impact Analysis \(BIA\) records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/bia-smart-assessment-owner-sync.html
release: zurich
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [BIA, business impact analysis, owner sync, field reference]
breadcrumb: [Group owner fields and role requirements, Reference, Business Continuity Management, Governance, Risk, and Compliance]
---

# BIA owner field reference and validation rules

Detailed field definitions, validation rules, filtering logic, and technical specifications for group ownership in Business Impact Analysis \(BIA\) records.

## BIA field mapping and definitions

Business Impact Analysis \(BIA\) records include a group field that identifies the team responsible for the record. They also include an individual field that identifies a specific person accountable for the record.

|Property|Value|
|--------|-----|
|Record type|Business Impact Analysis \(BIA\)|
|Table name|\[sn\_bcp\_impact\_analysis\]|
|Group field name|BIA Owner group|
|Individual field name|BIA Owner|

## BIA owner group field details

The **BIA Owner group** field identifies the team responsible for the BIA record.

|Property|Description|
|--------|-----------|
|Field type|Reference \(group table\)|
|Mandatory|No \(but at least one of group or individual field must be populated\)|
|Default value|Empty \(not auto-populated on record creation\)|
|Visibility|Visible in both Classic UI \(UI16\) and Business Continuity Workspace \(UI Builder\)|
|Filtering|Limited to groups holding BIA Planner or BIA Manager role \(role-based filtering\)|

## BIA owner field details

The **BIA Owner** field identifies a specific person accountable for the BIA record.

|Property|Description|
|--------|-----------|
|Field type|Reference \(user table\)|
|Mandatory|No \(but at least one of group or individual field must be populated\)|
|Default value|Current user \(pre-populated on record creation\)|
|Visibility|Visible in both Classic UI \(UI16\) and Business Continuity Workspace \(UI Builder\)|
|Filtering Behavior|When group is selected: Filters to members of the selected group. When group is not selected: Shows all users \(no filtering\); matches legacy behavior. When individual is selected before group: Allows selection of any user; if a group is later selected and the individual is not a member, the system allows the selection and displays an informational message.|

## Mandatory validation rules

Group ownership implements a special mandatory validation rule: at least one of the two fields \(**BIA Owner group** or **BIA Owner**\) must be populated.

|Validation State|Behavior|
|----------------|--------|
|**BIA Owner group** populated, **BIA Owner** empty|Valid — record can be saved|
|**BIA Owner** populated, **BIA Owner group** empty|Valid — record can be saved \(legacy behavior\)|
|Both fields populated|Valid — record can be saved|
|Both fields empty|Invalid — both fields highlighted in red with asterisk; mandatory error displayed; user must populate at least one field|

## Reference qualifiers

<table><thead><tr><th>

Qualifier

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**BIA Owner group** field qualifier \(filterBIAOwnerGroup\)

</td><td>

The **BIA Owner group** field reference qualifier filters candidate groups based on role eligibility. Only groups holding the BIA Planner \(sn\_bia.bia\_planner\) or BIA Manager \(sn\_bia.bia\_manager\) role are displayed. Any group without the required role is not shown in the selectable list.

</td></tr><tr><td>

**BIA Owner** field qualifier \(filterBIAOwner\)

</td><td>

The **BIA Owner** field reference qualifier adjusts dynamically based on whether a group is selected. -   When a group is selected, reference qualifier filters the user list to members of the selected group only. This verifies the selected owner is part of the assigned team.
-   When no group is selected, reference qualifier displays all users without filtering. This matches the original behavior and maintains backward compatibility.
-   If a user is selected and then a group is chosen that does not include that user, the system allows the selection and displays an informational message: "Allow selection outside the group."

</td></tr></tbody>
</table>## Implementation details

|Component|Description|
|---------|-----------|
|onChange: **BIA Owner group** field|When the group field value changes, this script re-filters the **BIA Owner** field reference qualifier to show only members of the newly selected group. If an individual was previously selected and is not a member of the new group, the system checks and displays an informational message.|
|onChange: **BIA Owner** field|When the individual field value changes, this script checks group membership via a GlideAjax helper. If the selected individual is not a member of the currently selected group, an informational message is displayed: "Allow selection outside the group." The selection is not blocked.|
|onLoad Script: Default Value Logic|When a new BIA record is created, the onLoad script pre-populates the **BIA Owner** field with the current user. The **BIA Owner group** field is left empty. This default behavior verifies backward compatibility and allows existing workflows to function unchanged.|
|UI Policy \#1: Verify at least one validation|On form submission, if both the **BIA Owner group** and **BIA Owner** fields are empty, both fields are marked as mandatory \(red outline, asterisk\). A validation error is displayed.|
|UI Policy \#2: Display guidance banner|An informational banner is displayed whenever the group or individual field pair is present: `Select either a group or an individual to save the record and proceed with the workflow.` This guides users to complete the required fields successfully.|

## Backward compatibility and legacy behavior

|Scenario|Behavior|
|--------|--------|
|Existing BIA records with individual owner only|Continue to function unchanged. The **BIA Owner group** field is optional; no changes are required for records with only an individual owner.|
|Unfiltered user selection when no group is selected|When the **BIA Owner group** field is empty, the **BIA Owner** field shows all users without filtering. This verifies workflows and automation that reference the individual owner field are unaffected.|

**Parent Topic:**[Group owner fields and role requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/owner-group-eligibility-roles.md)

