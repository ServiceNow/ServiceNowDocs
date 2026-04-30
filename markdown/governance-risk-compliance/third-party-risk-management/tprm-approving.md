---
title: Approving or rejecting requests for due diligence
description: Set up the approval levels and rules for due diligence requests in the Third-party Risk Management application to use while approving or rejecting requests after reviewing questionnaire responses and due diligence process results.
locale: en-US
release: xanadu
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Third-party Risk Management, Governance, Risk, and Compliance]
---

# Approving or rejecting requests for due diligence

Set up the approval levels and rules for due diligence requests in the Third-party Risk Management application to use while approving or rejecting requests after reviewing questionnaire responses and due diligence process results.

## Approval process overview

Approval levels and rules are used to determine which team members are assigned as approvers to the due diligence request. During the approval process, approvers review the external questionnaire responses and supporting documents that were provided by the third-party contact. They also consider any other information that was gathered during the due diligence process. Approvers can approve or reject due diligence requests depending on their interpretation of the information reviewed.

For more information on managing approvals, approval levels, and approval rules, see [Approval process management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-approvals.md).

**Note:** Any multi-level approvals related to a workflow require updates to be made using Workflow Studio. For more information on creating flows using Workflow Studio, see [Create a flow in Workflow Studio](https://www.servicenow.com/docs/access?context=create-flow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Setting up approval levels and rules

You must have the admin or Third-party risk \(TPR\) admin \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role to make the approval levels and rules for due diligence requests. You can create up to 10 different approval levels that each contain different approval rules. Within each approval level, you can assign one or more rules with different filter conditions that apply to the assigned approvers. For example, you might want different approvers to be assigned to the due diligence request depending on the engagement's risk rating and location.

With the Third-party due diligence default configuration, you can create three records with approval levels 1, 2, and 3. Level 1 has three rules, level 2 has two rules, and level 3 has two rules. The following example shows how you would assign these rules with filter conditions:

-   Level 1
    -   Rule 1: User A and User B are assigned to approve the engagement's low risk rating.
    -   Rule 2: User C and User D are assigned to approve the engagement's medium risk rating.
    -   Rule 3: User E and User F are assigned to approve the engagement's high-risk rating.
-   Level 2
    -   Rule 1: TPR manager is assigned to approve the engagement in Asia/Pacific.
    -   Rule 2: TPR manager is assigned to approve the engagement in Europe/North America.
-   Level 3
    -   Rule 1: All TPR administrators are assigned to approve an engagement in a specific region that has a high-risk rating.
    -   Rule 2: All TPR administrators are assigned to approve an engagement in a specific region that has a very high-risk rating.

During the approval process, level 1 is triggered first. If all assigned users approve the conditions in level 1, then level 2 is triggered and so on. If any assigned user in level 1 has rejected the due diligence request, level 2 isn't triggered and the due diligence request is rejected. For more information on possible rating definitions, see [Set up risk rating scales for scoring](../../grc-vendor-risk-implementation/task/tprm-risk-rating-scales-config.md).

**Note:** You can use the Third-party due diligence default configuration included as part of the base system or deactivate the default configuration and create an approval configuration that applies to a different table. For more information, see [Set up an approval configuration record](../../grc-common/task/set-up-approval-configurator.md).

For more information on setting up approval levels and rules, see [Set up the approval levels for due diligence requests](../../grc-workspace-vrm/task/tprm-set-request-approval-levels.md) and [Set up the approval rules for due diligence requests](../../grc-workspace-vrm/task/tprm-set-request-approval-rules.md).

## Approving due diligence requests

The following infographic shows the approval process.

![Infographic that shows the approval process in the due diligence workflow. For the text description, refer to the text that follows.](../../grc-workspace-vrm/image/mmasset0020743-approval-process-custom.png)

The due diligence request enters the Ready for TPRM approval state after all assessments have been closed. The TPR manager \[sn\_vdr\_risk\_asmt.vendor\_risk\_manager\] or TPR assessor \[sn\_vdr\_risk\_asmt.vendor\_assessor\] that has been assigned as the owner of the due diligence request confirm approvers have been assigned to the due diligence request. After validating the assigned approvers, the TPR manager or owner requests approval. The due diligence request enters the Awaiting approval state and the system sends an email notification to all assigned approvers.

All internal stakeholders \(approvers\) review the external questionnaire responses and supporting documents that were provided by the third-party contact. You must be part of the Third-party risk \(TPR\) manager user group to make approvals. Approvers perform all actions by using Vendor Management Workspace or VRM Classic user interface. Approvers can view all of their pending **My approvals**, **Tasks**, and **Issues** by navigating to the Task page.

To view the Task page in the Vendor Management Workspace, select **Workspaces** &gt; **Vendor Management Workspace**. Then, select the task icon ![](../../grc-workspace-vrm/image/icon-tprm-ws-tasks.png).

To view your assigned approvals, select **My approvals**.

To view **My approvals** in the VRM Classic user interface, navigate to **All** &gt; **Self-Service** &gt; **Third-party Risk Management** &gt; **Due Diligence Requests** &gt; **My Approvals**

From this view, you can accomplish the following tasks:

-   Review the internal questionnaire responses.

    Navigate to the Due diligence request record page by selecting the Due Diligence Request \(DDR\) number and then selecting the Internal assessment \(INA\) number on the **Internal assessments** tab. For more information, see [IRQ process management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-irq-tab.md).

-   Review the risk intelligence scores.

    Navigate to the Due diligence request record page by selecting the DDR number and then selecting the **Risk intelligence scores** tab. For more information, see [Viewing risk intelligence scores](../../grc-workspace-vrm/reference/tprm-ws-tab-risk-intel-scores.md).

-   Review the external questionnaire responses and supporting documents.

    Navigate to the Due diligence request record page by selecting the DDR number and then selecting the External assessment \(VRA\) number on the **External assessments** tab. For more information, see [Third-party \(external\) risk assessment management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-extrnl-assessment.md).

-   Access the approval request record page.

    Select one of the Requested states from the list to open the approval request record page. From this page, you can select **Approve** or **Reject**. For more information, see [Approval process management](../../grc-workspace-vrm/reference/tprm-ws-dd-mgt-pg-approvals.md).


If the responses meet your requirements, one or more approvers approves the request, and the owner \(TPR manager or TPR assessor\) closes the due diligence request and the engagement. The third party or engagement state is now **Active**. If a contract is going to be prepared, an approver, TPR manager, or owner selects **Send to contract negotiator** and assigns a contract negotiator. The approved due diligence request's state is updated to the Contract Risk Process state and the contract risk negotiator is notified through an automated email.

For more information, see [Managing the contract risk process](tprm-ws-contract-risk-process.md).

## Rejecting due diligence requests

If an issue can't be resolved or the due diligence request is canceled, the approver can enter comments and reject the due diligence request. To view your **My approvals**, navigate to the task page, select **My approvals**, and then select a Requested state from the list to open the approval request record page. From this page, you can select **Reject** to reject the request.

After the due diligence request is rejected, the following actions occur:

1.  The due-diligence request's state is updated from Awaiting approval to Rejected.
2.  You must enter an explanation for rejecting the due diligence request in the **Comments** field.
3.  The Due diligence process state is updated to Rejected and all stakeholders are notified that the engagement has been rejected.

**Note:** The owner can reopen the approval process by selecting the due diligence request from the All request list. The owner is required to provide a justification for restarting the approval process.

