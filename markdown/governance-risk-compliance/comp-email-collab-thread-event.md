---
title: Create a collaboration thread in an exercise
description: Create a collaboration thread from an exercise and send an email to its recovery teams to coordinate a response.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/governance-risk-compliance/comp-email-collab-thread-event.html
release: zurich
topic_type: task
last_updated: "2026-08-23"
reading_time_minutes: 6
breadcrumb: [Structured workflows for exercises, Manage, Business Continuity Management, Governance, Risk, and Compliance]
---

# Create a collaboration thread in an exercise

Create a collaboration thread from an exercise and send an email to its recovery teams to coordinate a response.

## Before you begin

Role required: sn\_bcm.manager

An administrator must configure at least one active email account and enable the **Email sending enabled** and **Email receiving enabled** system properties before you can send or receive collaboration emails. For more information, see [Configure email for collaboration threads](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-email-for-collaboration-threads.md).

Sending email from a collaboration thread also requires the platform `email_composer` role. This role is granted automatically to `sn_recovery.event_manager`; users with other roles may need it granted separately.

## Procedure

1.  In the List view, navigate to **Exercises** and select the crisis event in the list.

2.  In the **Collaboration threads** tab of the event, select **New**.

    The Create New Collaboration Thread form is displayed.

    \[Omitted image "cm-create-collab-thread.png"\] Alt text: Create New Collaboration Thread form with name, state, recovery teams, impacted assets, and description fields.

3.  On the form, fill in the fields.

    For descriptions of all these fields, see [Create Collaboration thread form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-collaboration-thread-crisis-event-form.md).

    1.  Add the name of the thread in the **Name** field, add **Description**, and select one or more **Recovery teams**.

    2.  Check the activated plan and impacted assets for the event.

        The **Impacted assets** field only lists assets that are already associated with the parent crisis event, for example, through an activated plan. If no assets appear, add the plan or asset to the event first. You can then select them from the **Impacted assets** field.

        The following example shows an activated plan added to the event. Selecting **View progress** shows the progress tracker processing the activated plans. Assets added from the activated plan to the event are displayed in the **Assets** tab as shown in the example.

        \[Omitted image "acti-plan-f-event-prog-tra.png"\] Alt text: Progress tracker.\[Omitted image "acti-plan-added-to-the-event.png"\] Alt text: Plan added to the event.

    3.  Add **Impacted assets** to the collaboration thread.

    4.  Select **Save**.

    The collaboration thread record is created in the **Open** state.

    Saving the record also sends an automatic notification email to the members of the selected recovery teams, letting them know the thread was opened. This system-generated email appears in the **Emails** tab along with any email that you send later with **Compose email**.

4.  On the **Action items** tab of the collaboration thread, select **New** to track follow-up work assigned during the coordination effort.

    1.  Fill in the **Short description**, **Description**, and **Type** fields, assign the action item, and select **Save**.

    \[Omitted image "cm-collab-thread-create-action-item.png"\] Alt text: Create New Action item form with short description, description, type, and assignment fields.

5.  On the **Emails** tab of the collaboration thread, select **Compose email**.

    Verify that email sending option is enabled for the inbound and outbound emails as shown in the example.

    \[Omitted image "cm-collab-email-config-email-properties-config.png"\] Alt text: Email Properties page with outbound and inbound email configuration sections.

    **Note:** For setting up email properties in the instance, see [Configure email for collaboration threads](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/configure-email-for-collaboration-threads.md).

    For more information on the Email Properties configurations in the ServiceNow AI Platform, see [Email properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/c_EmailProperties.md).

    The email panel opens with the **To** field populated from the members of the recovery teams that you selected. The **Subject** and body fields are populated with default text from the **Collaboration Thread Default** email template, which names the crisis event.

    The **To** field also includes the members of any groups linked to the recovery teams, including their nested sub-groups. Only active users are included, and duplicate addresses are removed.

    You can also open the same email panel by selecting the **Email** option next to **Work notes** in the activity panel of the collaboration thread record.

    \[Omitted image "cm-collab-compose-email-two-ways.png"\] Alt text: Collaboration thread record with the Compose email button and the Email option next to Work notes in the activity panel. \[Omitted image "cm-collab-email.png"\] Alt text: Email panel with subject and body text populated from the collaboration thread email template.

6.  Add or remove recipients in the **To**, **Cc**, or **Bcc** fields, and edit the **Subject** or body text.

7.  Select **Send**.

    The email is sent and is added to the **Emails** tab of the collaboration thread. The activity feed of the collaboration thread and of its parent crisis event both show that the email was sent.

8.  To discard the email without sending it, select the delete icon instead of **Send**.

9.  To view a sent or received message, select it in the **Emails** tab of the collaboration thread.

    The email preview screen opens, showing the message and any attachments. Each row in the **Emails** tab shows a **Status** of **Processed** or **Error** for the message.

    \[Omitted image "cm-collab-email-shown-in-tab-state-column.png"\] Alt text: Emails tab with subject, recipient, body text, created, and status columns.

10. To reply to or forward a message, select **Reply** or **Forward** on the email preview screen, add any attachments, and select **Send**.

    \[Omitted image "cm-collab-tab-email-replied-from-thread.png"\] Alt text: Email preview screen with Reply, Reply all, and Forward options and an attachment.

    **Note:** An inbound reply is captured automatically and shown in the **Emails** tab and in the activity feed. Attachments sent or received through email appear under **Email Attachments**, separate from the record's **Attachments** tab, which holds only files attached directly to the record.

    \[Omitted image "cm-collab-email-sent-frm-outl-recd-in-collab-emails-tab.png"\] Alt text: Emails tab showing an inbound reply received alongside the outbound collaboration thread email. \[Omitted image "cm-collab-email-atch-tab.png"\] Alt text: Email Attachments tab listing a file attached through a collaboration email.

11. Review and track all collaboration thread details in the Activity panel of the event.

12. To generate a report of the record in Microsoft Word format, select **More \(...\)**, choose **Generate MS Word**, choose one of the following templates, and select **Generate**.

    \[Omitted image "default-event-word-temp.png"\] Alt text: Default template.\[Omitted image "default-event-word-temp-w-collab-blk.png"\] Alt text: Default template with a block.

    |Choice|Description|
    |------|-----------|
    |**Event Word template**|Generate Microsoft Word report with default template. Collaboration thread details are shown in a tabular format with the default template.|
    |**Event Word template with collab-Block**|Generate Microsoft Word report with collaboration block. Collaboration block with action items related to that collaboration detail are shown in a tabular format.|

    \[Omitted image "collab-thread-in-pdf.png"\] Alt text: Default template.\[Omitted image "collab-thread-as-a-block.png"\] Alt text: Block.

    For enabling addition of a collaboration block in the Microsoft Word document, see [Update the Word template with a collaboration block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/add-collaboration-block-docudesigner.md).

13. To generate a report of the event in PDF format, select **More \(...\)** and then choose **Generate PDF** and check collaboration thread details in the PDF.


**Parent Topic:**[Structured workflows for exercises](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/performing-tasks-to-manage-exercise-events.md)

**Related topics**  


[Creating collaborations in exercises and crisis events](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/creating-collaboration-threads-in-crisis.md)

[Create a collaboration thread in a crisis event](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/compose-email-collaboration-thread-crisis.md)

[Create Collaboration thread form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/governance-risk-compliance/create-collaboration-thread-crisis-event-form.md)

