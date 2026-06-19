---
title: OSCAL SSP fields mapping
description: CAM exports authorization package and control data to OSCAL System Security Plan \(SSP\) format using the following field mappings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-ssp-fields-mapping.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: reference
last_updated: "2026-06-12"
reading_time_minutes: 3
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# OSCAL SSP fields mapping

CAM exports authorization package and control data to OSCAL System Security Plan \(SSP\) format using the following field mappings.

## Metadata

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`uuid`|Authorization package UUID|Unique identifier of the authorization package|
|`metadata.title`|Authorization package name|Name of the authorization package|
|`metadata.version`|Package version|Version of the authorization package|
|`metadata.last-modified`|Last modified date|Date the SSP was last modified|
|`metadata.oscal-version`|OSCAL version|Version of the OSCAL standard used|

## User and role mapping

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`metadata.roles[].id`|Role ID|System identifier of the role \(for example, system-owner, ISSO\)|
|`metadata.roles[].title`|Role name|Display name of the role|
|`metadata.parties[].name`|User name|Name of the user associated with the package|
|`metadata.parties[].uuid`|User UUID|Unique identifier of the user|
|`metadata.responsible-parties[].role-id`|Role assignment|Role assigned to a party in the package|
|`metadata.responsible-parties[].party-uuids[]`|Assigned user|UUID of the user assigned to the role|

## Profile reference

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`import-profile.href`|Baseline profile|Reference to the profile \(baseline\) linked to the package|

## Authorization boundary

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`system-characteristics.system-name`|Authorization boundary name|Name of the authorization boundary|
|`system-characteristics.system-name-short`|Authorization boundary short name|Short name of the authorization boundary|
|`system-characteristics.system-ids[].id`|Authorization package number|ServiceNow record number of the package \(for example, AP0010030\)|
|`system-characteristics.description`|Authorization boundary description|Description of the authorization boundary|
|`system-characteristics.status.state`|Authorization boundary status|Current status of the boundary \(for example, under-development\)|
|`system-characteristics.authorization-boundary.description`|Authorization boundary description|Description of the system boundary|
|`system-characteristics.authorization-boundary.props[@name=mission-critical]`|Mission critical|Indicates whether the system is mission-critical|

## Security impact

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`system-characteristics.security-sensitivity-level`|Security sensitivity level|Overall sensitivity level \(for example, fips-199-HIGH\)|
|`system-characteristics.security-impact-level.security-objective-confidentiality`|Confidentiality impact|Confidentiality impact level|
|`system-characteristics.security-impact-level.security-objective-integrity`|Integrity impact|Integrity impact level|
|`system-characteristics.security-impact-level.security-objective-availability`|Availability impact|Availability impact level|

## Package properties

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`system-characteristics.props[@name=skip-attestations]`|Skip attestations|Indicates whether attestations are skipped for all controls|
|`system-characteristics.props[@name=active]`|Active|Indicates whether the authorization package is active|
|`system-characteristics.props[@name=version]`|Revision|Revision version of the package|
|`system-characteristics.props[@name=privacy-sensitive-system]`|Privacy sensitive system|Indicates whether the system is privacy sensitive|
|`system-characteristics.props[@name=impact-change-justification]`|Impact change justification|Justification provided when the recommended impact is changed|
|`system-characteristics.props[@name=percentage-of-controls-implemented]`|Percentage of controls implemented|Percentage of controls implemented in the package|
|`system-characteristics.props[@name=number-of-vulnerable-items]`|Number of vulnerable items|Count of vulnerable items associated with the package|
|`system-characteristics.props[@name=number-of-security-incidents]`|Number of security incidents|Count of security incidents associated with the package|

## System components

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`system-implementation.components[].title`|Authorization boundary name|Name of the system component|
|`system-implementation.components[].description`|Authorization boundary description|Description of the system component|
|`system-implementation.components[].type`|Component type|Type of the component \(for example, this-system\)|
|`system-implementation.components[].status.state`|Component status|Current status of the component|

## Controls

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`control-implementation.implemented-requirements[].control-id`|Control ID|Identifier of the implemented control|
|`control-implementation.implemented-requirements[].uuid`|Control UUID|Unique identifier of the implemented control record|
|`control-implementation.implemented-requirements[].props[@name=status]`|Compliance status|Compliance status of the control \(for example, Not Applicable, Compliant\)|
|`control-implementation.implemented-requirements[].props[@name=state]`|Control state|Workflow state of the control \(for example, Draft, Review\)|
|`control-implementation.implemented-requirements[].props[@name=owner]`|Control owner|UUID of the user who owns the control|
|`control-implementation.implemented-requirements[].props[@name=respondents]`|Respondents|UUID of users assigned as respondents for the control|
|`control-implementation.implemented-requirements[].props[@name=frequency]`|Assessment frequency|Frequency at which the control is assessed \(for example, Annually\)|
|`control-implementation.implemented-requirements[].props[@name=attestation]`|Attestation|Reference to the attestation record for the control|
|`control-implementation.implemented-requirements[].props[@name=discussion]`|Discussion|Discussion notes for the control|
|`control-implementation.implemented-requirements[].props[@name=weighting]`|Weighting|Weighting assigned to the control|
|`control-implementation.implemented-requirements[].props[@name=sync_with_entity_owner]`|Sync with entity owner|Indicates whether the control owner is synced with the entity owner|
|`control-implementation.implemented-requirements[].props[@name=requirement_level_attestation]`|Requirement level attestation|Indicates whether attestation is at the requirement level|
|`control-implementation.implemented-requirements[].responsible-roles[].role-id`|Control role|Role assigned at the control level \(for example, owner, control-respondents\)|
|`control-implementation.implemented-requirements[].responsible-roles[].party-uuids[]`|Assigned user|UUID of the user assigned to the control role|

## Control requirements

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`control-implementation.implemented-requirements[].statements[].props[@name=state]`|Control requirement state|Workflow state of the control requirement|
|`control-implementation.implemented-requirements[].statements[].props[@name=description]`|Control requirement description|Description of the control requirement|
|`control-implementation.implemented-requirements[].statements[].props[@name=requirement_number]`|Requirement number|Number of the control requirement|
|`control-implementation.implemented-requirements[].statements[].props[@name=respondents]`|Requirement respondents|UUID of users assigned as respondents for the requirement|

## Back matter

|OSCAL SSP field|CAM field|Description|
|---------------|---------|-----------|
|`back-matter.resources[].rlinks[].href`|Profile reference|Path to the linked profile JSON file|

**Parent Topic:**[CAM OSCAL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-cam-ws.md)

