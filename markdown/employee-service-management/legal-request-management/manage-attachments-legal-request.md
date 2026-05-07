---
title: Manage attachments for a legal request
description: Upload supporting documentation, such as documents, email copies, images, or any other files into a legal request while you are working on it.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Work on a legal request, Managing legal requests, Use, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Manage attachments for a legal request

Upload supporting documentation, such as documents, email copies, images, or any other files into a legal request while you are working on it.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## About this task

You can also use these artifacts as a reference material to solve similar requests in future.

If the [external storage option](associate-categories-practice-area.md) is enabled, you can manage document access for users to see these attachments. For more information, see [Document access in a legal request](../concept/document-access-legal-request.md#).

If the Privileged and Confidential status is enabled on a legal request, you can change the permission of attached documents from the Privileged Document Access tab.

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  Click the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal request by selecting an option under **Legal Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d78342e113">

Option

</th><th align="left" id="d78342e116">

Steps

</th></tr></thead><tbody><tr><td id="d78342e122">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start Work** to start working on the request.

The state of the legal request is Work in progress and the document is Legal review.

</td></tr><tr><td id="d78342e151">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>4.  Manage documents in the legal request.

<table id="choicetable_rpv_3f2_f5b"><thead><tr><th align="left" id="d78342e181">

Option

</th><th align="left" id="d78342e184">

Steps

</th></tr></thead><tbody><tr><td id="d78342e190">

**Using the attachment icon**

</td><td>

The attachment icon ![Attachment icon.](../image/add-attachment-icon.png) appears in the Counsel Assist side bar when the external storage option is not enabled.

 1.  In the Counsel Assist sidebar, select the attachment icon.
2.  In the **Attachments** pane, add, rename, or remove attachments.
    -   To upload a document, select the **Browse** button or the add attachment icon \(![Add attachment icon.](../../ppe-inventory-management/image/plus-icon.png)\) and select a file.

**Note:** The **Browse** button is available when the legal request has no attachments else the add attachment icon ![Add attachment icon.](../../ppe-inventory-management/image/plus-icon.png) is available.

    -   To rename an attached file, select the actions icon \(![Actions icon.](../image/more-actions-icon.png)\), select **Rename** and update the file name.
    -   To delete an attached file, select the actions icon, select **Remove**.
    -   To download an attached file, select the actions icon, select **Download**.


</td></tr><tr><td id="d78342e272">

**Using the Documents tab**

</td><td>

The **Documents** tab appears when the external storage option is enabled.

 -   Upload a new document.

    1.  In the **Documents** tab, select **Attach** and select a file.
    2.  On the New Document form, select **Attach file** link and select a file.
    3.  Select **Save**.
In the **Documents** tab, a link to the document is listed in the **External URL** column of the documents list.

-   Remove an attached file.

    1.  In the **Documents** tab, select a document from the list that you want to delete.
    2.  Select **Delete**.
Access to these documents to various users is controlled in multiple ways. For more information on managing document access, see [Document access in a legal request](../concept/document-access-legal-request.md#).

</td></tr><tr><td id="d78342e348">

**Using Privileged Document Access tab**

</td><td>

The Privileged Document Access tab appears when Privileged and confidential status is enabled. The document permission is marked as Privileged &amp; confidential when the request status is set as privileged and confidential, and resets to Public when the status is removed. Access to these documents for users is controlled by the Assignment group permissions.

Change permissions for documents.1.  In the **Privileged Document Access** tab, select the check box next to the document for which you want to change the permission.
2.  Select **Manage Access**.
3.  Select the option applicable.
    -   Privileged and Confidential – Protects documents under legal privilege and confidentiality. Use this option for sensitive communications between an attorney and client.
    -   Legal Work Product Protected – Restricts access to internal legal analysis, drafts, or investigation notes prepared in anticipation of litigation.
    -   Public – Marks documents as freely shareable externally without restrictions.
4.  Select **Update**.


</td></tr></tbody>
</table>
-   **[Document access in a legal request](../concept/document-access-legal-request.md#)**  
Documents attached to legal requests are uploaded to the configured external storage system when the external storage option is enabled on the legal request intake form. The access of these documents to various personas is controlled in real time, via a scheduled job, or on-demand.

**Parent Topic:**[Work on a legal request](work-on-legal-request.md)

