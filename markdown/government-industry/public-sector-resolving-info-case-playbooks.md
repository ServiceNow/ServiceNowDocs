---
title: Resolving an information request case using the Information Request Playbook
description: You can use playbooks to create cases and to complete the tasks and activities that are needed to resolve specific types of cases.Complete the Intake stage as your first step in resolving a case using the Information Request Playbook.Complete the Review stage as your second step in resolving a case using the Information Request Playbook.Complete the Process stage as your third step in resolving a case using the Information Request Playbook.Complete the Decision stage as your last step in resolving a case using the Information Request Playbook.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Using Information Request Playbook, Playbooks, Use, Public Sector Digital Services \(PSDS\)]
---

# Resolving an information request case using the Information Request Playbook

You can use playbooks to create cases and to complete the tasks and activities that are needed to resolve specific types of cases.

**Note:** Verify that the Information Request Playbook application, which is separate from the Public Sector Digital Services Core application, has been installed and configured. For instructions, see [Install and configure the Information Request Playbook application](configuring-information-request-playbook.md).

By default, the following stages are available to you as an information request case agent in the Information Request Playbook in the CSM Configurable Workspace.

-   Intake
-   Review
-   Processing
-   Decision

## Stages in an Information Request Playbook

The Information Request Playbook experience starts with the Intake stage. This stage is the default playbook stage for a new information request case. Use this playbook stage to gather information about the requester, the documents being requested, and any exemption categories that the request falls into. You can also request additional information from the requester.

The playbook continues with the Review stage. In this stage, you can do the initial troubleshooting on the case, evaluate similar or duplicate requests, and determine whether the information requested can be released and if a fee needs to be charged. You can move the case to the next stage when the requester accepts the fee, or if a fee waiver is submitted and approved.

The playbook continues with the Process stage. In this stage, you can assess resources, request a fee approval, create case tasks, and add or request new information before the case resolution begins. The case status changes to Work in Progress once the fee payment is processed or waived. The case is then sent for legal review. After legal review is complete, the case is moved to the Decision stage. You may solicit additional information from the requester at any time during this stage.

The final stage of the Information Request Playbook is the Decision stage. At the Decision stage, the status of the case is updated from Review in Progress to Ready for Decision after the case has passed legal review. A notification is sent to the requester that lets them know that case approval has been has obtained and the requested documents have been uploaded. The requester can then either accept or reject the document. If the requester accepts the documents, the case is automatically closed. If the requester rejects the solution, the case is reopened, and the agent must propose another outcome.

## Complete the Intake stage in Information Request Playbook

Complete the Intake stage as your first step in resolving a case using the Information Request Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  In the CSM Configurable Workspace, navigate to **Lists** &gt; **Information Requests** &gt; **All**.

2.  Select **New**.

    The Information Request Playbook opens and initiates the first activity for collecting the request details.

3.  On the Enter Request Details activity card, fill in the information.

4.  Select **Save**.

    A case is created with the information request information. The case number is added to the tab and the first activity in the Intake stage is marked as complete. The second activity in this stage is highlighted as the current activity. If you have enabled the Similar Request documents UI activity, this will display as the second activity. For more information, see [Configure Similar Request Documents UI in Information Request Playbook](../task/psds-ir-playbooks-configure-similar-request-documents.md).

5.  Select a related document to link it to the request, and select **Next**.

6.  Review the details of the case and make updates if needed.

7.  Select **Submit**.

8.  Select **Assign to me**.

9.  Select **Move to review**.

    The Intake stage is now complete and the case is moved to the Review stage.


## Complete the Review stage in Information Request Playbook

Complete the Review stage as your second step in resolving a case using the Information Request Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Review the files attached to the case, and confirm that the requester has included the required documents to validate their identity by selecting the boxes associated with the document type.

2.  Select **Mark as Complete**.

3.  Select any exemptions that apply to the case, and select **Mark as Complete**.

    If no exemptions apply to the case, select **No exemption code\(s\) applicable**.

4.  Do one of the following actions depending on whether you have similar or linked completed requests.

    |Options|Steps|
    |-------|-----|
    |**If there are no similar or linked completed requests**|Select **Mark as Complete**.|
    |**If there are similar or linked completed requests**|Review them to see if any are relevant to the current request.|

5.  Estimate the fees associated with this request by using the fee estimator.

    The fee estimator can only be run once.

6.  Enter details on the fee estimate in the work notes, then select **Request Fee Approval**.

    If the requester qualifies for a fee waiver, enter that information here. The fee estimate is now sent to billing to be approved. Once the fee estimate has been approved, mark the step as complete.

7.  Select **Send for Requester Approval** to send the fee estimate to the requester.

    This activity will automatically be marked complete once the requester has approved the fee, and the case will be moved to the Process Payment activity.

8.  Verify the payment has been sent, and select **Move to Process**.

    The Review stage is now complete and the case is moved to the Process stage.


## Complete the Process stage in Information Request Playbook

Complete the Process stage as your third step in resolving a case using the Information Request Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Upload the documents needed to fill this request by selecting **New Document** or **Link Document**.

2.  Move to the next activity by selecting **Prepare for Review**.

3.  Enter any additional work notes or details needed for legal review, and then select **Send for Legal Review**.

    A case task is now created and assigned to the Legal Review assignment group for approval. If the uploaded documents are rejected during the legal review, you may need to make changes and request a review again or move the case directly to the Decision stage.

4.  After the legal review is complete, select **Mark as Complete**.

    The case is moved to the Final Review Pre-release activity, where the documents and details of the request are reviewed by the Final Review Team assignment group.

5.  After the documents have been approved by the Final Review Team, select **Move to Decision**.

    The Process stage is complete and the case is moved to the Decision stage.


## Complete the Decision stage in Information Request Playbook

Complete the Decision stage as your last step in resolving a case using the Information Request Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Enter any work notes for the customer or other users on the case watch-list, and then select **Release** to release the information to the requester.

2.  If the requester has opted to be notified by mail, in the work notes, verify that the notice has been sent by mail and select **Mark as Complete**.

3.  If the requester has opted to be notified by phone, in the work notes, verify that the notice has been sent by phone and select **Mark as Complete**.

4.  Review the resolution code and resolution notes, and select **Propose solution**.

    All case tasks must be closed before an agent can propose a solution to the case.

    A notification is sent to the constituent that lets them know that the request is completed. The constituent can either accept or reject the proposal. If the constituent accepts the proposal, the case is automatically closed. If the constituent rejects the solution, the case is reopened, and the agent must propose another outcome.


