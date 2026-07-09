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
reading_time_minutes: 3
breadcrumb: [Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# CAM OSCAL

Open Security Controls Assessment Language \(OSCAL\) provides a standardized way to express control-related information, enabling interoperability, consistency, and automation in IT security. It supports the JSON format only. CAM supports OSCAL version 1.1.2.

OSCAL is a set of machine-readable formats developed by the National Institute of Standards and Technology \(NIST\). It’s designed to support the automation of security control assessments, compliance reporting, and risk management processes.

CAM supports the export and import of OSCAL data for both Catalog and System Security Plan \(SSP\) models.

## CAM supported OSCAL models

CAM OSCAL supports the following models:

-   **Catalog**

    According to NIST, the catalog model provides a structured, machine-readable representation of a catalog of controls. As part of the catalog model, using CAM you can get the following control-related information:

    -   Control objectives: These are mapped to controls. The Reference field in a control objective maps to the NIST control. The requirements of a control objective map to the statements of the NIST's control. Each part of the Description field in a control objective aligns with the sub-part of the NIST's control. Child control objectives are mapped to the control field. Related control objectives are mapped to the links field.
    -   Control objective requirements: Statements or control requirements further broken down from a control objective's description.
    -   Test templates: Tests done on controls. Each control has at least one test template, which has one assessment objective.
    -   Assessment Procedures: Assessment objectives of a test template or the tests done on controls.
-   **Overlay catalog**

    Policies that consist of control objectives and aren't part of NIST but can be included in an authorization package.

-   **Profile**

    According to NIST, the profile model provides a structured, machine-readable representation of a baseline. The profile model represents a baseline of selected controls from one or more control catalogs.

    -   Baseline controls: Small set of control objectives that are auto-populated based on the impact level, which is determined by the Information Type of an authorization package.
    -   Include-controls: Baseline controls that are part of the authorization package.
    -   Exclude-controls: Baseline controls marked as Not Applicable.
    A Profile consists of both Catalog and Overlay Catalog.

-   ****

    According to NIST, the OSCAL SSP model enables a system owner to express the system implementation of an information system within the context of a specific baseline or OSCAL profile. It represents a description of the control implementation of an information system.

    -   Authorization boundary: Defines the scope of a particular system that can be continuously managed and monitored using the CAM application.
    -   Authorization package: Created for processing assets or systems through the seven steps mandated by the RMF. For more information, see NIST RMF process overview.
    -   Information type: Defines the impact level of the package based on the criticality of the information system defined in the Categorize step.
    -   Control: When control objectives move to Implementation state, they become controls.
    -   Control requirement: When control objectives move to Implementation state, control objective requirements convert to control requirements.
    -   Inherited Control: Controls entirely inherited from parent authorization package, including all control requirements.
    -   Hybrid Control: Controls partially inherited from the parent authorization package.
-   **Assessment Plan \(AP\)**

    The Assessment Plan model represents the testing plan for an engagement: what needs to be tested and how testing will be performed. It supports the Assess step of the RMF process.

    Using CAM you can export and import the following AP-related information:

    -   Engagement metadata: Name, state, objectives, progress, timeline, and budget information
    -   Control tests: Tests specified for the engagement with assessment procedures and methods
    -   Users and roles: Assessors, auditors, approvers, and control test owners assigned to the engagement
    -   Test scope: System elements and components under assessment
-   **Assessment Results \(AR\)**

    The Assessment Results model represents completed engagement outcomes, including control test results, findings, and attestations. It captures assessment findings from the Assess step of the RMF process.

    Using CAM you can export and import the following AR-related information:

    -   Assessment outcomes: Test results \(effective/ineffective status\) and engagement findings
    -   Control findings: Weaknesses and observations identified during assessment
    -   POA&amp;M data: Plan of Action and Milestones items linked to findings
    -   Users and roles: Assessment team members and their assigned responsibilities

## Catalog

-   **[Export in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/oscal-support-cam.md)**  
CAM supports the Open Security Controls Assessment Language \(OSCAL\) used by the National Institute of Standards and Technology \(NIST\) that provides control-related information in standardized machine-readable formats. CAM supports Catalog, Profile, SSP, Assessment Plan \(AP\), Assessment Results \(AR\), and Control Tailoring Request data.
-   **[Import in OSCAL format](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/import-oscal.md)**  
The CAM OSCAL import offers a playbook-style experience designed to streamline the integration of security control data.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-ws-continuous-auth-monitor.md)

