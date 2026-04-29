---
title: Policy Exception Integration with Vulnerability Response
description: Starting with Version 10.1, you can request policy exceptions using the GRC policy exception management capability inherent in the Policy and Compliance Management application from within version 10.3 of the Vulnerability Response application.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Manage policy exceptions and extensions, Classic UI, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Policy Exception Integration with Vulnerability Response

Starting with Version 10.1, you can request policy exceptions using the GRC policy exception management capability inherent in the Policy and Compliance Management application from within version 10.3 of the Vulnerability Response application.

## Benefits of using the Policy Exception Integration

Requesting exceptions using the policy exception integration with Policy and Compliance Management provides the following benefits:

-   Perform assessments to gather additional information about the requests.
-   Request exceptions based on a specific policy or control objective. This action shows the effects on compliance when an exception is approved.
-   Configure approvals to be triggered automatically based on the risk rating, policy, or control objective associated with the policy exception.

## How the Policy Exception Integration works

The scenario described here assumes that a vulnerability has been identified in your system and your remediation owner has determined that a software patch is needed. The patch has not been fully tested and the owner is requesting a policy exception to defer deployment of the patch until testing is complete.

The following diagram illustrates the steps performed by the compliance manager and the remediation owner in each of the applications.

![Policy exception integration workflow](../image/pe-integration-workflow.png "Policy Exception integration")

**Note:** The GRC business user \(sn\_grc.business\_user\) or business user – lite \(sn\_grc.business\_user\_lite\) is the minimum required role to raise a policy exception from an upstream application.

1.  When the Vulnerability Response application was installed, two policy exception integration records are automatically created and added to the Integration Registry, one for a vulnerability group and one for a vulnerable item.

    ![Policy exception integration Register.](../image/pe-integ-reg.png "Policy exception integration register")

    To configure the vulnerable item record, the compliance manager performs the following steps.

    1.  [Identifies the mapping of tables used to integrate the two applications](../concept/allow-other-app-policy-except.md).
    2.  [Defines reasons for requesting exceptions](../task/define-reason-choices.md).
    3.  \(optionally\) [Defines policy categories](../task/define-policy-categories.md) for filtering policies
    4.  \(optionally\) [Creates one or more questionnaires](../task/create-except-quest.md) to be sent to the requester to gather additional information about the policy exception request.
2.  The compliance manager also defines optional [verification rules](../task/define-verification-rules.md) and [approval rules](../task/define-approval-rules.md) to automate the process of getting approvals for the policy exception.
3.  In Vulnerability Response, the remediation owner [Request an exception using GRC: Policy and Compliance Management](https://www.servicenow.com/docs/access?context=integration-with-grc&version=australia&pubname=australia-security-management&ft:locale=en-US) .
4.  If a verification rule was defined for the application, the designated approvers are notified that their approval is required. If any fields in the policy exception request were not filled in by the requester \(for example, the Policy or Control Objective\), those fields become mandatory for the approvers. When the approvers have reviewed, completed, and approved the request, it transitions to the Analyze state and is assigned to the compliance manager for further analysis and approval.
5.  In Policy and Compliance Management, the compliance manager receives the approved request, and assigns a risk rating to the policy exception request on the **Risk assessment** tab.

    ![Risk assessment](../image/risk-assess.png "Policy exception request on the Risk assessment tab")

    When the policy exception record is saved, information in the **Source** tab, including the source application and source record, as well as information in the **Vulnerable Items** related list are auto-populated. The compliance manager now has access to all the data needed to review and approve the policy exception.

6.  In Policy and Compliance Management, the compliance manager performs the exception assessment, [if assessments were configured](../task/create-except-quest.md). When the assessment is completed, the compliance manager returns to the **Risk assessment** tab and updates the **Risk rating** based on the findings of the assessment, if needed. The compliance manager also populates the following fields with information gathered during the assessment.

    |Field|Description|
    |-----|-----------|
    |Risk description|Provide details about the risk associated with this policy exception.|
    |Analysis of risk and impact|Provide details about your analysis of the risk and impact to the policy exception.|
    |Risk mitigation plan|Provide details about the mitigation plan associated with this policy exception.|

7.  If the policy exception is missing any information, the compliance manager can click **Request More Information** and add comments to identify the type of data needed. The requester is notified and provides the requested information.
8.  Optionally, the compliance manager can send the policy exception out for an additional in-house review before approving it by clicking **Request Review**.

    **Note:** Prior to requesting a review, ensure that the Impacted Controls related list contains the controls that are impacted by the policy exception. Simply open the related list, click **Add**, and select the controls.

9.  If the policy exception is of a particularly high risk, and the compliance manager believes that approval should come from someone higher in the organization \(for example, the CIO\), the compliance manager can click **Request Approval**.

    Otherwise, approval is performed in the following scenarios.

<table id="table_hdc_l3n_rlb"><thead><tr><th>

Approval rule defined

</th><th>

Effect on approval

</th></tr></thead><tbody><tr><td>

If an approval rule was not defined for Vulnerability Response

</td><td>

Selecting **Approved** causes the policy exception to be approved.

</td></tr><tr><td>

[If an approval rule was defined](../task/define-approval-rules.md), but the **Auto-trigger** check box was not selected

</td><td>

You can click **Request Approval** to send the policy exception to the users or groups defined in the rule. For example, an approval rule may indicate that when the policy exception is based on a particular policy, a certain set of users or groups are notified that they need to provide approval for the policy exception. Or, an approval rule may be defined so that any policy exception with a risk rating of Critical is automatically sent to a certain set of approvers.The number of approvers necessary to approve the policy exception depends on the setting in the **Required Approval** field in the rule.

 You can also click **Approve** to approve the policy exception yourself.

</td></tr><tr><td>

If an approval rule was defined, and the **Auto-trigger** check box was selected

</td><td>

Clicking the **Approve** button causes the approval rule to be executed and the policy exception is automatically sent to the users or groups defined by the rule for approval. Auto-trigger causes this step to be mandatory. When approvals are received, the policy exception goes into effect.

</td></tr></tbody>
</table>10. In Vulnerability Response, after the approvals have been received, the policy exception becomes active and the patching activity on the vulnerable item is deferred until the policy exception expires. When the **Valid until** date is reached, the policy exception expires and the state of the vulnerable item changes from Deferred to Open.

**Parent Topic:**[Manage policy exceptions and extensions](../concept/manage-policy-exceptions.md)

