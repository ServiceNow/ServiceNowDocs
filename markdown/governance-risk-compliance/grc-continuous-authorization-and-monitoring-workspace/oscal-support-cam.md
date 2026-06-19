---
title: Export in OSCAL format
description: CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, SSP, Assessment Plan \(AP\), Assessment Results \(AR\), and Control Tailoring Request data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-support-cam.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [CAM OSCAL, Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Export in OSCAL format

CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, SSP, Assessment Plan \(AP\), Assessment Results \(AR\), and Control Tailoring Request data.

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
|Test plan|local-definitions.activities.related-controls.control-objective-selections|
|Test template|local-definitions.activities.props|
|Assessment procedures|local-definitions.activities.steps|
|Controls in scope|reviewed-controls|
|Package reference|import-ssp.href|
|Assessment Results|
|Engagement|results \(actual dates, actual cost, state, percent complete\)|
|Engagement metadata|metadata \(responsible parties, roles, parties, props\)|
|Control tests|local-definitions.activities, results.attestations|
|Assessment procedures|local-definitions.activities.steps, results.attestations.parts.parts|
|Reviewed controls|results.reviewed-controls|
|AP reference|import-ap.href|
|Control Tailoring Requests|
|Roles ctr-opened-by, ctr-assigned-to\)|metadata.roles\[\].id, metadata.roles\[\].title|
|Users \(Control Tailoring Request Opened by, Control Tailoring Request Assigned to\)|metadata.responsible-parties\[\].role-id, metadata.responsible-parties\[\].party-uuids\[\]|
|Traceability props|system-characteristics.props|

**Control Tailoring Request data in OSCAL files**

When you generate OSCAL files for an authorization package, the export now includes overlays from both the authorization package and any associated control tailoring requests. Previously, only package-level overlays were included.

The number of overlay catalog files generated reflects the total number of distinct overlays across the package and its control tailoring requests. For example, if a package has two overlays and a control tailoring request introduces a third, the export produces three overlay catalog files.

The OSCAL export files also include control tailoring request data. The data includes baseline controls, and overlays with references to their associated control tailoring requests. The metadata section includes:

-   Responsible parties: the CTR Assigned To role and CTR Opened By role, alongside existing package and boundary role assignments
-   Roles: CTR-specific roles exported alongside existing package roles
-   System characteristics props: props representing control tailoring request data for traceability

For more information, see the following topics:

-   [Export OSCAL catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/export-catalog-cam-ws.md)
-   [Export OSCAL SSP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/generate-oscal-models.md)
-   [Export an OSCAL Assessment Plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/export-oscal-assessment-plan.md)
-   [Export OSCAL Assessment Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-oscal-assessment-result-export.md)

-   **[Export OSCAL catalog](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/export-catalog-cam-ws.md)**  
From the Control objective list view page, you can export the catalog in OSCAL JSON format for the selected control objectives. This action enables you to export your control objectives from CAM.
-   **[Export OSCAL SSP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/generate-oscal-models.md)**  
From the Authorization package overview record page, generate zip files and export the record's mapped content details in OSCAL format. To generate OSCAL SSP, the selected Authorization package must be in implemented state or after that. This action enables you to export your authorization package from CAM.
-   **[Export OSCAL POA&amp;M](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/export-oscal-poa-m.md)**  
Generate zip files Plan of Action and Milestones \(POA&amp;M\) data in Open Security Controls Assessment Language \(OSCAL\) JSON format from the Authorization package overview record page. The authorization package must be in Implement state or later, and a POA&amp;M file must link to the selected authorization package.
-   **[Export an OSCAL Assessment Plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/export-oscal-assessment-plan.md)**  
Export engagement data as OSCAL Assessment Plan files to share testing plans with auditors or import into external systems.
-   **[Export OSCAL Assessment Results](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-oscal-assessment-result-export.md)**  
Export the OSCAL Assessment Results \(AR\) file for an authorization package from the CAM Workspace.

**Parent Topic:**[CAM OSCAL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-cam-ws.md)

