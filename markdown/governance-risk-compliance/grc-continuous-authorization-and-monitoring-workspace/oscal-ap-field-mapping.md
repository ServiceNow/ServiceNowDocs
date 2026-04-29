---
title: OSCAL Assessment Plan field mapping
description: CAM exports engagement and control test data to OSCAL Assessment Plan format using the following field mappings.
locale: en-US
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [OSCAL Assessment Plan export and import, CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# OSCAL Assessment Plan field mapping

CAM exports engagement and control test data to OSCAL Assessment Plan format using the following field mappings.

## Engagement metadata mapping

The OSCAL Assessment Plan metadata section contains engagement-level information exported from the CAM engagement record.

<table><thead><tr><th>

OSCAL AP field

</th><th>

CAM field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

assessment\_plan.uuid

</td><td>

sn\_audit\_engagement.sys\_id

</td><td>

Unique identifier for the engagement

</td></tr><tr><td>

assessment\_plan.metadata.title

</td><td>

sn\_audit\_engagement.name

</td><td>

Engagement name

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=state\]

</td><td>

sn\_audit\_engagement.state.displayValue

</td><td>

Current engagement state \(Open, Work in Progress, Closed, Complete\)

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=fieldwork\_complete\_percentage\]

</td><td>

sn\_audit\_engagement.task\_percent\_complete

</td><td>

Percentage of testing tasks completed

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=objective\]

</td><td>

sn\_audit\_engagement.objectives

</td><td>

Testing objectives for this engagement

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=planned\_end\_date\]

</td><td>

sn\_audit\_engagement.audit\_period\_end

</td><td>

Planned audit end date

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=planned\_start\_date\]

</td><td>

sn\_audit\_engagement.audit\_period\_start

</td><td>

Planned audit start date

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=engagement\_starts\]

</td><td>

sn\_audit\_engagement.engagement\_starts

</td><td>

When the engagement officially begins

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=engagement\_ends\]

</td><td>

sn\_audit\_engagement.engagement\_ends

</td><td>

When the engagement officially ends

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=fieldwork\_start\_date\]

</td><td>

sn\_audit\_engagement.start\_date

</td><td>

When actual testing work begins

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=fieldwork\_end\_date\]

</td><td>

sn\_audit\_engagement.end\_date

</td><td>

When actual testing work ends

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=budget\_cost\]

</td><td>

sn\_audit\_engagement.budget\_cost

</td><td>

Approved budget amount for the engagement

</td></tr><tr><td>

assessment\_plan.metadata.props\[@name=planned\_cost\]

</td><td>

sn\_audit\_engagement.cost

</td><td>

Planned cost for the engagement

</td></tr></tbody>
</table>## User and role mapping

The OSCAL metadata.parties section contains user information, and metadata.roles defines available roles. Responsible parties link users to their roles.

|OSCAL AP Field|CAM Field|Description|
|--------------|---------|-----------|
|assessment\_plan.metadata.parties.uuid|sys\_user.sys\_id|ServiceNow user unique identifier|
|assessment\_plan.metadata.parties.type|person \(default for individual users\)|Party type: person for individual users, organization for groups|
|assessment\_plan.metadata.parties.name|sys\_user.first\_name + ' ' + sys\_user.last\_name|User's full name|

Exported roles include: engagement lead, approvers, auditors, and control test owner \(mapped from control test assigned to field\).

## Control test mapping \(activities\)

The OSCAL local-definitions.activities section contains control test information. Each activity represents one control test in CAM.

|OSCAL AP Field|CAM Field|Description|
|--------------|---------|-----------|
|assessment\_plan.local-definitions.activities.uuid|sn\_audit\_control\_test.sys\_id|Unique identifier for the control test|
|assessment\_plan.local-definitions.activities.title|sn\_audit\_control\_test.short\_description|Brief title of the control test|
|assessment\_plan.local-definitions.activities.description|sn\_audit\_control\_test.description|Detailed description of what will be tested|
|assessment\_plan.local-definitions.activities.props\[@name=state\]|sn\_audit\_control\_test.state.getDisplayValue|Current test status \(Not tested, In progress, Complete\)|
|assessment\_plan.local-definitions.activities.props\[@name=operational-assessment-procedures\]|sn\_audit\_control\_test.operation\_assessment\_procedures|Operational assessment procedures for this control test|
|assessment\_plan.local-definitions.activities.related-controls.control-selections.include-controls.control-id|sn\_audit\_control\_test.control|Control being tested \(foe example, AC-2, AU-3\)|
|assessment\_plan.local-definitions.activities.related-controls.control-objective-selections.include-objectives.objective-id|sn\_audit\_control\_test.test\_plan|Test plan associated with this control test|

## Assessment procedure mapping \(steps\)

The OSCAL activities.steps section contains assessment procedure information. Each step represents one assessment procedure in CAM.

|OSCAL AP Field|CAM Field|Description|
|--------------|---------|-----------|
|assessment\_plan.local-definitions.activities.steps.uuid|sn\_audit\_asmnt\_procedure\_control\_test.sys\_id|Unique identifier for the assessment procedure|
|assessment\_plan.local-definitions.activities.steps.description|sn\_audit\_asmnt\_procedure\_control\_test.assessment\_objective|What this test step assesses or verifies|
|assessment\_plan.local-definitions.activities.steps.props\[@name=label\]|sn\_audit\_asmnt\_procedure\_control\_test.identifier|Step identifier \(for example, AC-2\(a\), AC-2\(b\)\)|

## Reviewed controls mapping

The OSCAL reviewed-controls section identifies which controls are in scope for the assessment engagement.

|OSCAL AP Field|CAM Field|Description|
|--------------|---------|-----------|
|assessment\_plan.reviewed-controls.control-selections.include-controls.control-id|sn\_audit\_m2m\_control\_engagement.sn\_compliance\_control.reference|Control reference included in this engagement \(e.g., AC-2, AU-3\)|
|assessment\_plan.reviewed-controls.control-selections.include-controls.statement-ids|sn\_audit\_m2m\_control\_engagement.sn\_compliance\_control.sn\_compliance\_m2m\_control\_control\_requirement.control\_requirement|Specific control requirements being tested \(e.g., AC-2\(a\), AC-2\(b\)\)|

## SSP reference mapping

The OSCAL import-ssp section links the Assessment Plan to its parent System Security Plan.

|OSCAL AP Field|CAM Field|Description|
|--------------|---------|-----------|
|assessment\_plan.import-ssp.href|Package UUID \(links to parent authorization package\)|UUID reference linking this assessment plan to the package it tests|

The href uses the package UUID. If the package was imported, it uses the UUID from the external system. If the package was created in CAM, the system converts the sys\_id to UUID format.

## Custom properties

Custom properties contain CAM-specific data not natively supported by OSCAL standards. These properties use the ServiceNow namespace \(identified by "ns:servicenow" in the JSON\). Custom properties include engagement-specific fields such as fieldwork dates, budget information, and control test methods. Documentation of all custom properties is available on the ServiceNow product documentation site.

**Parent Topic:**[OSCAL Assessment Plan export and import](oscal-assessment-plan-import-export.md)

