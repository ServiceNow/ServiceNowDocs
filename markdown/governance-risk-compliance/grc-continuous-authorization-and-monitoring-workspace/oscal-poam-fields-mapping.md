---
title: OSCAL POAM fields mapping
description: CAM exports POA&amp;M item data to OSCAL Plan of Action and Milestones \(POA&amp;M\) format using the following field mappings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-poam-fields-mapping.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: reference
last_updated: "2026-06-12"
reading_time_minutes: 3
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# OSCAL POAM fields mapping

CAM exports POA&amp;M item data to OSCAL Plan of Action and Milestones \(POA&amp;M\) format using the following field mappings.

## Metadata

|OSCAL POA&amp;M field|CAM field|Description|
|---------------------|---------|-----------|
|`uuid`|POA&amp;M UUID|Unique identifier of the POA&amp;M record|
|`metadata.title`|POA&amp;M name|Name of the POA&amp;M record|
|`metadata.version`|Version|Version of the POA&amp;M|
|`metadata.oscal-version`|OSCAL version|Version of the OSCAL standard used|
|`metadata.last-modified`|Last modified date|Date the POA&amp;M was last modified|
|`metadata.published`|Published date|Date the POA&amp;M was published|

## User and role mapping

|OSCAL POA&amp;M field|CAM field|Description|
|---------------------|---------|-----------|
|`metadata.roles[].id`|Role ID|System identifier of the role \(for example, poam-owner, poam-manager, watchlist, task-owner\)|
|`metadata.roles[].title`|Role name|Display name of the role|
|`metadata.parties[].uuid`|User or group UUID|Unique identifier of the user or group|
|`metadata.parties[].name`|User or group name|Name of the user or group|
|`metadata.parties[].type`|Party type|Type of the party: person for individual users, organization for groups|
|`metadata.responsible-parties[].role-id`|Role assignment|Role assigned to a party in the POA&amp;M|
|`metadata.responsible-parties[].party-uuids[]`|Assigned user or group|UUID of the user or group assigned to the role|

## SSP reference

|OSCAL POA&amp;M field|CAM field|Description|
|---------------------|---------|-----------|
|`import-ssp.href`|Authorization package UUID|UUID reference linking the POA&amp;M to its parent authorization package|

## POA&amp;M items

|OSCAL POA&amp;M field|CAM field|Description|
|---------------------|---------|-----------|
|`poam-items[].uuid`|POA&amp;M item UUID|Unique identifier of the POA&amp;M item|
|`poam-items[].title`|Short description|Brief title of the POA&amp;M item|
|`poam-items[].description`|Description|Detailed description of the POA&amp;M item|
|`poam-items[].props[@name=uuid]`|sys\_id|ServiceNow sys\_id of the POA&amp;M item record|
|`poam-items[].props[@name=state]`|State|Current state of the POA&amp;M item \(for example, Respond, Closed\)|
|`poam-items[].props[@name=priority]`|Priority|Priority of the POA&amp;M item \(for example, 4 – Low\)|
|`poam-items[].props[@name=response]`|Response|Response type for the POA&amp;M item \(for example, Accept, Remediate\)|
|`poam-items[].props[@name=explanation]`|Explanation|Explanation provided for the POA&amp;M item|
|`poam-items[].props[@name=issue_type]`|Issue type|Type of issue \(for example, Control design effectiveness failure\)|
|`poam-items[].props[@name=classification]`|Classification|Classification of the POA&amp;M item \(for example, Audit, Compliance\)|
|`poam-items[].props[@name=issue_rating]`|Issue rating|Risk rating of the issue \(for example, 2 – High\)|
|`poam-items[].props[@name=issue_source]`|Issue source|Source from which the issue was identified \(for example, Control Test Failure\)|
|`poam-items[].props[@name=planned_start_date]`|Planned start date|Planned start date of the POA&amp;M item|
|`poam-items[].props[@name=planned_end_date]`|Planned end date|Planned end date of the POA&amp;M item|
|`poam-items[].props[@name=actual_start_date]`|Actual start date|Actual start date of the POA&amp;M item|
|`poam-items[].props[@name=actual_end_date]`|Actual end date|Actual end date of the POA&amp;M item|
|`poam-items[].props[@name=assigned_to]`|Assigned to|UUID of the user assigned to the POA&amp;M item|
|`poam-items[].props[@name=issue_manager]`|Issue manager|UUID of the user assigned as issue manager|
|`poam-items[].props[@name=issue_manager_group]`|Issue manager group|UUID of the group assigned as issue manager group|
|`poam-items[].props[@name=watch_list]`|Watch list|UUID of users on the watch list for the POA&amp;M item|
|`poam-items[].props[@name=authorization_package]`|Authorization package|Name of the authorization package associated with the POA&amp;M item|
|`poam-items[].props[@name=control]`|Control|Control associated with the POA&amp;M item \(for example, IA-8\(2\)\)|
|`poam-items[].props[@name=control_test]`|Control test|Control test associated with the POA&amp;M item|
|`poam-items[].props[@name=engagement]`|Engagement|Engagement associated with the POA&amp;M item \(for example, ENG0020017\)|
|`poam-items[].props[@name=weakness_description]`|Weakness description|Description of the weakness identified in the POA&amp;M item|
|`poam-items[].props[@name=business_effect]`|Business effect|Effect of the weakness on the business|
|`poam-items[].props[@name=business_justification]`|Business justification|Business justification for the risk acceptance decision|
|`poam-items[].props[@name=request_justification]`|Request justification|Justification provided with the risk acceptance request|
|`poam-items[].props[@name=request_overview]`|Request overview|Overview of the risk acceptance request|
|`poam-items[].props[@name=short_description]`|Short description|Short description of the milestone or acceptance task|
|`poam-items[].props[@name=work_note]`|Work notes|Work note for a milestone or acceptance task associated with the POA&amp;M item|
|`poam-items[].props[@name=additional_comment]`|Additional comments|Additional comment for a milestone or acceptance task associated with the POA&amp;M item|
|`poam-items[].related-findings[].finding-uuid`|Finding|UUID reference to the finding associated with the POA&amp;M item|

## Findings

|OSCAL POA&amp;M field|CAM field|Description|
|---------------------|---------|-----------|
|`findings[].uuid`|Finding UUID|Unique identifier of the finding|
|`findings[].title`|Finding title|Title of the finding \(for example, Control Test Failure, Control Attestation Failure\)|
|`findings[].description`|Finding description|Description of the finding|
|`findings[].target.target-id`|Control or objective ID|Control ID or objective ID associated with the finding \(for example, IA-8.2, CA-3\)|
|`findings[].target.type`|Target type|Type of the target: objective-id for control test failures, statement-id for attestation failures|
|`findings[].target.props[@name=target-uuid]`|Control test or attestation UUID|ServiceNow UUID of the control test or attestation that produced the finding|
|`findings[].target.status.state`|Finding status|Indicates whether the control objective is satisfied or not-satisfied|

## Observations

|OSCAL POA&amp;M field|CAM field|Description|
|---------------------|---------|-----------|
|`observations[].uuid`|Observation UUID|Unique identifier of the observation|
|`observations[].description`|Observation description|Description of the observation|
|`observations[].collected`|Collected date|Date the observation was collected|
|`observations[].origins[].actors[].role-id`|Actor role|Role of the actor who made the observation \(for example, poam-owner, poam-manager\)|
|`observations[].origins[].actors[].actor-uuid`|Actor UUID|UUID of the user who made the observation|

**Parent Topic:**[CAM OSCAL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-cam-ws.md)

