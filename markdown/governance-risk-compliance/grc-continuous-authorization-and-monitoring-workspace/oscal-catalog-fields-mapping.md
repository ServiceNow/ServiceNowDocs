---
title: Oscal Catalog fields mapping
description: CAM exports catalog and control data to OSCAL Catalog format using the following field mappings.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-catalog-fields-mapping.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: reference
last_updated: "2026-06-12"
reading_time_minutes: 1
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Oscal Catalog fields mapping

CAM exports catalog and control data to OSCAL Catalog format using the following field mappings.

## Metadata

|OSCAL Catalog field|CAM field|Description|
|-------------------|---------|-----------|
|`metadata.title`|Catalog name|Name of the NIST catalog|
|`metadata.version`|Catalog version|Version of the catalog \(for example, 5.1.1+u3\)|
|`metadata.oscal-version`|OSCAL version|Version of the OSCAL standard used|
|`metadata.last-modified`|Last modified date|Date the catalog was last modified|

## Control families

|OSCAL Catalog field|CAM field|Description|
|-------------------|---------|-----------|
|`groups[].id`|Control family ID|Identifier of the control family \(for example, PE, AC, IA\)|
|`groups[].title`|Control family name|Name of the control family|

## Controls

|OSCAL Catalog field|CAM field|Description|
|-------------------|---------|-----------|
|`groups[].controls[].id`|Control ID|Identifier of the control \(for example, PE-5, AC-2\)|
|`groups[].controls[].title`|Control name|Name of the control|
|`groups[].controls[].props[@name=impact]`|Impact|Impact levels applicable to the control \(for example, Moderate, High\)|
|`groups[].controls[].props[@name=active]`|Active|Indicates whether the control is active|
|`groups[].controls[].props[@name=auto_control_create]`|Auto control create|Indicates whether controls are automatically created from the catalog|
|`groups[].controls[].props[@name=create_control_requirements]`|Create control requirements|Indicates whether control requirements are automatically created|
|`groups[].controls[].props[@name=organizational_guidance]`|Organizational guidance|Organizational guidance associated with the control|

## Control content

|OSCAL Catalog field|CAM field|Description|
|-------------------|---------|-----------|
|`groups[].controls[].parts[@name=statement]`|Control statement|Prose description of the control requirement|
|`groups[].controls[].parts[@name=guidance]`|Supplemental guidance|Additional guidance for implementing the control|
|`groups[].controls[].parts[@name=assessment-objective]`|Assessment objective|Objectives used to assess the control|
|`groups[].controls[].parts[@name=assessment-method]`|Assessment method|Method used to assess the control \(Examine, Interview, Test\)|

## Control enhancements

|OSCAL Catalog field|CAM field|Description|
|-------------------|---------|-----------|
|`groups[].controls[].controls[].id`|Control enhancement ID|Identifier of the control enhancement \(for example, AC-2.1\)|

**Parent Topic:**[CAM OSCAL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-cam-ws.md)

