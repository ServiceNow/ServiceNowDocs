---
title: CAM OSCAL
description: Open Security Controls Assessment Language \(OSCAL\) provides a standardized way to express control-related information, enabling interoperability, consistency, and automation in IT security. It supports the JSON format only. CAM supports OSCAL version 1.1.2.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-cam-ws.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Continuous authorization and monitoring tasks in the CAM Workspace, Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# CAM OSCAL

Open Security Controls Assessment Language \(OSCAL\) provides a standardized way to express control-related information, enabling interoperability, consistency, and automation in IT security. It supports the JSON format only. CAM supports OSCAL version 1.1.2.

OSCAL is a set of machine-readable formats developed by the National Institute of Standards and Technology \(NIST\). It’s designed to support the automation of security control assessments, compliance reporting, and risk management processes.

CAM supports the export and import of OSCAL data for both Catalog and System Security Plan \(SSP\) models.

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
    -   Authorization package: Created for the purpose of processing the assets or systems through the seven steps mandated by the RMF. For more information, see [NIST RMF process overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-common-functions/nist-rmf-process.md).
    -   Information type: Information type defines the impact level of the package, which is based on the criticality of the information system defined in the Categorize step.
    -   Control: When control objectives move to Implementation state, they become controls.
    -   Control requirement: When control objectives move to Implementation state, they become controls. Correspondingly, the control objective requirements convert to control requirement.
    -   Inherited Control: Controls that are entirely inherited from parent authorization package. Then, it means that all the control requirements of each such control are also inherited completely.
    -   Hybrid Control: These are partially inherited from the parent authorization package.

-   **[Export in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-support-cam.md)**  
CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, SSP, Assessment Plan \(AP\), Assessment Results \(AR\), and Control Tailoring Request data.
-   **[Import in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal.md)**  
The CAM OSCAL import offers a playbook-style experience designed to streamline the integration of security control data.
-   **[OSCAL Assessment Plan field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-ap-field-mapping.md)**  
CAM exports engagement and control test data to OSCAL Assessment Plan format using the following field mappings.
-   **[OSCAL Assessment Results field mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-ar-field-mapping.md)**  
CAM exports engagement and control test result data to the OSCAL Assessment Results \(AR\) format using the following field mappings.
-   **[Oscal Catalog fields mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-catalog-fields-mapping.md)**  
CAM exports catalog and control data to OSCAL Catalog format using the following field mappings.
-   **[OSCAL SSP fields mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-ssp-fields-mapping.md)**  
CAM exports authorization package and control data to OSCAL System Security Plan \(SSP\) format using the following field mappings.
-   **[OSCAL POAM fields mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-poam-fields-mapping.md)**  
CAM exports POA&amp;M item data to OSCAL Plan of Action and Milestones \(POA&amp;M\) format using the following field mappings.
-   **[OSCAL custom properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-namespace.md)**  
Custom properties with a unique namespace are used to include specific information, capture impact, and tailor OSCAL content for CAM import and export across all supported models.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-ws-continuous-auth-monitor.md)

