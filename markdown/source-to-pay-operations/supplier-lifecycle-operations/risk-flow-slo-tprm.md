---
title: Risk assessment flow when Third-party Risk Due Diligence is installed
description: If you have installed both the Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] and GRC: Third-party Risk Due Diligence \[com.sn\_tprm\_onboarding\] plugins, the Perform risk assessment playbook triggers the flow that includes activities to create a due diligence request, complete Inherent Risk Questionnaire \(IRQ\) assessments, and conduct risk assessments for a third-party and an engagement.
locale: en-US
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use the risk assessment playbook, Create a supplier, Using Source-to-Pay Workspace, Use, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Risk assessment flow when Third-party Risk Due Diligence is installed

If you have installed both the Risk Assessments Integration for Supplier Lifecycle Operations \[com.snc.sn\_supplier\_tprm\] and GRC: Third-party Risk Due Diligence \[com.sn\_tprm\_onboarding\] plugins, the Perform risk assessment playbook triggers the flow that includes activities to create a due diligence request, complete Inherent Risk Questionnaire \(IRQ\) assessments, and conduct risk assessments for a third-party and an engagement.

In this flow, the following occurs:

1.  The supplier manager receives a supplier onboarding request.
2.  The supplier manager uses the onboarding playbook, which provides a streamlined and guided process to onboard suppliers. For more information, see [Use the supplier onboarding playbook to onboard suppliers](use-playbooks-onboard-supp.md#).
3.  The supplier manager submits a due diligence request. For more information about the fields in this activity, see [Request due diligence for a third-party engagement](https://www.servicenow.com/docs/access?context=tprm-ws-request-dd-for-engagement&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).

    The supplier manager must fill in the details and assign the due diligence request to the TPR manager.

    **Note:** For each due diligence request, the system auto-assigns a unique ID number that starts with the prefix **DDR**.

4.  If the due diligence request is approved by the TPR manager, the inherent risk questionnaire \(IRQ\) is sent to the TPR assessor \(internal stakeholder\).
5.  After the TPR assessor submits the completed IRQ, the due diligence process begins.
6.  The due diligence process creates two risk assessments, each containing an external due diligence questionnaire, one for the third-party and another for engagement.
7.  After the supplier contacts complete and submit the external questionnaires from the Supplier Collaboration Portal, the TPR manager goes through the questionnaires and approves the due diligence request.
8.  A contract record is created with an approval. After the contract record is approved, the risk record is updated with the final rating.
9.  After the supplier manager accepts the risk rating, an email is sent to the requester informing that the due diligence request has been successfully processed and approved.
10. The supplier manager closes the due diligence request \(case\).

    After the case is closed, you can continue with completing the activities in the Activation stage.

    For more information about the due diligence workflow, see [Due diligence workflow](https://www.servicenow.com/docs/access?context=tprm-workflow-in-workspace&version=australia&pubname=australia-governance-risk-compliance&ft:locale=en-US).


-   **[Playbook stages and activities when Third-party Risk Due Diligence is installed](risk-flow-tprmdd-stages.md)**  
The following table lists the Perform risk assessment playbook stages and activities when Third-party risk Due Diligence is installed.

**Parent Topic:**[Perform risk assessment playbook](perform-risk-playbook.md)

**Related topics**  


[Playbook stages and activities when Third-party Risk Due Diligence is installed](risk-flow-tprmdd-stages.md)

