---
title: Implement controls and assessment objectives
description: NIST 800-53A – assessment objectives are included in the base system with the CAM application. The assessment objectives are mapped to revision 5 control objectives.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-assessment-objectives.html
release: australia
product: GRC: Continuous Authorization and Monitoring Workspace
classification: grc-continuous-authorization-and-monitoring-workspace
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Continuous authorization and monitoring tasks in the CAM Workspace, Use, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Implement controls and assessment objectives

NIST 800-53A – assessment objectives are included in the base system with the CAM application. The assessment objectives are mapped to revision 5 control objectives.

**Note:**

-   NIST SP 800-53 is the Security and Privacy Controls for Federal Information Systems and Organizations.
-   NIST SP 800-53A is the Guide for Assessing the Security controls in Federal Information systems and organizations: Building Effective Security Assessment Plans.

Each test template has assessment procedure templates and is imported by the ServiceNow base system to CAM users for control objectives sourced by NIST 800-53 revision 5. Each assessment procedure template has an identifier and assessment objective. The assessment objective determines how controls are tested.

A new CAM view is available for control test in which design effectiveness is removed and there is only operating effectiveness, which is named as Operational test.

In CAM, a control is tested at a more granular level with multiple assessment procedures. The control test measures the effectiveness of a control. The effectiveness of a control test is measured through its operating effectiveness and assessment procedure effectiveness, based on which the control effectiveness of the control test is determined. A control test failure indicates the failure of the assessment objective as well.

New control test criteria such as Examine, Interview, and Test are available during control testing. These fields are read-only, however you can update these descriptions at the test template and test plan levels. A set of assessment procedures is available as a related list while control testing. Assessment procedures are at the objective level, and can be marked as not applicable in addition to being effective, ineffective, and none.

\[Omitted image "cam-nist-co.png"\] Alt text: Control objectives sourced by NIST for which test templates are provided.

-   **[Generate assessment procedure plans for a test plan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-assess-controls-assess-obj.md)**  
Use the test plan that is automatically generated for a control, which is in an assess state, to view and determine if the control is assessed in accordance with the assessment procedure plan.
-   **[Determine control effectiveness of a control test](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-control-effectiveness-control-test.md)**  
Apply the objective effectiveness of the assessment procedures and the operating effectiveness of the control test to determine the control effectiveness of the control test. An assessment procedure is applied to check the control test at a granular level.
-   **[Define control requirements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-control-req-sca.md)**  
You can break down a control at a more granular level as requirements when you generate the control at the control objective level.
-   **[Modify control requirement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-ap-control-req.md)**  
Approve the authorization package when it is in the Select step to create controls. After approval, the authorization package moves to the Implement step and the controls are generated. You can still modify the control requirement implementation status at the control level.
-   **[Control requirement generation and upgrade steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-upgrade-scene.md)**  
The **Creates controls automatically** and **Create control requirements** options in the control objective form and the state of the authorization package are important to create control requirements.
-   **[View control tests in grid view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/view-control-tests-in-grid-view.md)**  
View and edit control tests and assessment procedures in a hierarchical data grid.

**Parent Topic:**[Continuous authorization and monitoring tasks in the CAM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/grc-continuous-authorization-and-monitoring-workspace/cam-ws-continuous-auth-monitor.md)

