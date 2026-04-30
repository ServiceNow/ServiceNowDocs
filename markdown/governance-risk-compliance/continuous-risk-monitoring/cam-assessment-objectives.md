---
title: Implementing controls and assessment objectives in CAM
description: NIST 800-53A – assessment objectives are included in the base system with the CAM application. The assessment objectives are mapped to revision 5 control objectives.
locale: en-US
release: yokohama
product: Continuous Risk Monitoring
classification: continuous-risk-monitoring
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Using CAM, Continuous Authorization and Monitoring, Governance, Risk, and Compliance]
---

# Implementing controls and assessment objectives in CAM

NIST 800-53A – assessment objectives are included in the base system with the CAM application. The assessment objectives are mapped to revision 5 control objectives.

**Note:**

-   NIST SP 800-53 is the Security and Privacy Controls for Federal Information Systems and Organizations.
-   NIST SP 800-53A is the Guide for Assessing the Security controls in Federal Information systems and organizations: Building Effective Security Assessment Plans.

Each test template has assessment procedure templates and is imported by the ServiceNow base system to CAM users for control objectives sourced by NIST 800-53 revision 5. Each assessment procedure template has an identifier and assessment objective. The assessment objective determines how controls are tested.

A new CAM view is available for control test in which design effectiveness is removed and there is only operating effectiveness, which is named as Operational test.

In CAM, a control is tested at a more granular level with multiple assessment procedures. The control test measures the effectiveness of a control. The effectiveness of a control test is measured through its operating effectiveness and assessment procedure effectiveness, based on which the control effectiveness of the control test is determined. A control test failure indicates the failure of the assessment objective as well.

New control test criteria such as Examine, Interview, and Test are available during control testing. These fields are read-only, however you can update these descriptions at the test template and test plan levels. A set of assessment procedures is available as a related list while control testing. Assessment procedures are at the objective level, and can be marked as not applicable in addition to being effective, ineffective, and none.

![Control objectives sourced by NIST for which test templates are provided.](../image/cam-nist-co.png "Control objectives sourced by NIST 800-53 revision 5")

