---
title: Exporting Catalog, Profile, and SSP in OSCAL format
description: CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardised machine readable formats. CAM supports Catalog, Profile, and SSP models.
locale: en-US
release: xanadu
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2024-08-07"
reading_time_minutes: 3
breadcrumb: [Continuous authorization and monitoring tasks in the CAM Workspace, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Exporting Catalog, Profile, and SSP in OSCAL format

CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardised machine readable formats. CAM supports Catalog, Profile, and SSP models.

## Exporting SSP in CAM

With CAM, you can generate Catalog, Profile, System Security Plan \(SSP\) models and export the following:

-   **Catalog**

    According to NIST, the catalog model provides a structured, machine-readable representation of a catalog of controls. Therefore, as part of the catalog model, using CAM you can export the following control-related information:

    -   Control objectives: These are mapped to controls. The **Reference** field in a control objective maps to the NIST control. The requirements of a control objective map to the statements of the NIST's control. Therefore, each part of the **Description** field in a control objective align with the sub-part of the NIST's control. The child control objectives of each control objective are mapped to the control field. Related control objectives of the control objective are mapped to the links field.
    -   Control objective requirements: Statements or control requirements that are further broken down from a control objective's description.
    -   Test templates: Tests done on controls. Each control has at least one test template, which has one assessment objective.
    -   Assessment Procedures: These are assessment objectives of a test template or the tests done on controls.
    ![Export OSCAL UI actions.](../image/cam-export-oscal-ui.png)

-   **Overlay catalog**

    Overlay controls: These are policies that consist of control objectives and are not part of NIST but can be in an authorization package. Therefore, these are exported as a separate file.

-   **Profile**

    According to NIST, the profile model provides a structured, machine-readable representation of a baseline. The profile model also represents a baseline of selected controls from one or more control catalogs.

    Baseline controls: Small set of control objectives that are auto-populated based on the impact. Impact is decided based on the Information Type of an authorization package.

    -   Include-controls: These are baseline controls, which are part of the authorization package.
    -   Exclude-controls: These are baseline controls that have been marked as Not Applicable.
    Profile consists of both Catalog and Overlay Catalog.

-   **System Security Plan \(SSP\)**

    According to NIST, OSCAL SSP model enables a system owner to express the system implementation of an information system within the context of a specific baseline or OSCAL profile. Or, it represents a description of the control implementation of an information system.

    -   Authorization boundary: An authorization boundary defines the scope of a particular system that can be continuously managed and monitored using the CAM application.
    -   Authorization package: Created for the purpose of processing the assets or systems through the seven steps mandated by the RMF. For more information, see [NIST RMF process overview](../../grc-nist-rmf/concept/nist-rmf-process.md).
    -   Information type: Information type defines the impact level of the package, which is based on the criticality of the information system defined in the Categorize step.
    -   Control: When control objectives move to Implementation state, they become controls.
    -   Control requirement: When control objectives move to Implementation state, they become controls. Correspondingly, the control objective requirements convert to control requirement.
    -   Inherited Control: Controls that are entirely inherited from parent authorization package. Then, it means that all the control requirements of each such control are also inherited completely.
    -   Hybrid Control: These are partially inherited from the parent authorization package.

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

