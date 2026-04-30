---
title: Document access in a legal request
description: Documents attached to legal requests are uploaded to the configured external storage system when the external storage option is enabled on the legal request intake form. The access of these documents to various personas is controlled in real time, via a scheduled job, or on-demand.Request access to documents attached to a legal request that you do not currently have access to.Remove existing users' access to documents attached to a legal request when they are no longer required to view those documents.
locale: en-US
release: yokohama
product: Legal Request Management
classification: legal-request-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Manage attachments for a legal request, Work on a legal request, Managing legal requests, Legal Request Management, Legal Service Delivery, Employee Service Management]
---

# Document access in a legal request

Documents attached to legal requests are uploaded to the configured external storage system when the external storage option is enabled on the legal request intake form. The access of these documents to various personas is controlled in real time, via a scheduled job, or on-demand.

## Document access for various personas

The following table shows the type of access to documents and when it is granted to various personas.

<table id="table_egh_qmf_htb"><thead><tr><th>

Persona

</th><th>

Access type

</th><th>

When

</th></tr></thead><tbody><tr><td>

Requester, requested for

</td><td>

Read, Write, Delete—on their own documentsRead only—on documents attached by the legal request fulfiller

</td><td>

Request is submitted

</td></tr><tr><td>

Group manager

</td><td>

Read, Write, Delete

</td><td>

Request is submitted

</td></tr><tr><td>

Legal request fulfiller \(Assigned to\)

</td><td>

Read, Write, Delete

</td><td>

Request is assigned

</td></tr><tr><td>

Collaborators

</td><td>

Read, Write, Delete

</td><td>

Added to the **Collaborators** list

</td></tr><tr><td>

Ad hoc approvers

</td><td>

Read only, No delete

</td><td>

Ad hoc approval is initiated

</td></tr><tr><td>

Practice area lead

</td><td>

Read only, No delete

</td><td>

Scheduled job is run or on-demand

</td></tr><tr><td>

Members of assignment group

</td><td>

Depends on the **Assignment group permission** field

</td><td>

Scheduled job is run or on-demand

</td></tr><tr><td>

Watch list users

</td><td>

Read only, No delete

</td><td>

Added to the **Watch list**

</td></tr><tr><td>

Delegates

</td><td>

Read, Write, Delete

</td><td>

**Resolve platform delegation permissions for legal request** job is run as scheduled, or on-demand

</td></tr><tr><td>

Delegates through granular delegation

</td><td>

Read only, No delete

</td><td>

User is delegated

</td></tr></tbody>
</table>The scheduled job **Process External Storage Permissions** runs at the defined intervals to sync access for all unprocessed permissions on documents for legal requests stored in external storage.

-   Requesters can access documents attached to their legal requests from the **Documents** tab on the Standard Ticket page.

    **Note:** Requesters can delete only those documents from the request that they've attached.

-   The legal fulfiller assigned to the legal request can access documents from the **Documents** tab of the request record in the Legal Counsel Center.
-   Users added to the matter can request on-demand access to documents if they need access before the scheduled job is run.
-   The legal fulfiller can revoke a user's access to documents.
-   Ad hoc approvers lose document access after they approve or reject the requested item.
-   Delegates lose access after the delegation period expires.

**Parent Topic:**[Manage attachments for a legal request](../task/manage-attachments-legal-request.md)

## Request document access for a legal request

Request access to documents attached to a legal request that you do not currently have access to.

### Before you begin

Role required: sn\_lg\_ops.legal\_user or sn\_lg\_ops.legal\_fulfiller

### About this task

### Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, under **Legal Requests**, click **All**.

4.  Open a legal request you want to request access to see the documents attached to it.

5.  In the **Documents** tab, click **Request Access**.


### Result

The system processes the user's permissions and grants access to the documents in the legal request.

## Remove document access of users in a legal request

Remove existing users' access to documents attached to a legal request when they are no longer required to view those documents.

### Before you begin

Role required: sn\_lg\_ops.request\_admin

### Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, under **Legal Requests**, click **All**.

4.  Open a legal request you want to remove users' access to documents attached to it.

5.  In the **Documents Access** tab, select users for whom you want to remove the document access.

    **Note:** The **Document Access** tab is only visible to the practice area lead, the manager of the current assignment group, and the assigned to person.

6.  Click **Remove Access**.


### Result

The document access of the selected users is removed, and they're also removed from the list. The user will no longer be able to view the request's documents.

