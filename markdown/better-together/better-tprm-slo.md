---
title: Minimize risk by assessing suppliers during the onboarding process
description: With Risk Assessments Integration for Supplier Lifecycle Operations, you can identify and assess potential supplier risks when onboarding new suppliers.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Solutions]
---

# Minimize risk by assessing suppliers during the onboarding process

With Risk Assessments Integration for Supplier Lifecycle Operations, you can identify and assess potential supplier risks when onboarding new suppliers.

## Combined benefits of integrating Supplier Lifecycle Operations with Third-party Risk Management

<table id="table_jcw_cxv_hyb"><thead><tr><th>

Feature

</th><th>

Supplier Lifecycle Operations

</th><th>

Third-party Risk Management

</th><th>

All applications together

</th></tr></thead><tbody><tr><td>

Supplier onboarding

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Information and data management

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Case and dispute management

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Risk onboarding

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Third-party risk due diligence, external and internal risk assessment

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Risk intelligence

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Risk scoring and monitoring

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr><tr><td>

Risk executive dashboard

</td><td>

![No](../../reuse/images/icon-error-red-x.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td><td>

![Yes](../../reuse/images/icon-check-mark-green.png)

</td></tr></tbody>
</table>## Workflow of Risk Assessments Integration for Supplier Lifecycle Operations

Use Supplier Lifecycle Operations and Third-party Risk Management together for these benefits:

-   Evaluate supplier risk when onboarding suppliers
-   Analyze risk score to determine whether to onboard a supplier

The following figure shows an example workflow of how a supplier manager and a third-party risk \(TPR\) assessor can use the applications together to evaluate supplier risk.

![SLO and TPRM risk assessment flow](../image/supp-onboarding-dd.png "The Supplier Lifecycle Operations and Third-party Risk Management workflow")

In this workflow:

1.  The supplier manager receives a supplier onboarding request.
2.  The supplier manager uses the onboarding playbook, which provides a streamlined and guided process to onboard suppliers. For more information, see [Using the supplier onboarding playbook to onboard suppliers](https://www.servicenow.com/docs/access?context=use-playbooks-onboard-supp&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).
3.  The supplier manager submits a due diligence request.

    Performing due diligence is a key aspect of onboarding a supplier. The supplier risk assessment is done by the third-party risk \(TPR\) assessor. For more information, see [Get started with Risk Assessments Integration for Supplier Lifecycle Operations](#get-started-risk-assess).

4.  The TPR manager approves the due diligence request.
5.  The inherent risk questionnaire is created and assigned to the TPR assessor.
6.  The TPR assessor submits the completed IRQ.
7.  Two risk assessment questionnaires are created and assigned to the supplier contact.
8.  The supplier contact logs in to the Supplier Collaboration Portal and completes the risk assessment questionnaires.
9.  A contract record is created with an approval. After the contract record is approved, the risk record is updated with the final rating.
10. The supplier manager accepts the risk rating and closes the due diligence request.

## Requirements for integrating Supplier Lifecycle Operations and Third-party Risk Management

1.  Install the Supplier Lifecycle Operations \(com.snc.sn\_supplier\_mgmt\) application from the ServiceNow® Store. For more information, see [Install Supplier Lifecycle Operations](https://www.servicenow.com/docs/access?context=install-supp-mgmt&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).
2.  Install and activate the Risk Assessments Integration for Supplier Lifecycle Operations \(com.snc.sn\_supplier\_tprm\) plugin.
3.  Install the Third-party Risk Management \(com.sn\_vdr\_risk\_asmt\) application from the ServiceNow® Store. For more information, see [Configuring Third-party Risk Management](https://www.servicenow.com/docs/access?context=tprm-configuring&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).
4.  Install and activate the GRC: Third-party Due Diligence Request \(com.sn\_tprm\_onboarding\) plugin.

**Note:** You must have a license for Third-party Risk Management \(formerly Vendor Risk Management\) to take advantage of this better together solution.

## Get started with Risk Assessments Integration for Supplier Lifecycle Operations

Get started with Risk Assessments Integration for Supplier Lifecycle Operations by completing these tasks:

1.  Create a supplier. For more information, see [Create a supplier from the Source-to-Pay Workspace](https://www.servicenow.com/docs/access?context=new-supplier&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).
2.  Onboard a new supplier using playbooks. For more information, see [Using the supplier onboarding playbook to onboard suppliers](https://www.servicenow.com/docs/access?context=use-playbooks-onboard-supp&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).
3.  The playbook creates a due diligence request. For more information about the fields in this activity, see [Request due diligence for a third-party engagement](https://www.servicenow.com/docs/access?context=tprm-ws-request-dd-for-engagement&version=xanadu&pubname=xanadu-governance-risk-compliance&ft:locale=en-US).
4.  The supplier manager fills and submits a due diligence request, which is assigned to the TPR manager.

    **Note:** For each due diligence request, the system auto-assigns a unique ID number that starts with the prefix **DDR**.

5.  If the due diligence request is approved by the TPR manager, the inherent risk questionnaire \(IRQ\) is sent to the TPR assessor \(internal stakeholder\).
6.  After the TPR assessor submits the completed IRQ, the due diligence process begins.
7.  The due diligence process creates two risk assessments, each containing an external due diligence questionnaire, one for the third-party and another for engagement.
8.  After the supplier contacts complete and submit the external questionnaires from the Supplier Collaboration Portal, the TPR manager goes through the questionnaires and approves the due diligence request. For more information, see [Complete a risk assessment from the Supplier Collaboration Portal](https://www.servicenow.com/docs/access?context=complete-risk-assessments&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US).
9.  A contract record is created with an approval. After the contract record is approved, the risk record is updated with the final rating.
10. After the supplier manager accepts the risk rating, an email is sent to the requester informing that the due diligence request has been successfully processed and approved.
11. The supplier manager closes the due diligence request \(case\).
12. As a supplier manager, you can use the risk assessment result data in combination with any other data to determine whether to continue or cancel the onboarding process.

**Parent Topic:**[Solutions](../reference/solutions-gallery.md)

