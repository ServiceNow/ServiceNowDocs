---
title: Work on a legal request
description: Work on legal requests assigned to you or as a collaborator to resolve issues or answer queries.
locale: en-US
release: australia
product: Legal Request Management
classification: legal-request-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Managing legal requests, Use, Legal Request Management, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Work on a legal request

Work on legal requests assigned to youor as a collaboratorto resolve issues or answer queries.

## Before you begin

Role required: sn\_lg\_ops.legal\_fulfiller

## About this task

As a collaborator added to a request, you can access and work on the request just as assignees can. However, you can't modify the **Assigned to** and **Assignment group** fields.

**Note:** During times when you're unavailable, you can [delegate your legal duties to other users](../concept/legal-services-delegation.md).

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  In the Legal Counsel Center tab, select the list icon \(![List icon](../image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal request by selecting an option under **Legal Requests**.

<table id="choicetable_jhj_kb3_gtb"><thead><tr><th align="left" id="d208824e116">

Option

</th><th align="left" id="d208824e119">

Steps

</th></tr></thead><tbody><tr><td id="d208824e125">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a request to work on.
3.  If the request is newly assigned to you, select **Start Work** to start working on the request.

The state of the legal request is Work in progress and the document is Legal review.

</td></tr><tr><td id="d208824e154">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a request to work on.


</td></tr></tbody>
</table>4.  Enable privilege and confidential status.

    1.  Select **Enable Privilege and Confidential**.

        The enable action is available only when the request is in the Assigned or Work in progress state. Requests in states such as Closed Complete, Closed Incomplete, or Cancelled cannot have their Privileged and Confidential status changed.![Enable privileged and confidential](../image/lsd-acp-enable.png)

    2.  On the confirmation modal, select **Continue**.

    -   The legal request is marked as Privileged and Confidential.
    -   The assignment group permission is automatically updated to No Access. You can manually modify the assignment group permission.
    -   Privileged and Confidential field in the secondary header is changed to Enabled.
    -   In the Privileged Document Access tab, the document permissions are marked as Privileged &amp; confidential. Access to these documents for users is controlled by the Assignment group permissions.
    -   Notifications and outbound emails from the request automatically include "privileged and confidential" markers in the email content.
    -   Stakeholders are notified when changes occur to the collaborator list, watchlist, or fulfiller assignment of a privileged and confidential enabled request.
5.  Update the **Assignment group permission** to change the permission level of the legal request for the users.

    -   **No Access**: Only the practice area lead, group manager, and user in the **Assigned to** field can access the legal request and assign it to one of the members in the assignment group. The assigned user can then work on the legal request.
    -   **Read**: All members from the assignment group can only view the legal request. This option is the default permission level.
    -   **Edit**: All members from the assignment group can view and work on the legal request. The Assigned To field becomes optional if this option is set.
    Assignment Group Permission field of a active Legal Request Record can be edited by:

    -   Practice area lead, Assignment group manager, Assigned to, and delegated users.
    -   Any Assignment group member, if the record is in New state or Assignment group permission is edit or Configured options have assigned\_to\_field\_not\_mandatory in it.
6.  If the request must be reassigned to a new assignment group due to business needs, select a new assignment group in the **Assignment group** field.

    **Note:** Editing of the **Assignment group** field is available only when the **Editable Assignment group in Request** [option is configured](associate-categories-practice-area.md) in the associated intake form.

    When the assignment group is changed, existing group users who are not in the updated assignment group might lose access to the request. The **Assigned to** field is also cleared, and the assigned user is notified via email.

7.  If you need help from other fulfillers to work on the legal request, add them in the **Collaborators** field.

    **Note:** Users with the sn\_lg\_contracts.contracts\_fulfiller role are listed in the **Collaborators** field.

    The collaborators are notified via email that they have been added as collaborators to a legal request.

8.  Work on the legal request to fulfill the requested services or information.

    If the request needs detailed investigation, you can [promote the request to a legal matter](promote-legal-request-to-matter.md).

    **Note:** To promote a legal request to a legal matter, you must have the Legal Matter Management app installed and the record producer type for the associated intake form must be set to **Request and Matter**. For more information on setting a record producer type, see [Add an intake form to a practice area](associate-categories-practice-area.md).

9.  [Manage documents](manage-attachments-legal-request.md) that are part of the resolution to the legal request.

10. [Initiate an ad hoc approval](initiate-approval-legal-request.md) for the legal request or its attachments when an approval is required from other stakeholders.

11. Communicate with the requester or other stakeholders using emails, chats, work notes, or comments.

    -   Using emails: Communicate with any stakeholders using emails. For more information, see [Communicate using emails](send-receive-email-legal-req.md).
    -   Using live chats: Communicate with any stakeholders using chats. For more information, see [Start a chat session through Legal Counsel Center Inbox](chat-employee-counsel-center.md).
    -   Using Comments: To communicate with the requester or other stakeholders, in the Compose section, enter your message in the **Comments** field and click **Post Comments**.
    -   Using Work notes: Communicate with the other members of the legal department, in the Compose section, enter your message in the **Work notes** field and click **Post Work notes**.

        Using response templates, you can insert predefined content into emails, chats, and legal request and legal matter form fields such as **Comments** and **Work notes**. Select the response template icon \(![Response template icon.](../image/response-template-email-icon.png)\) and find an appropriate response template based on the subject of your email. Copy and paste the template's content into the required field.

        **Note:** [Response templates configured for legal services](create-lsd-response-template.md) are only available to use.

    Legal requests marked as Privileged and Confidential, contain confidentiality markers to comply with legal requirements. This applies to both system-generated notifications and fulfiller-initiated outbound emails.

12. Either close the request or cancel it.

    -   After you resolve the request, you can [close the request](close-legal-request.md).
    -   If you identify that the request doesn't need any action, you can cancel it.

-   **[Manage attachments for a legal request](manage-attachments-legal-request.md)**  
Upload supporting documentation, such as documents, email copies, images, or any other files into a legal request while you are working on it.
-   **[Initiate an ad hoc approval for a legal request or its attachment](initiate-approval-legal-request.md)**  
Initiate an ad hoc approval for a legal request or its attachments from a user or a user group.
-   **[Approve or reject a legal request or its attachment](approve-reject-legal-request-attach.md)**  
Review a legal request or attachment and approve or reject it.
-   **[Communicate using emails from Legal Counsel Center](send-receive-email-legal-req.md)**  
Compose and send emails directly from legal request record form in the Legal Counsel Center. You can also save the email as draft to send it later.
-   **[Promote a legal request to a legal matter](promote-legal-request-to-matter.md)**  
Promote a legal request to a legal matter when the request needs additional investigation and cross-departmental collaboration that might take more time to resolve.
-   **[Transfer a legal request](transfer-existing-legal-request.md)**  
Transfer a legal request to a new practice area or category if the request was submitted with an inappropriate practice area or category.
-   **[Update a legal request by requester](submit-legal-request-requester.md)**  
Update the variables in the form fields and submit the legal request by the requester once the request is sent back by the fulfiller.
-   **[Disable attorney client privilege for a legal request](../concept/lsd-acp-enable.md)**  
Disable attorney client privilege for a legal request.
-   **[Close a legal request](close-legal-request.md)**  
You can close a legal request assigned to you when you've resolved it.

**Parent Topic:**[Managing legal requests](../concept/managing-legal-request.md)

