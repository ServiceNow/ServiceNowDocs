---
title: Export in OSCAL format
description: CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, SSP, and Assessment Plan \(AP\) models.
locale: en-US
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export in OSCAL format

CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, SSP, and Assessment Plan \(AP\) models.

## Source tables to fetch data for the models

|Source table|JSON property|
|------------|-------------|
|Catalog|
|Control objective|controls|
|Control Objective to Control objective requirement|statements parts|
|Test template to Assessment procedure|assessment objective parts|
|Control Objective|guidance|
|Test Template|Assessment-method \(Examine\)|
|Test Template|Assessment-method \(Interview\)|
|Profile|
|Baseline Control|Include-controls|
|Baseline Control|Exclude-controls|
|SSP|
|Authorization boundary|components|
|Authorization package|leveraged-authorization|
|Authorization boundary|security-impact-level|
|Control requirement|statements|
|Authorization boundary|by-components|
|Information type|Information-types|
|Assessment Plan|
|Engagement|assessment-plan|
|Engagement metadata|metadata \(title, state, objectives, progress, dates, budget\)|
|Users|metadata.parties|
|Roles|metadata.roles, responsible-parties|
|Control tests|local-definitions.activities|
|Assessment procedures|local-definitions.activities.steps|
|Controls in scope|reviewed-controls|
|Package reference|import-ssp.href|

Using the CAM export OSCAL feature, you can perform the following:

-   [Export OSCAL catalog](../task/export-catalog-cam-ws.md)
-   [Export OSCAL SSP](../task/generate-oscal-models.md)
-   [Export an OSCAL Assessment Plan](../../grc-cam/task/export-oscal-assessment-plan.md)

For more information about OSCAL Assessment Plan export, see [OSCAL Assessment Plan export and import](../../grc-cam/concept/oscal-assessment-plan-import-export.md).

-   **[Export OSCAL catalog](../task/export-catalog-cam-ws.md)**  
From the Control objective list view page, you can export the catalog in OSCAL JSON format for the selected control objectives. This action enables you to export your control objectives from CAM.
-   **[Export OSCAL SSP](../task/generate-oscal-models.md)**  
From the Authorization package overview record page, generate zip files and export the record's mapped content details in OSCAL format. To generate OSCAL SSP, the selected Authorization package must be in implemented state or after that. This action enables you to export your authorization package from CAM.
-   **[Export an OSCAL Assessment Plan](../../grc-cam/task/export-oscal-assessment-plan.md)**  
Export engagement data as OSCAL Assessment Plan files to share testing plans with auditors or import into external systems.

**Parent Topic:**[CAM OSCAL](oscal-cam-ws.md)

