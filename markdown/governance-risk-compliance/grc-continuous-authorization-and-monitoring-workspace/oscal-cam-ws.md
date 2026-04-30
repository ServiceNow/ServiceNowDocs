---
title: CAM OSCAL
description: Continuous Authorization and Monitoring supports Open Security Controls Assessment Language \(OSCAL\) version 1.1.2 for importing and exporting security control data in JSON format.
locale: en-US
release: zurich
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# CAM OSCAL

Continuous Authorization and Monitoring supports Open Security Controls Assessment Language \(OSCAL\) version 1.1.2 for importing and exporting security control data in JSON format.

OSCAL provides a standardized way to express control-related information, enabling interoperability, consistency, and automation in IT security. The National Institute of Standards and Technology \(NIST\) developed OSCAL to support automated security control assessments, compliance reporting, and risk management processes using machine-readable formats. CAM supports OSCAL version 1.1.2 and accepts only JSON format files.

CAM supports Catalog, Profile, System Security Plan \(SSP\), and Plan of Action and Milestones \(POA&amp;M\) models for importing and exporting OSCAL data. The Catalog model provides a structured representation of security controls. The SSP model enables system owners to document system implementation within a specific baseline or OSCAL profile. The POA&amp;M model tracks security weaknesses and remediation activities.

## CAM supported OSCAL models

CAM OSCAL supports the following models:

-   **Catalog**

    According to NIST, the catalog model provides a structured, machine-readable representation of a catalog of controls. Therefore, as part of the catalog model, using CAM you can get the following control-related information:

    -   Control objectives: These are mapped to controls. The **Reference** field in a control objective maps to the NIST control. The requirements of a control objective map to the statements of the NIST's control. Therefore, each part of the **Description** field in a control objective align with the sub-part of the NIST's control. The child control objectives of each control objective are mapped to the control field. Related control objectives of the control objective are mapped to the links field.
    -   Control objective requirements: Statements or control requirements that are further broken down from a control objective's description.
    -   Test templates: Tests done on controls. Each control has at least one test template, which has one assessment objective.
    -   Assessment Procedures: These are assessment objectives of a test template or the tests done on controls.
-   **Overlay catalog**

    Overlay controls: These are policies that consist of control objectives and are not part of NIST but can be in an authorization package.

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
-   **Plan of Action and Milestones**

    The Plan of Action and Milestones \(POA&amp;M\) model provides a structured representation of identified security weaknesses, planned remediation activities, and associated milestones according to National Institute of Standards and Technology \(NIST\) specifications. This model enables organizations to track and document the resolution of security findings and compliance gaps.

    Plan of Action and Milestones \(POA&amp;M\) records link to authorization packages and contain structured lists of issues, milestones, and acceptance tasks. Each POA&amp;M entry identifies a specific weakness or finding, documents the remediation plan, assigns responsibility for resolution, and tracks completion milestones. POA&amp;M items can map to specific controls, control requirements, or control tests within the authorization package, establishing traceability between findings and affected controls.

    Acceptance tasks within POA&amp;M records define discrete actions required to remediate the identified weakness. Milestones track progress toward completion and provide target dates for remediation activities. The POA&amp;M model supports both inherited and unique findings, enabling organizations to track weaknesses that span multiple authorization packages or system boundaries.


-   **[Export in OSCAL format](oscal-support-cam.md)**  
Continuous Authorization and Monitoring supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, System Security Plan \(SSP\), and Plan of Action and Milestones \(POA&amp;M\) models.
-   **[Import in OSCAL format](import-oscal.md)**  
Import Open Security Controls Assessment Language \(OSCAL\) formatted Catalog, System Security Plan \(SSP\), and Plan of Action and Milestones \(POA&amp;M\) into Continuous Authorization and Monitoring using a guided playbook experience that validates data and manages conflicts.
-   **[OSCAL namespace](oscal-namespace.md)**  
To include CAM specific information, custom properties with a unique namespace are used to add impact and tailor the content as needed.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](cam-ws-continuous-auth-monitor.md)

