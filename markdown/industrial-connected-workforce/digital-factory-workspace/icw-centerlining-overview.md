---
title: Industrial Centerlines
description: Industrial Centerlines enables you to identify and maintain critical equipment settings by specifying baseline targets and ranges, and routinely verifying that all settings conform to the defined standard. This process reduces the risk of quality and reliability losses in manufacturing operations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/industrial-connected-workforce/digital-factory-workspace/icw-centerlining-overview.html
release: australia
product: Digital Factory Workspace
classification: digital-factory-workspace
topic_type: concept
last_updated: "2026-10-02"
reading_time_minutes: 3
breadcrumb: [Explore, Digital Factory Workspace, Industrial Connected Workforce]
---

# Industrial Centerlines

Industrial Centerlines enables you to identify and maintain critical equipment settings by specifying baseline targets and ranges, and routinely verifying that all settings conform to the defined standard. This process reduces the risk of quality and reliability losses in manufacturing operations.

## Industrial Centerlines overview

In manufacturing environments, equipment is operated with a set of configurable settings that directly affect product quality, process reliability, and safety. Industrial Centerlines verifies that these settings are documented, standardized, and routinely confirmed by operators.

You can use Industrial Centerlines for confirmation and verification of settings according to their defined standard values. This practice is called conforming base condition. When settings conform to the standard base condition, the risk of reliability or quality losses such as stops, deviations, breakdowns, and defects are reduced. When operators discover anomalies during centerline verification, the system creates deviation tasks to investigate and resolve the issues. For example, equipment settings don't conform to a standard. Using Industrial Centerlines, you can create a deviation task to investigate and execute correct equipment settings.

## Industrial Centerlines process

The Industrial Centerlines process consists of the following key activities:

-   Define settings: Identify the operator-modifiable settings for each piece of equipment and define the format for each setting's value. For example, numeric range, numeric target, choice, or text.
-   Specify standard values: Establish the acceptable values, ranges, and targets for each setting through setting specifications within a setting plan.
-   Create a centerline standard: Define a manufacturing standard that includes the settings to be confirmed and the schedule for generating confirmation tasks.
-   Execute centerline tasks: Operators confirm or update each setting's value as part of a generated centerline task. The system records the confirmed value, previous value, and compliance status.
-   Review and refine: Analyze confirmation results over time and refine targets and ranges to improve performance.

## Industrial Centerlines personas

|User|Description|
|----|-----------|
|Industrial Centerlines admin|Configures the Industrial Centerlines system, manages all Industrial Centerlines data, and has full access to all Industrial Centerlines tables.|
|Industrial Centerlines config|Creates and manage setting definitions, setting plans, and setting specifications for equipment. Can create and update records in Draft state.|
|Industrial Centerlines standard author|Creates and manages Industrial Centerlines manufacturing standards, including selecting which settings to include and defining the task schedule.|
|Industrial Centerlines expert|Advanced access for Industrial Centerlines operations beyond the standard user role.|
|Industrial Centerlines user|View Industrial Centerlines data and execute centerline tasks to confirm equipment settings.|

## Industrial Centerlines benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Reduce quality and reliability losses|Routine verification of equipment settings against standard values|Operators|
|Standardize equipment base conditions|Setting definitions with defined value types and ranges|Equipment owners|
|Automate confirmation scheduling|Centerline standards integrated with Industrial Standards scheduling|Standard authors|
|Capture compliance evidence|Setting results recording confirmed values, changes, and compliance status|All Centerline users|
|Support continuous improvement|Versioned setting plans and specifications with effective date ranges|Equipment owners, Admins|

## How Industrial Centerlines integrates with ICW

Industrial Centerlines integrates with the following Industrial Connected Workforce components:

-   Industrial Standards: Industrial Centerlines standards extend the Industrial Standards framework, reusing its scheduling, state management, and publishing mechanisms. For more information, see [Exploring Industrial Standards](https://www.servicenow.com/docs/access?context=industrial-standards-landing-page).
-   Digital Factory Workspace: Industrial Centerlines tasks appear in the workspace task lists. Equipment settings are managed through a Settings tab on the Equipment form. For more information, see [Task lists in the Digital Factory Workspace](https://www.servicenow.com/docs/access?context=task-lists-digital-factory-workspace).
-   Operational Equipment Model: Setting definitions are associated with operational equipment items within the ISA-95 equipment hierarchy. For more information, see [Operational equipment form](https://www.servicenow.com/docs/access?context=operational-equipment-form).

-   **[Setting definitions and value types](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/icw-setting-definitions-and-value-types.md)**  
A setting definition describes a single configurable parameter on a piece of operational equipment, including its data type, value format, and optional properties such as criticality and classification.
-   **[Setting plans and specifications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/icw-setting-plans-and-specifications.md)**  
Setting plans group one or more setting specifications for a given equipment and material context. Setting specifications define the standard values and limits for each setting definition.

**Parent Topic:**[Exploring Digital Factory Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/industrial-connected-workforce/digital-factory-workspace/exploring-digital-factory-workspace.md)

