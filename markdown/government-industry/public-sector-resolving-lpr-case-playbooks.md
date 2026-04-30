---
title: Resolving a license and permit case using License and Permit Playbook
description: You can use playbooks to create cases and to complete the tasks and activities that are needed to resolve specific types of cases.Complete the Intake stage as your first step in resolving a case using the License and Permit Playbook.Complete the Review stage as your second step in resolving a case using the License and Permit Playbook.Complete the Process stage as your third step in resolving a case using the License and Permit Playbook.Complete the Decision stage as your last step in resolving a case using the License and Permit Playbook.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Using License and Permit Playbook, Using Playbooks, Using Public Sector Digital Services, Public Sector Digital Services \(PSDS\)]
---

# Resolving a license and permit case using License and Permit Playbook

You can use playbooks to create cases and to complete the tasks and activities that are needed to resolve specific types of cases.

**Note:** Verify that the License and Permit Playbook application, which is separate from the Public Sector Digital Services Core application, has been installed and configured. For instructions, see [Install and configure the License and Permit Playbook application](configuring-license-permit-playbook.md).

By default, the following stages are available to you as a government service agent in the License and Permit Playbook in the CSM Configurable Workspace.

-   Intake
-   Review
-   Processing
-   Decision

## Case Stages in License and Permit Playbook

The License and Permit Playbook experience starts with the **Intake** stage. This stage is the default playbook stage for a new license and permit request case.

Use this playbook stage to gather and confirm information about the requester, the license or permit being requested, whether the requester is eligible for this type of license or permit, and whether they are exempt from the fees associated with the license or permit. You can also request additional information from the requester at this stage, upload additional documents, add additional comments, add related parties, and schedule a consultation through the work notes.

If the case was submitted by a constituent through the Government Service Portal, the constituent will be able to upload documents, and review the fees and disclaimers associated with the license or permit application before the case continues. At the end of the Intake stage, agents must enter details about the payment that was processed or waived.

The playbook continues with the **Review** stage. In this stage, you can do the initial troubleshooting on the case, verify supporting documents and credentials, and set up any inspections needed for license or permit approval. You can move the case to the next stage when details are provided in the work notes on the inspections \(open work orders or work performed during\) or verifying documents.

The playbook continues with the **Process** stage. In this stage, the case might be routed to a higher-tier agent, who can assess the entire request for the license or permit, approve a fee exemption, create case tasks, request or perform additional inspections, and add or request additional information.

Once requests for any additional information and any open case tasks are complete, the case is moved to the **Propose Decision** activity. Additional information may be solicited from the requester at any time during this stage. After the decision, often made by a higher-tier agent, is proposed, it is routed to the original agent, who may request or perform their own additional inspections, and add or request more information. This agent then has the option of confirming or vetoing the decision proposal of the other agent.

The final stage of the License and Permit Playbook is the **Decision** stage. At the Decision stage, the status of the license or permit is changed to **Granted**, and the license or permit can be generated and routed to the constituent. A notification is sent to the requester that lets them know that license or permit approval has been has obtained and the requested license or permit has been digitally generated within the playbook, and delivered via the Government Service Portal.

The requester can then either accept or reject the license or permit. If the requester accepts the outcome, the case is automatically closed. If the requester rejects the solution, the case is reopened, and the agent must propose another outcome. A request for a license or permit may also be conditionally approved, or denied. The agent can specify why in the work notes.

## Complete the Intake stage in License and Permit Playbook

Complete the Intake stage as your first step in resolving a case using the License and Permit Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  In the CSM Configurable Workspace, navigate to **Lists** &gt; **License &amp; Permit Requests** &gt; **All**.

2.  Select **New** to create a case.

3.  Select **General License/Permit** under the Service dropdown, and **New License/Permit Request** under the Case Type dropdown.

4.  Select **Create Case**.

    The License and Permit Playbook opens and initiates the first activity for collecting the request details.

5.  On the Enter Application Details activity card, confirm the applicant's eligibility and select **Continue**.

6.  On the form, fill in the fields with the requester's contact information and details of the request.

7.  Under Representation, select the checkbox for **Requesting on behalf of someone else**.

8.  Enter the name of the constituent or business that the requester is submitting the application on behalf of, and select **Save**.

    **Note:** All license/permit co-applicants must have a business contact account associated with your business to be included on a license/permit application. Each contact can create an account by registering on the Government Service Portal, or a government service agent can create a business contact record for them. For information on how agents can create a business contact record from information entered in a License and Permit application, see [Create a business contact account from license or permit application data](../task/psds-multi-party-create-business-contact.md).

9.  Select any add-ons, such as permit endorsements.

    You may add more than one. The pricing of the license or permit varies with each selection or combination of selections.

10. Review the fees associated with the requester's choices.

    The fee total changes dynamically based on the options selected. If the constituent or requester is fee exempt, select the **Fee Waiver** checkbox and enter a justification to claim an exemption for them.

11. Select **Submit** to move to the next activity.

12. Add any additional related parties.

    Related parties may include business partners, managers, or any business contact who may need access to this license/permit. They must be contacts already registered on the Government Service Portal and associated with your business.

13. Select **Mark Complete** to move to the **Upload Documents** activity.

14. Upload any documents that verifies the identity of the requester and the related party, or provides additional context for your request.

    A case is created with the license or permit request information and all related parties, and is now routed to the constituent via the Government Service Portal, where they can upload any applicable identity documents, credentials, or supporting documentation required for this license/permit request. The case continues once the constituent has uploaded these documents. Required documentation varies by request.

15. Once the constituent has uploaded supporting documentation, review the attachment\(s\) and select **Mark Complete** to move to the **Review Fees &amp; Disclaimer** activity.

    The case is again routed to the constituent via the Government Service Portal, where they can upload fee waiver justification documents, if applicable, or other supporting documentation required for this license/permit request. The case continues once the constituent has uploaded these documents and acknowledged the fees and disclaimers.

16. Once the constituent has acknowledged the fees and disclaimers, the case is moved to the queue, where it can be picked up by another agent in your agency, who will review the request and provide appointment options for the license or permit consultation.

17. Select **Mark Complete** to acknowledge that you have reviewed the request.

18. Enter available times in the work notes.

19. Select **Schedule Consultation**

    The case is again routed to the constituent via the Government Service Portal, where they can accept or reject the times proposed for an interview consultation or inspection.

20. After the consultation, enter any relevant notes about the case in the work notes and select **Mark Complete** to move to the next activity.

21. Payment.

22. Select **Move to Review**.

    The case is moved to the **Review** stage, and the **Intake** stage is marked complete.


## Complete the Review stage in License and Permit Playbook

Complete the Review stage as your second step in resolving a case using the License and Permit Playbook.

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


## Complete the Process stage in License and Permit Playbook

Complete the Process stage as your third step in resolving a case using the License and Permit Playbook.

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


## Complete the Decision stage in License and Permit Playbook

Complete the Decision stage as your last step in resolving a case using the License and Permit Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Enter any work notes for the customer or other users on the case watch-list, and then select **Release** to release the information to the requester.

2.  If the requester has opted to be notified by mail, in the work notes, verify that the notice has been sent by mail and select **Mark as Complete**.

3.  If the requester has opted to be notified by phone, in the work notes, verify that the notice has been sent by phone and select **Mark as Complete**.

4.  Review the resolution code and resolution notes, and select **Propose solution**.

    All case tasks must be closed before an agent can propose a solution to the case.

    A notification is sent to the constituent that lets them know that the request is completed. The constituent can either accept or reject the proposal. If the constituent accepts the proposal, the case is automatically closed. If the constituent rejects the solution, the case is reopened, and the agent must propose another outcome.


