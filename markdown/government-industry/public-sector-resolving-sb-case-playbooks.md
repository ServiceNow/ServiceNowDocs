---
title: Resolving a social benefits case using Social Benefits Playbook
description: You can use playbooks to create cases and to complete the tasks and activities that are needed to resolve specific types of cases.Complete the Intake stage as your first step in resolving a case using the Social Benefits Playbook.Complete the Review stage as your second step in resolving a case using the Social Benefits Playbook.Complete the Process stage as your third step in resolving a case using the Social Benefits Playbook.Complete the Decision stage as your last step in resolving a case using the Social Benefits Playbook.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Using Social Benefits Playbook, Playbooks, Use, Public Sector Digital Services \(PSDS\)]
---

# Resolving a social benefits case using Social Benefits Playbook

You can use playbooks to create cases and to complete the tasks and activities that are needed to resolve specific types of cases.

**Note:** Verify that the Social Benefits Playbook application, which is separate from the Public Sector Digital Services Core application, has been installed and configured. For instructions, see [Install and configure the Social Benefits Playbook application](configuring-social-benefit-playbook.md).

By default, the following stages are available to you as a government service agent in the Social Benefits Playbook in the CSM Configurable Workspace.

-   Intake
-   Review
-   Processing
-   Decision

## Case Stages in Social Benefits Playbook

The Social Benefits Playbook experience starts with the **Intake** stage. This stage is the default playbook stage for a new social benefits request case.

Use this playbook stage to gather and confirm information about the applicant, the social benefit program being applied for, and whether the applicant is eligible for this type of social benefit program. You can also request additional information from the applicant at this stage, upload additional documents, add additional beneficiaries, and schedule a interview, if needed.

If the case was submitted by a constituent through the Government Service Portal, the constituent will be able to upload documents, review proposed benefits, and respond to interview requests before the case continues. At the end of the Intake stage, agents must review and verify the information provided before proceeding.

The playbook continues with the **Review** stage. In this stage, agents must review and verify the information provided, verify supporting documents and credentials \(and flag any for follow-up\), check for duplicate requests, and set up any interviews needed for social benefit program approval. You can move the case to the next stage when all documents have been verified and there are no pending case tasks.

The playbook continues with the **Process** stage. In this stage, the agent proposes their decision. The case might then be routed to a higher-tier agent, who can assess the entire application, create any additional case tasks, request or perform additional interviews, add or request additional information, or simply approve or deny based on the information provided. Once requests for any additional information and any open case tasks are complete and all agents have reached a decision, the case is moved to the **Decision** stage.

The final stage of the Social Benefits Playbook is the **Decision** stage, where the status of the decision is relayed to the constituent. The status of the social benefit application is changed to **Granted**, and the social benefit program can be routed to the constituent. A notification is sent to the applicant via the Government Service Portal, letting them know that their application has been has approved.

## Complete the Intake stage in Social Benefits Playbook

Complete the Intake stage as your first step in resolving a case using the Social Benefits Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  In the CSM Configurable Workspace, navigate to **Lists** &gt; **Social Benefits** &gt; **All**.

2.  Select **New** to create a case.

3.  Select **Create Case**.

    The Social Benefits Playbook opens and initiates the first activity for collecting the request details and determining eligibility for the social benefits offered by your agency.

4.  On the Answer eligibility questions activity card, confirm the applicant's eligibility using the eligibility questions, and select **Check Eligibility**.

    The benefits card will display possible eligibility for each of the social benefits offered by the agency. An agent can review the details of the case to make a final determination.

5.  If the applicant is eligible for the benefit associated with the application currently open, select **Start Application**.

    If the applicant is not eligible for the benefit associated with the application currently open, the application cannot move forward. The benefits card displays other social benefit programs the applicant may be eligible for, in addition to or instead of the benefit associated with the application currently open.

6.  On the form, fill in the fields with the primary applicant's personal and financial information, including SSN, demographic information, location, and contact information.

7.  Select the checkbox if the customer has indicated that they would prefer to be contacted via SMS.

8.  Select **Mark Complete** to continue to the next activity.

9.  Add any people who would also be receiving benefits along with the primary applicant.

    You may add more than one. Related people may include spouses, dependents, children, household members, or any person who may be receiving benefits along with the primary applicant.

10. Select **Mark Complete** to move to the next activity.

11. If anyone in the applicant's household has a source of income, select **Yes**, and on the form, fill in the fields.

    If no one in the applicant's household has a source of income, select **No**.

12. If anyone in the applicant's household has any pre-tax contributions on any of their current income, select **Yes**, and enter any pre-tax contributions that affect income for the applicant's household.

    If no one in the applicant's household has any pre-tax contributions, select **No**.

13. Select **Mark Complete** to move to the next activity.

14. If anyone in the applicant's household has any expenses or financial commitments, select **Yes**.

    If no one in the applicant's household has any expenses or financial commitments, select **No**

15. On the form, fill in the fields, doing so for each expense item.

    You may add more than one. Select **Add Item** to add multiple expenses to the list.

16. Select **Mark Complete** to move to the next activity.

17. If anyone in the applicant's household has any financial accounts, assets, or resources, select **Yes**, and on the form, fill in the fields.

    You may add more than one. Select **Add Item** to add multiple expenses to the list. If no one in the applicant's household has any financial accounts, assets, or resources, select **No**.

18. Select **Mark Complete** to move to the next activity.

19. Upload any supporting documents that verify the identity of the applicant and any related parties, or provide additional context for their request.

    A case is created with the information the agent has provided on the applicant thus far, and is now routed back to the applicant via the Government Service Portal. There, they can upload any applicable identity documents, credentials, or supporting documentation required for their application. The case continues once the applicant has uploaded these documents. Required documentation varies by request.

20. Once the applicant has uploaded supporting documentation via the Government Service Portal, review the attachment\(s\) and select **Mark Complete** to move to the next activity.

21. On the form, select the options that best describe the applicant's criminal history, communication preferences, and accessibility needs.

22. Select **Mark Complete** to move to the next activity.

23. Review the application in its entirety and correct any errors before submitting the application.

24. Select **Request Signature** to request a signature from the constituent via the **Sign and Submit** activity on the Government Service Portal.

    If the constituent does not respond, you may move this application directly to the **Decision** stage, where the case can be closed.

    Once the constituent has completed the **Sign and Submit** activity via the Government Service Portal, the case is automatically moved to the next activity.

25. Select **Apply Now** to use information from the current application to apply for other social benefits programs that the applicant may be eligible for.

    You may apply for more than one. Each new application opens in a new browser tab. The option to create an appended case expires after a specified amount of time.

    A child Social Benefits case is appended to the case of the original benefit application, and the benefit card updates based on the status of the new application.

26. Select **Skip** to skip this activity.

    The case state of the additional benefit application changes to "Not submitted". A new case can no longer be created and appended to the primary application.

27. Select **Mark Complete** once the desired applications are submitted.

    The case is moved to the **Review** stage, and the **Intake** stage is marked complete.


## Complete the Review stage in Social Benefits Playbook

Complete the Review stage as your second step in resolving a case using the Social Benefits Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Review the information collected during the intake stage, and confirm that the information is complete and correct.

    If the agent is selecting the case from an unassigned queue, they will see the option to **Assign to Me**. If the case is auto-assigned, they will see the option to **Mark Complete**.

2.  Correct any errors before submitting the application, and select **Mark Complete**.

    Select the pencil icon to navigate back to an Intake stage activity that needs to be corrected.

3.  Verify there are no duplicate benefit applications for the primary applicant, and select **Mark Complete**.

4.  Review and verify the files and supporting documentation attached to the application.

    Here, you can flag documents for further verification, request additional documents, or close the case by moving it directly to Decision.

5.  Select **Mark as Complete** once all documents have been verified and any flagged documents have been resolved.

6.  Select a date and time in the dropdown menu to recommend an interview slot if an interview is required to process the application, and select **Request Interview**

    The interview is now routed to the applicant, who can accept, reject, or respond to the interview request via the Government Service Portal. The case continues once the applicant has responded to the request. If an interview is not required, select **Skip**.

7.  Select **Move to Process** once the interview is complete.


### Result

The case is now moved to the **Process** stage.

## Complete the Process stage in Social Benefits Playbook

Complete the Process stage as your third step in resolving a case using the Social Benefits Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Review the auto-calculated eligibility assessment and the benefit summary card, which uses application information as an input to provide guidance on the benefit amount for which an applicant may qualify.

    This engine utilizes information such as the total household income, assets owned, expenses, etc. as inputs into the calculation.

2.  Select **Grant** or **Deny** in the Proposed Decision dropdown to propose a decision for the applicant's social benefits case.

3.  Enter a justification for the proposed decision in the description box, then select **Propose Decision**.

    The case is now routed to an approval agent. The Process stage will complete automatically once the decision is approved.


### Result

The Process stage is complete and the case is moved to the Decision stage.

## Complete the Decision stage in Social Benefits Playbook

Complete the Decision stage as your last step in resolving a case using the Social Benefits Playbook.

### Before you begin

Role required: sn\_gsm.constituent\_agent, sn\_gsm.relationship\_agent, sn\_gsm.government\_service\_manager, sn\_gsm.business\_agent, sn\_gsm.agency\_constituent\_agent, sn\_gsm.agency\_manager, sn\_gsm.agency\_agent

### Procedure

1.  Enter the resolution code and cause.

2.  Enter resolution notes outlining the case decision for the applicant, or other users on the case watch-list.

3.  Select the checkbox for **Add resolution notes to comments** if these notes are to be shown to the applicant.

4.  Select **Close** to close and resolve the case.

    A notification is sent to the applicant that lets them know that the request is completed.


