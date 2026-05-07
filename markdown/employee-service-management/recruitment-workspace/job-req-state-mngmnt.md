---
title: Job requisition state management
description: An overview of the job requisition state management system for a recruiter.
locale: en-US
release: australia
product: Recruitment Workspace
classification: recruitment-workspace
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Reference, Recruitment Workspace, Hiring Experiences, HR Service Delivery, Employee Service Management]
---

# Job requisition state management

An overview of the job requisition state management system for a recruiter.

<table id="table_job_req_sys"><thead><tr><th>

State

</th><th>

On hold

</th><th>

Access for recruiter

</th><th>

Allowed actions

</th><th>

Result of the action

</th><th>

New state post the action

</th><th>

Access for recruiter in new state

</th></tr></thead><tbody><tr><td rowspan="6">

Open

</td><td rowspan="3">

Yes

</td><td rowspan="3">

Read only

</td><td>

Resume

</td><td>

Withdraw the hold from the job requisition.

</td><td>

Open

</td><td rowspan="3">

Read only

</td></tr><tr><td>

Close

</td><td>

Close the job requisition and don't cancel any approvals.

</td><td>

Closed

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

Open

</td></tr><tr><td rowspan="3">

No

</td><td rowspan="3">

Read only

</td><td>

On Hold

</td><td>

Put the job requisition on hold.

</td><td>

Open

</td><td rowspan="3">

Read only

</td></tr><tr><td>

Close

</td><td>

Close the job requisition and don't cancel the approvals.

</td><td>

Closed

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

Open

</td></tr><tr><td rowspan="8">

Ready

</td><td rowspan="3">

Yes

</td><td rowspan="3">

Editable

</td><td>

Resume

</td><td>

Withdraw the hold from the job requisition.

</td><td>

Ready

</td><td>

Editable

</td></tr><tr><td>

Close

</td><td>

Close the job requisition and don't cancel the approvals.

</td><td>

Closed

</td><td>

Ready only

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

Ready

</td><td>

Read only

</td></tr><tr><td rowspan="5">

No

</td><td rowspan="5">

Editable

</td><td>

On Hold

</td><td>

Put the job requisition on hold.

</td><td>

Ready

</td><td>

Editable

</td></tr><tr><td>

Open

</td><td>

Send the job requisition to the designated application tracking system \(ATS\).

</td><td>

Open

</td><td>

Read only

</td></tr><tr><td>

Resend for Approval

</td><td>

Cancel all existing approvals and submit the requisition for fresh approvals.

</td><td>

Pending Approval

</td><td>

Read only

</td></tr><tr><td>

Close

</td><td>

Close the job requisition and don't cancel the approvals.

</td><td>

Closed

</td><td>

Read only

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

Ready

</td><td>

Read only

</td></tr><tr><td rowspan="7">

Rejected

</td><td rowspan="3">

Yes

</td><td rowspan="3">

Editable

</td><td>

Resume

</td><td>

Withdraw the hold from the job requisition.

</td><td>

New

</td><td>

Editable

</td></tr><tr><td>

Close

</td><td>

Close the job requisition.

</td><td>

Closed

</td><td>

Read only

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

New

</td><td>

Editable

</td></tr><tr><td rowspan="4">

No

</td><td rowspan="4">

Editable

</td><td>

Submit for Approval

</td><td>

Submit the job requisition for approval.

</td><td>

Pending Approval

</td><td>

Read only

</td></tr><tr><td>

On Hold

</td><td>

Put the job requisition on hold.

</td><td>

New

</td><td>

Editable

</td></tr><tr><td>

Close

</td><td>

Close the job requisition.

</td><td>

Closed

</td><td>

Read only

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

New

</td><td>

Editable

</td></tr><tr><td rowspan="7">

Pending Approval \(Requested\)

</td><td rowspan="3">

Yes

</td><td rowspan="3">

Read only

</td><td>

Resume

</td><td>

Withdraw the hold from the job requisition.

</td><td>

New

</td><td>

Editable

</td></tr><tr><td>

Close

</td><td>

Close the job requisition.

</td><td>

Closed

</td><td>

Read only

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

Pending Approval

</td><td>

Read only

</td></tr><tr><td rowspan="4">

No

</td><td rowspan="4">

Read only

</td><td>

Cancel Approval

</td><td>

Cancel all existing approvals and put the job requisition in **New** state.

</td><td>

New

</td><td>

Editable

</td></tr><tr><td>

On Hold

</td><td>

Put the job requisition on hold and cancel all existing approval requests.

</td><td>

New

</td><td>

Editable

</td></tr><tr><td>

Close

</td><td>

Close the job requisition and don't cancel the approvals.

</td><td>

Closed

</td><td>

Read only

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

Pending Appoval

</td><td>

Read only

</td></tr><tr><td>

Ready

</td><td colspan="6">

In **Ready** state and follows the behaviour of the same.

</td></tr><tr><td>

Rejected

</td><td colspan="6">

In **New** state and follows the behaviour of the **Rejected** state.

</td></tr><tr><td rowspan="3">

Closed

</td><td>

Yes

</td><td>

Read only

</td><td colspan="4">

**Note:** Withdraw the hold whenever a job requisition is closed.

</td></tr><tr><td rowspan="2">

No

</td><td rowspan="2">

Read only

</td><td>

Reopen

</td><td>

Changes to **New** state and follows the behaviour of the same.

</td><td>

New

</td><td>

Editable

</td></tr><tr><td>

Duplicate

</td><td>

Create a new job requisition by duplicating an existing one.

</td><td>

Closed

</td><td>

Read only

</td></tr></tbody>
</table>**Parent Topic:**[Recruitment Workspace reference](../concept/recruitment-workspace-reference.md)

