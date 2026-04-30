---
title: Approval process management
description: You can view the list of users who can approve or reject a DD request and also view the details of their approval actions. In addition, you can view the approval levels for a request.
locale: en-US
release: zurich
product: Third-party Risk Management
classification: third-party-risk-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Reference, Third-party Risk Management, Governance, Risk, and Compliance]
---

# Approval process management

You can view the list of users who can approve or reject a DD request and also view the details of their approval actions. In addition, you can view the approval levels for a request.

## Approval process

During the approval process, each aspect of risk is analyzed by the appropriate internal stakeholders. All internal stakeholders \(approvers\) review the questionnaire responses and supporting documents from the third-party and engagement contacts. If the responses are good, one or more approvers approves and then closes the DD request. If a contract will be prepared, the approved request moves to the Contract Risk process.

## Accessing the Due diligence management page

You can access the Due diligence management page from many locations by selecting the **DDR** number for any DD request. Select either the **Approvers** tab or the **Approval levels** tab.

## Approvers tab

The tab lists the users that have responded to the engagement request. Select the **State** value to view the details of the approval action that the approver performed.

The state of the approval can be one of the following values:

-   Not yet requested
-   Requested
-   Approved
-   Rejected
-   Cancelled
-   No longer required

![Accessing the Approvers tab.](../image/tprm-ws-dd-mgt-approvers-tab.png)

Select the **State** value for a request to view the **Details** tab for the request.

![Viewing the details of an approval.](../image/tprm-ws-dd-mgt-apprvl-details-tab.png)

## Approval levels tab

![Viewing approval levels.](../image/tprm-ws-dd-mgt-approval-levels-tab.png)

**Note:** For more information on how Third-party risk \(TPR\) admins can set approval levels and rules, see [Set up the approval levels for due diligence requests](../task/tprm-set-request-approval-levels.md) and [Set up the approval rules for due diligence requests](../task/tprm-set-request-approval-rules.md).

## Approval business rules

If you have the TPR admin \[sn\_vdr\_risk\_asmt.vendor\_risk\_admin\] role, you can view all business rules by navigating to **All** &gt; **System Definition** &gt; **Business Rules**.

The following business rules are included when the Third-party Risk Due Diligence \[sn\_tprm\_dd\] application is activated.

|Business rule|Source table|Description|
|-------------|------------|-----------|
|Create approval records|Third-party due diligence request \[sn\_tprm\_dd\_request\]|Creates approval records for the evaluated approvers, setting the first record to **Requested** and subsequent records to **Not yet requested** when the due diligence request state updates to **Awaiting for approval**.|
|Roll up approval and update DD|Approval \[sn\_tprm\_approval\]|Marks next approval record as **Requested** if multiple approvals are required. If all required approval records are approved, then the due diligence record state is updated to **Approved**.|
|Cancel existing approvals|Third-party due diligence request \[sn\_tprm\_dd\_request\]|Cancels approval requests if the state of the approval record is updated to **No longer required**.|

-   **[Approval rule form](tprm-ar-form.md)**  
The approval rule form captures all the information needed to create an approval rule. An admin or third-party risk admin can create an approval rule.

**Parent Topic:**[Third-party Risk Management reference](../../grc-vendor-risk/concept/tprm-reference.md)

**Related topics**  


[Approving or rejecting requests for due diligence](../../grc-vendor-risk/concept/tprm-approving.md)

[Set up the approval levels for due diligence requests](../task/tprm-set-request-approval-levels.md)

[Set up the approval rules for due diligence requests](../task/tprm-set-request-approval-rules.md)

[Approval rule form](tprm-ar-form.md)

