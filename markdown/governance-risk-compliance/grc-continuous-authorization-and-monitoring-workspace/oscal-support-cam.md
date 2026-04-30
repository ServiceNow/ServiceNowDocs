---
title: Exporting in OSCAL format
description: CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, and SSP models.
locale: en-US
release: yokohama
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Exporting in OSCAL format

CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, and SSP models.

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

-   **[Export OSCAL SSP](../task/generate-oscal-models.md)**  
From the Authorization package overview record page in the CAM Workspace, generate ZIP files and export the mapped content details for the record in OSCAL format. To generate OSCAL System Security Plan Model \(SSP\), the selected authorization package must be in the implemented state or further.
-   **[Export OSCAL catalog](../task/export-catalog-cam-ws.md)**  
From the Control objective list view page in the CAM Workspace, export the catalog in the OSCAL JSON format for the selected control objectives. This action enables you to export your control objectives from CAM.

**Parent Topic:**[CAM OSCAL](oscal-cam-ws.md)

