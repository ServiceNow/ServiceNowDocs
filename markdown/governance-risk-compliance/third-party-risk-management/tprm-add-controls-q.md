---
title: Manually add a control objective to a question
description: If you’re using both Policy and Compliance Management and Third-party Risk Management, you can associate control objectives and controls with questions. Controls can be marked as compliant or non-compliant based on the response to the question.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/third-party-risk-management/tprm-add-controls-q.html
release: australia
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [TPRM with Policy and Compliance Management, Integrate, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Manually add a control objective to a question

If you’re using both Policy and Compliance Management and Third-party Risk Management, you can associate control objectives and controls with questions. Controls can be marked as compliant or non-compliant based on the response to the question.

## Before you begin

Role required: sn\_compliance.manager and sn\_vdr\_risk\_asmt.vendor\_risk\_manager to associate control objectives in the Vendor Management Workspace.

## About this task

Control objectives are authored and managed in Policy and Compliance Management and can be associated with questions used in assessments.

A control objective is an objective, direction, or standard that acts as guidance for company interactions and operations. Control objectives can be categorized, classified, and related to policies.

For more information on creating policies in Policy and Compliance Management, see [Create a policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/t_DefineAPolicy.md).

To understand the difference between a control objective and a control, see [Structural overview of Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/pc-structural-overview-policy-comp.md).

**Note:** Although it is not possible to directly map control objectives to questions in SAE questionnaires, SAE provides the capability to flag controls as compliant or non-compliant through post-assessment actions.

## Procedure

1.  Navigate to **All** &gt; **Third-party Risk Management** &gt; **Assessment Setup** &gt; **Questionnaire Templates** and select the questionnaire template you want.

2.  Select the metric categories that you want from the related list and then select the question you want.

3.  Navigate to the Control Objectives related list and associate an existing control objective by selecting **New**.

4.  On the form, fill in the fields.

    For descriptions of all these fields, see [Control objectives form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-control-objective-form.md).

5.  Select **Submit**.

    For more information on managing controls, see [Manage controls](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/policy-and-compliance-management/c_GRCControls.md).

    The control objective is associated with the question and all related lists are visible.


-   **[Control objectives form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-control-objective-form.md)**  
Use the control objectives form to capture all the information that you need to associate a control objective with a question using the Third-party Risk Management application.

**Parent Topic:**[Integrating Third-party Risk Management with GRC: Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/pc-assessment-integration.md)

**Related topics**  


[Integrating Third-party Risk Management with GRC: Policy and Compliance Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/pc-assessment-integration.md)

[Manually add a control to a third party or engagement](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-add-controls-tp.md)

[Control objectives form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-control-objective-form.md)

[Create new control form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/third-party-risk-management/tprm-control-record-form.md)

