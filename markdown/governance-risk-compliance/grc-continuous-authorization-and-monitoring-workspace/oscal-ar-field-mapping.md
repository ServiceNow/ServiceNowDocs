---
title: OSCAL Assessment Results field mapping
description: CAM exports engagement and control test result data to the OSCAL Assessment Results \(AR\) format using the following field mappings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-ar-field-mapping.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# OSCAL Assessment Results field mapping

CAM exports engagement and control test result data to the OSCAL Assessment Results \(AR\) format using the following field mappings.

## Metadata

The `metadata` section exports the roles, parties, and responsible parties associated with the engagement and POA&amp;M.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`last-modified`|Last modified timestamp of the engagement|
|`roles[].id`|Role ID. Exported values include: `engagement_lead`, `approvers`, `auditors`, `control_test_owner`, `poam-owner`, `poam-manager`, `poam-manager-group`, `watchlist``poam-owner``poam-manager``poam-manager-group`|
|`roles[].title`|Display title of the role \(for example, Engagement Lead, Control Test Owner, POAM Owner\)|
|`parties[].uuid`|UUID of the user or group|
|`parties[].name`|Name of the user or group|
|`parties[].type`|Party type: `person` or `organization`|
|`responsible-parties[].role-id`|Role ID assigned to a party \(for example, engagement\_lead, poam-owner\)|
|`name="actual_cost"`|Engagement actual/work cost name|
|`name="report_template"`|Engagement report template|
|`responsible-parties[].party-uuids[]`|UUID of the user or group assigned to the role|

## Import AP

The `import-ap` field links the AR to the Assessment Plan \(AP\) from which it was generated.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`import-ap.href`|UUID of the Assessment Plan linked to this Assessment Results file|

## Activities

The `activities` array contains one object per control test. Each object exports control test details, related controls, and assessment procedures.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`uuid`|Control test UUID|
|`title`|Control test short description|
|`description`|Control test description|
|`responsible-roles[].role-id`|Role of the control test owner \(`control_test_owner`\)|
|`responsible-roles[].party-uuids[]`|UUID of the user assigned to the control test \(Assigned to\)|
|`related-controls.control-selections[].include-controls[].control-id`|ID of the control linked to the control test|
|`related-controls.control-selections[].include-controls[].statement-ids[]`|Control requirement IDs linked to the control test|
|`related-controls.control-selections[].name="entity"`|Entity linked to the control test|
|`related-controls.control-objective-selections[].include-objectives[].objective-id`|Control objective ID linked to the control test|
|`steps[].uuid`|Assessment procedure UUID|
|`steps[].description`|Assessment procedure description|
|`steps[].name="label"`|Assessment procedure identifier \(label\)|
|`name="state"`|Control test state \(for example, Closed Complete\)|
|`name="operation_effectiveness"`|Operating effectiveness of the control test|
|`name="operation_assessment_procedures"`|Assessment procedures description|
|`name="test_plan_uuid"`|UUID of the test plan linked to the control test|
|`name="interview"`|Interview sources for the control test|
|`name="examine"`|Examine sources for the control test|
|`name="test"`|Test sources for the control test|
|`name="method"`|Assessment method \(for example, TEST\)|
|`name="planned_start_date"`|Planned start date of the control test|
|`name="planned_end_date"`|Planned end date of the control test|
|`name="actual_start_date"`|Actual start date of the control test|
|`name="actual_end_date"`|Actual end date of the control test|

## Results — engagement properties

The `results[].props` array exports engagement-level fields that are captured during the assessment lifecycle.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`name="state"`|Engagement state|
|`name="short_description"`|Engagement short description|
|`name="entity"`|Entity linked to the engagement|
|`name="engagement_starts"`|Engagement start step \(for example, Fieldwork\)|
|`name="engagement_ends"`|Engagement end step \(for example, Closed\)|
|`name="schedule_start_date"`|Scheduled start date|
|`name="schedule_end_date"`|Scheduled end date|
|`name="fieldwork_start_date"`|Fieldwork start date|
|`name="fieldwork_end_date"`|Fieldwork end date|
|`name="planned_start_date"`|Planned start date|
|`name="budget_cost"`|Budget cost|
|`name="planned_cost"`|Planned cost|
|`name="percent_complete"`|Percent complete|
|`name="fieldwork_complete_percentage"`|Fieldwork complete percentage|
|`name="active"`|Whether the engagement is active|

## Results — Reviewed controls

The `results[].reviewed-controls` object exports the controls and control objectives linked to the engagement.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`control-selections[].name="entity"`|Entity linked to the control selection|
|`control-selections[].include-controls[].control-id`|Control ID|
|`control-selections[].include-controls[].statement-ids[]`|Control requirement IDs|
|`control-objective-selections[].include-objectives[].objective-id`|Control objective ID|

## Results — Findings

The `results[].findings` array exports POA&amp;M items, milestones, and acceptance tasks linked to control tests in the engagement.

**POA&amp;M items**

Each finding object represents one POA&amp;M item.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`uuid`|POA&amp;M item UUID|
|`title`|POA&amp;M item title|
|`description`|POA&amp;M item description|
|`target.target-id`|ID of the control objective that the finding targets|
|`target.type`|Target type \(`objective-id`\)|
|`target.name="target-uuid"`|UUID of the control test linked to the POA&amp;M item|
|`status.state`|Finding status \(for example, `not-satisfied`\)|
|`name="state"`|POA&amp;M item state \(for example, Respond\)|
|`name="priority"`|POA&amp;M item priority \(for example, 4 – Low\)|
|`name="response"`|POA&amp;M response \(for example, Remediate, Accept\)|
|`name="explanation"`|POA&amp;M explanation|
|`name="issue_type"`|Issue type \(for example, Control design effectiveness failure\)|

**Milestones**

Milestone fields are exported as props within the finding object associated with the POA&amp;M item.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`name="state"`|Milestone state|
|`name="priority"`|Milestone priority|
|`name="short_description"`|Milestone short description|
|`name="description"`|Milestone description|
|`name="parent"`|Parent POA&amp;M item|
|`name="assigned_to"`|User assigned to the milestone|
|`name="watch_list"`|Watch list for the milestone|
|`name="planned_start_date"`|Planned start date|
|`name="planned_end_date"`|Planned end date|
|`name="actual_start_date"`|Actual start date|
|`name="actual_end_date"`|Actual end date|

**Acceptance tasks**

Acceptance task fields are exported as props within the finding object associated with the POA&amp;M item. Acceptance tasks export all milestone fields plus the following additional fields.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`name="weakness_description"`|Weakness description|
|`name="effect_on_business"`|Effect on business|
|`name="risk_acceptance_request"`|Risk acceptance request|
|`name="business_justification"`|Business justification|
|`name="justification_for_request"`|Justification for request|

## Results — Attestations

The `results[].attestations` array exports control test effectiveness data. Each object in `parts` represents one control test, and the nested `parts` within it represent the assessment procedures of that control test.

|OSCAL AR field|ServiceNow CAM field|
|--------------|--------------------|
|`responsible-parties[].role-id`|Role of the control test owner \(`control_test_owner`\)|
|`responsible-parties[].party-uuids[]`|UUID of the control test owner|
|`parts[].uuid`|Control test UUID|
|`parts[].title`|Control test short description|
|`parts[].class`|Object class \(`control-test`\)|
|`parts[].name`|Part name \(`objective`\)|
|`parts[].prose`|Control effectiveness value \(for example, `ineffective`\)|
|`parts[].name="operation_effectiveness"`|Operating effectiveness of the control test|
|`parts[].name="operation_assessment_procedures"`|Assessment procedures description|
|`parts[].name="planned_start_date"`|Planned start date of the control test|
|`parts[].name="planned_end_date"`|Planned end date of the control test|
|`parts[].name="actual_start_date"`|Actual start date of the control test|
|`parts[].name="actual_end_date"`|Actual end date of the control test|
|`parts[].name="method"`|Assessment method|
|`parts[].parts[].uuid`|Assessment procedure UUID|
|`parts[].parts[].title`|Assessment procedure description|
|`parts[].parts[].class`|Object class \(`assessment-procedure`\)|
|`parts[].parts[].name`|Part name \(`objective`\)|
|`parts[].parts[].prose`|Assessment procedure effectiveness value \(for example, `ineffective`\)|
|`parts[].parts[].name="label"`|Assessment procedure identifier \(label\)|
|`parts[].parts[].name="method"`|Assessment method for the assessment procedure|

**Parent Topic:**[CAM OSCAL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-cam-ws.md)

