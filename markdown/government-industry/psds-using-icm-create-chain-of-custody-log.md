---
title: Create a chain of custody log for an evidence record in an investigative case
description: As an investigator or supervisory agent, you can create a Chain of Custody \(CoC\) log within the workspace to keep track of evidence if or when it is transferred or moved.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Using Evidence Management, Using Investigative Case Management, Solutions, Use, Public Sector Digital Services \(PSDS\)]
---

# Create a chain of custody log for an evidence record in an investigative case

As an investigator or supervisory agent, you can create a Chain of Custody \(CoC\) log within the workspace to keep track of evidence if or when it is transferred or moved.

## Before you begin

Role required: icm.investigator, supervisory\_agent, admin

**Note:** The ability to create a Chain of Custody Log for an evidence record is strictly tied to write access for that evidence record. If the particular user does not have write access to the open evidence record, they will not be able to create a record. For more information on modifying the security classification for an evidence record or for a case, see .

## About this task

With Investigative Case Management Evidence Management, investigators can create a chain of custody log within the workspace to track the movement, transfer, and status changes of evidence records associated with the case. You can view timestamps and responsible personnel for each action with audit logging, capturing when and by who something was opened and viewed.

**Note:** A Chain of Custody Log cannot be created if the evidence record is in Draft state.

The Chain of Custody Log form collects the following information about a piece of evidence:

<table id="table_g15_kmx_n3c"><thead><tr><th>

Fields

</th><th>

Description

</th></tr></thead><tbody><tr><td>

From custodian

</td><td>

The custodian that the evidence was transferred from. Filled in by default.

</td></tr><tr><td>

 

</td><td>

Method used to transfer custody of evidence from one individual to another. If this is the first time this piece of evidence is being received or handled, select **Initial Receipt**. Otherwise, the method of transfer may be:-   In-person
-   Secure upload
-   Courier
-   Email

</td></tr><tr><td>

 

</td><td>

The date and time of the transfer. You may enter a past, present, or future date.

</td></tr><tr><td>

 

</td><td>

The action taken on the evidence. The evidence may have been taken:-   To laboratory for analysis
-   To court for trial/proceeding
-   To storage/vault
-   To case agent or investigator
-   For review or inspection
-   To case agent or investigator
-   For review or inspection
-   Collected
-   Return from court
-   Inter-agency transfer
-   Disposal
-   Return to owner
-   Digital transfer
-   Returned from laboratory
-   Temporary custody assignment

</td></tr><tr><td>

Custodian type

</td><td>

Whether the receiving custodian is an internal user with a user record in the instance, or external.

</td></tr><tr><td>

To Custodian

</td><td>

The custodian’s name. If internal, a user record reference. If external, a string.

</td></tr><tr><td>

Location type

</td><td>

Indicates whether the evidence is changing physical location, digital location, or both.

</td></tr><tr><td>

From location

</td><td>

Location the evidence is being transferred from. Filled in by default.

</td></tr><tr><td>

To location

</td><td>

Location the evidence is being transferred to. Changing the location within the Chain of Custody log will change the physical/digital location in the evidence record at large.

</td></tr></tbody>
</table>## Procedure

1.  Navigate to the CSM Configurable Workspace and select **My active cases**.

    Alternatively, you can select a case using the CSM Configurable Workspace Lists menu by selecting **Lists** &gt; **Investigative Cases** &gt; **All** and selecting the case.

2.  Select the case you wish to add a chain of custody log to.

3.  Select the **Chain of Custody** tab.

4.  Select **Add Entry**.

5.  On the form, fill in the fields with details about the evidence interaction.

6.  Enter the method of transfer.

7.  Enter the date and time during which the evidence was handled.

8.  Select the action that was taken with the evidence from the dropdown menu.

9.  Enter any notes.

10. Add any attachments.

    Attachments can be deleted or renamed until the chain of custody log is added to the evidence record. After the log is added, the user can add attachments but not delete or rename existing ones. Work notes can be added in the activity stream after creating the log.

11. Select the checkbox to affirm that you have complied with all evidence handling requirements, and enter your signature.

    You can type or draw your signature. The signature image is saved as an attachment to the log.

12. Select **Create Entry**.


## Result

A Chain of Custody log is now started, and a new entry can be added every time a piece of evidence is moved, handled, or otherwise interacted with. To create a log entry, select **Add Entry** on the Chain of Custody record page. Select the log number to view the details of a CoC log entry.

**Note:** The Chain of Custody log record becomes read only after it is created. Existing Chain of Custody log records can only be modified by an admin.

