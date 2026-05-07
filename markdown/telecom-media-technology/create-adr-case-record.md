---
title: Create an Alternative Dispute Resolution case
description: Create an Alternative Dispute Resolution \(ADR\) case record in the CSM/FSm Configurable Workspace so that you can investigate and resolve an escalated complaint.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [ADR, Use, Customer Service Problem Management, Telecommunications, Media, and Technology \(TMT\)]
---

# Create an Alternative Dispute Resolution case

Create an Alternative Dispute Resolution \(ADR\) case record in the CSM/FSm Configurable Workspace so that you can investigate and resolve an escalated complaint.

## About this task

At the initial stage, you capture the complaint initiator details and complaint details. Throughout the investigation, all relevant interactions, updates, and findings are captured within the ADR case record. After completion of the review, you propose the resolution with the customer. If the customer accepts the resolution, close the case accordingly. If the customer doesn't accept the resolution, generate and issue a deadlock letter to conclude the internal complaint process formally. The ADR case record details are captured in the ADR Complaint \[sn\_telco\_adr\_mgmt\_complaint\] table.

## Before you begin

Role required: sn\_telco\_adr\_mgmt\_manager

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **CSM/FSM Configurable Workspace**.

2.  Select the list \(![ListIcon.](../image/Lists.png)\) icon.

3.  Navigate to **Alternative Dispute Resolution** &gt; **All**.

4.  Select **New**.

5.  On Intake stage, do the following.

    1.  On the Capture initiator details form, fill in the fields.

        You can submit the details of the initiator of the complaint in the Capture initiator details form. To learn more about field information, see [Capture initiator details form](../reference/capture-initiator-details-form.md).

    2.  Select **Continue**.

    3.  On the Capture ADR information form, fill in the fields.

        You can submit the details of your complaint in the Capture ADR information form. To learn more about field information, see [Capture ADR information form](../reference/capture-adr-information-form.md).

    4.  Select **Mark Complete**.

    5.  On the Upload documents view, select **Add file** to add any attachments such as any evidence related your issue.

    6.  Select **Continue**.

        An email is sent to the customers. You can view the email details on the Notify customer activity view.

6.  On Investigate stage, do the following.

    1.  On the Lookup record history view, under the Relevant record section, select **Link this record** on the record tile that you want to link with the complaint.

        Relevant records that match with the complaint's short description. It displays the five relevant records. You can also select the search \(\) icon to find more records that are relevant to the complaint.

        **Note:** If you’re using the Now Assist for TMT, you can see the requester's sentiments on a case record. To learn more, see [Analyze the sentiment of a service problem case using Now Assist for TMT](now-assist-tmt-analyze-sentiment-spc-adr.md).

        The selected records appear under the Current Linked section.

    2.  To unlink the record, select **Unlink this record**.

        The unlinked records don't appear on the Relevant records section again.

    3.  Select **Continue**.

    4.  On the Analyze linked facts card, enter your findings in the **Key findings** field.

        **Note:** If you’re using the Now Assist for TMT application, you can generate the comprehensive summary of the linked records. To learn more, see [Summarize the linked records using Now Assist for Telecommunications, Media and Technology \(TMT\)](now-assist-tmt-summarize-linked-record.md).

    5.  Select **Continue**.

7.  On the Resolution stage, do the following.

    1.  On the Propose resolution plan form, fill in the fields.

<table id="table_ad2_2qp_h3c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Resolution code

</td><td>

Type of proposed resolution to identify the solution.

</td></tr><tr><td>

Add resolution notes to comments

</td><td>

Select this option to add the resolution notes to the ADR case activity stream. Selecting this check box makes the resolution notes available to anyone who can view the ADR activity stream.

</td></tr><tr><td>

Resolution notes

</td><td>

Detailed summary to resolve the complaint.**Note:** If you’re using the Now Assist for TMT application, you can generate the resolution notes using the Now Assist component. To learn more, see [Generate resolution notes for Alternative Dispute Resolution case using Now Assist for TMT](now-assist-tmt-generate-resolution-notes-ad.md).

</td></tr></tbody>
</table>    2.  Select **Propose resolution**.

        An email with the details of the key findings and resolution notes is sent to the customer.

    3.  On the Resolution feedback form, add the feedback from the customer in the **Resolution notes** field.

    4.  Select one of the UI actions based on the customer feedback and do the following.

<table id="table_whw_xqp_h3c"><thead><tr><th>

UI action

</th><th>

Steps

</th></tr></thead><tbody><tr><td>

**Customer accepted**

</td><td>

The Outcome stage appears.1.  On the Implement resolution card, select **Create task**.

**Note:** You can create multiple case tasks depends on the resolution plan.

2.  Execute and close the tasks.

The **Continue** button appears.

3.  Select **Continue**.


</td></tr><tr><td>

**Customer rejected**

</td><td>

1.  On the Generate deadlock letter card, add the details in the **Customer correspondence content** field.

**Note:** If you’re using the Now Assist for TMT application, you can generate the deadlock letter details using the Now Assist component. To learn more, see [Generate a deadlock letter using Now Assist for TMT](now-assist-tmt-generate-deadlock-letter.md).

2.  Select **Generate and send**.

A deadlock letter is generated in PDF format and sent to the customer via an email.

</td></tr></tbody>
</table>8.  On the Closure stage, Select **Close complete**.


**Parent Topic:**[Using alternative dispute resolution case](../concept/use-alternative-dispute-resolution-case.md)

**Related topics**  


[View an Alternative Dispute Resolution case record](view-adr-case.md)

[Alternative dispute resolution management](../concept/alternative-dispute-resolution.md)

