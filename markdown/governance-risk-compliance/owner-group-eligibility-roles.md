---
title: Group owner fields and role requirements
description: Reference guide for group owner role eligibility requirements, field mapping, and filtering logic across all Business Continuity Management record types.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/owner-group-eligibility-roles.html
release: australia
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [business continuity management, group ownership, role requirements]
breadcrumb: [Reference, Business Continuity Management, Governance, Risk, and Compliance]
---

# Group owner fields and role requirements

Reference guide for group owner role eligibility requirements, field mapping, and filtering logic across all Business Continuity Management record types.

## Group ownership functionality

Group ownership is available across three BCM record types: Business Impact Analysis \(BIA\), Business Continuity Plan \(Plan\), and Recovery Event \(Event\). Each record type maintains its own field naming convention while sharing the same underlying logic for filtering, mandatory validation, and role-based access control.

## Field mapping by record type

The following table shows the field naming convention for each BCM record type:

|Record Type|Table Name|Group Field Name|Individual Field Name|
|-----------|----------|----------------|---------------------|
|Business Impact Analysis \(BIA\)|sn\_bcp\_impact\_analysis|BIA Owner group|BIA Owner|
|Business Continuity Plan \(Plan\)|sn\_bcp\_plan|Plan owner group|Plan owner|
|Recovery Event \(Event\)|sn\_recovery\_event|Assignment group|Assigned to|

## Role-based group filtering

The group field on each record type filters candidate groups based on role eligibility. Only groups that hold a role equivalent to the record's owner role are shown as selectable options. This confirms that groups shown in the owner field actually have the permissions needed to manage the record.

|Record Type|Groups Shown|Groups Excluded|Purpose|
|-----------|------------|---------------|-------|
|BIA records \(sn\_bcp\_impact\_analysis\)|Only groups holding the BIA Planner role OR the BIA Manager role|Any group without one of these roles is not shown in the BIA Owner group selectable list|Ensures only qualified groups can be assigned as BIA record owners|
|Plan records \(sn\_bcp\_plan\)|Only groups holding the Plan Owner role OR equivalent BCM Manager role|Any group without one of these roles is not shown in the Plan owner group selectable list|Ensures only qualified groups can be assigned as Plan record owners|
|Event records \(sn\_recovery\_event\)|Only groups with task assignment permissions \(inherited from sn\_task table role model\)|Any group without the required task assignment role is not shown in the Assignment group selectable list|Verifies only qualified groups can be assigned as Event record owners. Filter may vary based on task table configuration|

## Individual field filtering across record types

The individual field \(BIA Owner, Plan owner, or Assigned to\) adjusts its filtering behavior dynamically based on group selection across all record types.

## Record type comparison

|Aspect|BIA records|Plan records|Event records|
|------|-----------|------------|-------------|
|Group field name|BIA Owner group|Plan owner group|Assignment group|
|Individual field name|BIA Owner|Plan owner|Assigned to|
|Eligible group roles|BIA Planner OR BIA Manager|Plan Owner OR BCM Manager|Task assignment role \(from sn\_task\)|
|Default individual|Current user \(pre-populated\)|Current user \(pre-populated\)|Current user \(pre-populated\)|
|Default group|Empty|Empty|Empty|
|Classic UI section|User Administration|User Administration|Assignment details|
|Workspace section|Assignment details|Assignment details \(Details tab\)|Assignment details \(Create Event page\)|

## Mandatory validation rules

Group ownership implements a special mandatory validation rule across all three record types: at least one of the two fields \(group or individual\) must be populated.

|Validation State|Behavior|
|----------------|--------|
|Group populated, Individual empty|Valid — record can be saved|
|Individual populated, Group empty|Valid — record can be saved \(legacy behavior\)|
|Both populated|Valid — record can be saved|
|Both empty|Invalid — both fields highlighted in red with asterisk; mandatory error displayed; user must populate at least one field|

Error message on submit with both fields empty: Both fields are outlined in red with an asterisk indicator, and a validation error is displayed prompting the user to fill in either field.

Guidance banner: `Select either a group or an individual to save the record and proceed with the workflow.`

## Role permissions and access control

Role-based group filtering confirms that only groups with the appropriate permissions are eligible to own records of each type. This maintains proper separation of duties and access control across the BCM suite.

|Record Type|Required Permissions|
|-----------|--------------------|
|BIA Owner permissions|Groups assigned as BIA Owner must hold either the BIA Planner role or BIA Manager role. These roles grant permission to create, edit, and maintain BIA records within their scope.|
|Plan Owner permissions|Groups assigned as Plan Owner must hold the Plan Owner role or an equivalent BCM Manager role. These roles grant permission to create, edit, and maintain Plan records within their scope.|
|Event Assignment permissions|Groups assigned as Assignment group must hold appropriate task assignment permissions \(inherited from the \[sn\_task\] table role model\). These roles grant permission to manage and track recovery event activities.|

## Backward compatibility and legacy behavior

|Scenario|Behavior|
|--------|--------|
|Existing records with individual owner only|Continue to function unchanged. The group field is optional; no changes are required for records with only an individual owner.|
|Automation and workflows|Workflows that reference the individual owner field are unaffected by the group ownership feature unless explicitly using the group field.|
|Role-based group filtering|Enforced at the reference qualifier level, ensuring that ineligible groups are excluded from the selectable list before presentation to the user.|
|Outside group selection|The "Allow selection outside the group" informational message provides flexibility for edge cases. An individual may serve as owner even if not formally part of the owning group.|
|UI consistency|Both Classic UI and Business Continuity Workspace implement group ownership consistently, ensuring a unified user experience across UI platforms.|

-   **[BIA owner field reference and validation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bia-smart-assessment-owner-sync.md)**  
Detailed field definitions, validation rules, filtering logic, and technical specifications for group ownership in Business Impact Analysis \(BIA\) records.

**Parent Topic:**[BCM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/bcm-reference.md)

**Related topics**  


[Group ownership in BIA, plan, and event records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/group-ownership-bias.md)

