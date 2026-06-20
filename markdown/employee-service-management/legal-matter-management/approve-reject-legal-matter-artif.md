---
title: Approve or reject a legal matter or its artifact
description: Review a legal matter or its artifact's content and approve or reject it.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/employee-service-management/legal-matter-management/approve-reject-legal-matter-artif.html
release: zurich
product: Legal Matter Management
classification: legal-matter-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Work on a legal matter, Use, Legal Matter Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Approve or reject a legal matter or its artifact

Review a legal matter or its artifact's content and approve or reject it.

## Before you begin

You must have received an email notification with a link to the legal item for approval.

Role required: none

## Procedure

1.  Open the approval record from the email notification, Legal Counsel Center, Self-Service, or Employee Center portal.

<table id="choicetable_ix4_gbl_trb"><thead><tr><th align="left" id="d303695e60">

Options

</th><th align="left" id="d303695e63">

Steps

</th></tr></thead><tbody><tr><td id="d303695e69">

**From the email notification**

</td><td>

Click the link in the email to open the record that needs approval.

</td></tr><tr><td id="d303695e78">

**From Legal Counsel Center**

</td><td>

**Note:** The request\_fulfiller role is required to access Legal Counsel Center.

 1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.
2.  Click the list icon \(\[Omitted image "lsd-lcc-list-icon.png"\] Alt text: List icon\).
3.  In the **Lists** tab, under **My Work**, click **Items Pending Approval**.
4.  In the Items Pending Approval list, click a record to open for approval.


</td></tr><tr><td id="d303695e139">

**From Self-Service**

</td><td>

1.  Navigate to **All** &gt; **Self-Service** &gt; **My Approvals**.
2.  In the My Approvals list, click a record to open for approval.


</td></tr><tr><td id="d303695e169">

**From Employee Center**

</td><td>

1.  In the Employee Center portal, on the menu bar, click the **My Tasks**.
2.  In the My To-dos list, click a record under the **Open** tab to open for approval.


</td></tr></tbody>
</table>2.  Review the record and either approve or reject:

    -   To approve the record, click **Approve**.
    -   To reject the record, enter comments for rejection in the **Comments** field and click **Reject**.

## Result

The following table shows the result of approve and reject actions on the approval record.

<table id="table_xst_hbd_hlb"><thead><tr><th>

Approve

</th><th>

Reject

</th></tr></thead><tbody><tr><td>

-   The approval record's state updates from Requested to Approved.

If the requested item was assigned to a user group for approval, then the state of the approval records for the remaining users updates from Requested to No Longer Required.

**Note:** If the approval was for an attachment of the legal matter artifact, the attachment cannot be deleted from the legal matter artifact.

-   Any approver who isn’t added to **Watch list** in the legal matter would lose access to the approved item.

</td><td>

-   The approval record's state updates from Requested to Rejected.

If the requested item was assigned to a user group for approval, then the state of the approval records for the remaining users updates from Requested to No Longer Required.

-   The comments for rejection posted by the approver is added to the legal matter's Activities section.
-   Any approver who isn’t added to **Watch list** in the legal matter would lose access to the approved item.

</td></tr></tbody>
</table>**Parent Topic:**[Work on a legal matter](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown)

