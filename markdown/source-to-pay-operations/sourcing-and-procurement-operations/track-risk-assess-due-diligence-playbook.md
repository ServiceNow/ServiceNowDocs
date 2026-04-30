---
title: Track risk assessments from the due diligence playbook
description: As procurement specialists, use the due diligence playbook to track supplier risk assessments and complete the associated tasks.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Streamlining the supplier risk assessment workflow, Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace, Using Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Track risk assessments from the due diligence playbook

As procurement specialists, use the due diligence playbook to track supplier risk assessments and complete the associated tasks.

## Before you begin

Role required: Procurement specialist

## About this task

When a sourcing request is added to a sourcing event, in the Qualification needed state, a supplier case of type due diligence is triggered to address risk assessments. You can choose to close the case through the playbook if there are duplicate requests. In case of no duplicates, a new due diligence is initiated through the playbook. The same Third-Party Risk Management \(TPRM\) record producer is used here. You are notified at each step in the TPRM workflow, such as inherent risk assessment, third-party risk assessment, and so on. You can review the risk rating after the due diligence is complete. Now, you can either accept or reject the risk rating, and take necessary actions based on this decision. Select **Mark Complete** to close the due diligence case.

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select **All work** &gt; **Cases**.

3.  Select the Due Diligence procurement case from the list for further processing.

    The **Playbook** tab opens with the **Assign case** section.

4.  Complete the steps in the various stages and activities of the Create a Due Diligence Request playbook.

<table id="table_bgd_tzx_ztb"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td rowspan="2">

Review case

</td><td>

Assign case

</td><td>

Use this activity to assign the case to a different person or keep the case assigned to you.You can do the following:

 -   In the **Assigned to** search field, search for and select the person that you want to assign the case to.
-   In the **Short description** field, update the description for the case.
-   Select one of the following actions:
    -   Select **Save** to save your changes.
    -   Select **Start work** to start working on the case.


</td></tr><tr><td>

Update case to work in progress

</td><td>

This activity updates the case to Work in progress and completes automatically.

</td></tr><tr><td rowspan="5">

Create Request

</td><td>

Review the Supplier details

</td><td>

Review the supplier details and select **Continue**.

</td></tr><tr><td>

Check for duplicate Due Diligence Requests

</td><td>

Checks for duplicate due diligence requests. If there aren't any duplicate requests, select **Create new request**.

</td></tr><tr><td>

Create Due Diligence Request

</td><td>

Request third-party risk due diligence by selecting one of the following options:-   Onboard a new engagement
-   Reassess an existing engagement
-   Reassess an existing engagement for contract renewal
-   Offboard an engagement with due diligence
-   Offboard an engagement with NO due diligence
Add any relevant attachments, if required, and select **Submit**.

The relevant third party, if available, is automatically populated.

If the third party is not listed here or incomplete information is provided, enter the following details:

-   Third-party information
-   Engagement information
-   Third-party address
-   Engagement address
-   Third-party primary contact
-   Engagement primary contact


</td></tr><tr><td>

Update PC Record with the DDR case

</td><td>

Updates the procurement case record with the due diligence request case.A due diligence case is created for the supplier. After that, the created case record ID gets populated in the **Related DDR** field under the **Details** tab.

</td></tr><tr><td>

Wait for risk process to start

</td><td>

Wait for the inherent risk assessment to complete.

At this point, the TPRM team starts onboarding the supplier associated with the created DDR.

</td></tr><tr><td rowspan="6">

Assess Risk

</td><td>

Wait for the Inherent Risk Assessment

</td><td>

Wait for the inherent risk assessment to complete.

Here, the assigned respondent completes and submits the inherent risk questionnaire, and the TPRM team updates the INA record and sets it to Closed state. Details of the INA record are provided in parallel in the playbook.

</td></tr><tr><td>

Notify requestor on the Inherent Risk Assessment

</td><td>

A notification is sent to you with the information that the inherent risk assessment is now complete.

</td></tr><tr><td>

Wait for the Third-Party Risk Assessments

</td><td>

Wait for the third-party risk assessments to complete.

Here, the TPRM team starts the due diligence for the supplier associated with the created DDR. Details of the third-party risk assessments for the third party and the engagement are provided in parallel in the playbook.

</td></tr><tr><td>

Notify requestor on the Third-Party Risk Assessment

</td><td>

A notification is sent to the requester when both these risk assessments are completed and in the Closed state.

</td></tr><tr><td>

Check for the status of the Due Diligence approval process

</td><td>

Review the status of the entire due diligence approval process.At this point, the TPRM team moves the DDR to the TPRM approved state. A notification is sent to you with the information that the due diligence request has been approved by the TPRM team. The risk ratings from all the above assessments are now displayed in the playbook.

**Note:** At any point during the above TPRM activities, if the record gets rejected, then a notification is sent to you regarding this rejection, and the case is moved to Closed rejected.

</td></tr><tr><td>

Notify requester that the request has been approved.

</td><td>

The requester is notified when the DD Request is approved by TPRM team.

</td></tr><tr><td>

Review Risk Rating

</td><td>

Accept or reject risk rating

</td><td>

Do one of the following:-   Select **Reject Risk Rating**, notify the requester that the request has been rejected, and mark the case as Rejected.
-   Select **Accept Risk Rating**, notify the supplier, and mark the case as Complete.


</td></tr><tr><td rowspan="4">

Close case

</td><td>

Get Supplier contact email from DDR record

</td><td>

Gets the email ID of the supplier contact from the due diligence request record.

</td></tr><tr><td>

Notify Supplier

</td><td>

Use this activity to email the supplier about the status of the due diligence request.

 A draft email appears with pre-populated data in the **Subject** field. The email body is pre-populated with the relevant text.

 Select one of the following actions:

 -   **Send Email**: Sends the email instantly.
-   **Skip**: Skips this activity and moves to the next activity.


</td></tr><tr><td>

Complete case

</td><td>

Use this activity to add work notes and close the case.

 Do the following:

-   In the **Work notes** field, add any comments about the case.
-   In the **Close notes** field, add any closing comments.
-   Select **Complete case**.


</td></tr><tr><td>

Update case to complete

</td><td>

Updates the case to Closed Completed.

</td></tr></tbody>
</table>
**Parent Topic:**[Streamlining the supplier risk assessment workflow](../concept/simplify-risk-assessment-wf.md)

