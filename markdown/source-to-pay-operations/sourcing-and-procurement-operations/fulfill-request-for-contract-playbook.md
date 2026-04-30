---
title: Fulfill request for copy of contract in playbook
description: Attach a copy of the contract from a playbook and send it as an email to the employee who requested for it.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Fulfilling request for copy of contract in playbook, Working with Sourcing and Procurement Operations playbooks in the Source-to-Pay Workspace, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Fulfill request for copy of contract in playbook

Attach a copy of the contract from a playbook and send it as an email to the employee who requested for it.

## Before you begin

Role required: Procurement specialist

![Fulfill request for copy of contract in playbook](../image/pb-request-contract.png)

## Procedure

1.  Navigate to **All** &gt; **Procurement Case Management** &gt; **Source-to-Pay Workspace**.

2.  Select the List icon \(![List icon.](../../supplier-lifecycle-operations/image/cases-list-icon.png)\) and select **All work** &gt; **Cases**.

3.  Select the applicable Request a copy of contract case from the list for further processing.

4.  Complete the steps in the various stages and activities of the Verify and approve delivery address playbook.

<table id="table_bgd_tzx_ztb"><thead><tr><th>

Stage

</th><th>

Activity

</th><th>

Activity Details

</th></tr></thead><tbody><tr><td>

Review case

</td><td>

Assign case

</td><td>

Use this activity to assign the case to a different person or keep the case assigned to you.In the **Assigned to** search field, select a procurement specialist to work on this case.

Select one of the following actions:

-   Select **Save** to save your changes.
-   Select **Start work** to start working on the case.


</td></tr><tr><td rowspan="3">

Send a copy of contract

</td><td>

Collect contract details properties

</td><td>

This is an automated step to get the contract details from submitted case.

</td></tr><tr><td>

Review/attach contract properties

</td><td>

Find and review the contract as specified in request.If a contract is already attached to this case, it’s displayed here. The procurement specialist can open and view the contract and verify the details, if necessary.

</td></tr><tr><td>

Find and attach contract when contract number is not specified

</td><td>

Find and attach contract when contract number is not specified.Select **Compose email** to draft the email for the employee.

Select **Add File** to browse and attach the contract file to the email.

Consider these scenarios:

-   If a contract number is specified in the request, and an attachment exists for that contract in the contract record, attach the requested contract number to the email.
-   If a contract number is specified in the request, but an attachment doesn't exist for that contract in the contract record, find the file for the contract number and attach it to the email.
-   If a contract number isn't specified in the request, and only details are mentioned, find the contract as described by the requester and attach it to the email.
Select **Send Email** to send the email for the employee.

Select **Done**.

</td></tr><tr><td rowspan="2">

Close case

</td><td>

Complete case

</td><td>

Use this activity to add work notes and close the case.

Do the following:

-   In the **Work notes** field, add any comments about the case.
-   In the **Close notes** field, add any closing comments.
-   Select **Complete case**.
Updates the case to Closed Completed.

</td></tr><tr><td>

Update case to complete

</td><td>

The request is now fulfilled and the procurement case moves to the Closed Completed state.

</td></tr></tbody>
</table>
**Parent Topic:**[Fulfilling request for copy of contract in playbook](../concept/fulfilling-request-for-contract.md)

