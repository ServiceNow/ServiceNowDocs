---
title: Work on a legal matter
description: As a matter owner, work on a legal matter assigned to you to resolve issues or answer queries.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 9
---

# Work on a legal matter

As a matter owner, work on a legal matter assigned to you to resolve issues or answer queries.

## Before you begin

Role required: sn\_lg\_matter.matter\_fulfiller

## About this task

When a legal request is promoted to a legal matter, the Privileged and Confidential status of the request determines the initial Privileged and Confidential status of the matter.

-   If the legal request has Privileged and Confidential enabled, the matter is created with Privileged and Confidential status. The matter owner can later remove the Privileged and Confidential status of the matter.
-   If the legal request has Privileged and Confidential disabled, the matter is created also has Privileged and Confidential disabled. You can enable the Privileged and Confidential status later.

The Privileged and Confidential status of a legal request and its associated matter are tracked independently. Changing the Privileged and Confidential status of a request does not automatically change the Privileged and Confidential status of the associated matter, and vice versa.

As a collaborator added to a legal matter, you can access and work on the legal matter just as matter owners can. However, you can't modify the **Matter owner**, **Assignment group**, and **Assignment group permission** fields.

**Note:** During times when you're unavailable, you can [delegate your legal duties to other users](../../legal-request-management/concept/legal-services-delegation.md).

## Procedure

1.  Navigate to **All** &gt; **Legal Request** &gt; **Legal Counsel Center**.

2.  In the Legal Counsel Center tab, select the list icon \(![List icon](../../legal-request-management/image/lsd-lcc-list-icon.png)\).

3.  In the **Lists** tab, open a legal matter by selecting an option under **Matters**.

<table id="choicetable_qbl_2bj_gtb"><thead><tr><th align="left" id="d189234e128">

Option

</th><th align="left" id="d189234e131">

Steps

</th></tr></thead><tbody><tr><td id="d189234e137">

**As an assignee**

</td><td>

1.  Select the **Assigned to Me** option.
2.  Select a legal matter to work on.
3.  If the legal matter is newly assigned to you, select **Start** to start working on it.

The state of the legal matter updates to Work in Progress.

</td></tr><tr><td id="d189234e166">

**As a collaborator**

</td><td>

1.  Select the **Collaborations** option.
2.  Select a legal matter to work on.


</td></tr></tbody>
</table>4.  Enable privilege and confidential status.

    1.  Select **Enable Privilege and Confidential** if already not enabled.

        The enable action is available only when the matter is in the Assigned or Work in progress state. Requests in states such as Closed Complete, Closed Incomplete, or Cancelled cannot have their Privileged and Confidential status changed.

    2.  On the confirmation modal, select **Continue**.

    -   The legal matter is marked as Privileged and Confidential.
    -   The assignment group permission is automatically updated to No Access. You can manually modify the assignment group permission.
    -   In the Privileged Document Access tab, the document permissions are marked as Privileged &amp; confidential. Access to these documents for users is controlled by the Assignment group permissions.
    -   Privileged and Confidential field in the secondary header is changed to Enabled.
    -   Notifications and outbound emails from the request automatically include "privileged and confidential" markers in the email content.
    -   Stakeholders are notified when changes occur to the collaborator list, watchlist, or fulfiller assignment for a privileged and confidential enabled request.
5.  Change permission for attachments.

    The document permission is marked as Privileged &amp; confidential when the request status is set as privileged and confidential, and resets to Public when the status is removed. Access to these documents for users is controlled by the Assignment group permissions.

    1.  Navigate to **Privileged Document Access**.

        The **Privileged Document Access** tab appears when Privileged and confidential status is enabled.

    2.  Select the check box next to the document for which you want to change the permission.

    3.  Select **Manage Access**.

    4.  Select the option applicable.

        -   Privileged and Confidential – Protects documents under legal privilege and confidentiality. Use this option for sensitive communications between an attorney and client.
        -   Legal Work Product Protected – Restricts access to internal legal analysis, drafts, or investigation notes prepared in anticipation of litigation.
        -   Public – Marks documents as freely shareable externally without restrictions.
    5.  Select **Update**.

6.  Update the **Assignment Group Permission** to change the permission level of the legal matter for the assigned user group.

    -   **No Access**: Only the practice area lead, group manager, and matter owner \(user in the **Matter owner** field\) can access and work on the legal matter.
    -   **Read**: All members from the assignment group can only view the legal matter.
    -   **Edit**: All members from the assignment group can view and edit the legal matter.
    **Note:** The matter owner, practice area lead, or group manager can set the assignment group permissions on the legal matter.

7.  [Create artifacts](add-artifact-to-legal-matter.md) \(folders\) and [attach files to a legal matter artifact](add-files-to-artifact.md) to store the collected supporting documents within the matter.

8.  If the request must be reassigned to a new assignment group due to business needs, select a new assignment group in the **Assignment group** field.

    **Note:** Editing of the **Assignment group** field is available only when the **Editable Assignment group in Matter** [option is configured](../../legal-request-management/task/associate-categories-practice-area.md) in the associated intake form.

    When the assignment group is changed, existing group members who are not in the updated assignment group might lose access to the matter. The **Matter owner** field is also cleared, and the matter owner is notified via email.

9.  If you need help from other fulfillers to work on the legal matter, add them in the **Collaborators** field.

    **Note:** Users with the matter\_fulfiller role are listed in the **Collaborators** field.

    The collaborators are notified via email that they have been added as collaborators to a legal matter.

10. [Initiate an ad hoc approval](initiate-approval-legal-matter.md) for the legal matter or its artifact's content when an approval is required from other stakeholders.

11. [Engage with outside counsel](lmm-eng-outcounsel.md) while resolving matters.

12. Communicate with the requester or other stakeholders using emails, chats, work notes, or comments.

    -   Using emails: Communicate with any stakeholders using emails. For more information, see [Communicate using emails](send-receive-email-legal-matter.md).
    -   Using live chats: Communicate with any stakeholders using chats. For more information, see [Start a chat session through Legal Counsel Center Inbox](../../legal-request-management/task/chat-employee-counsel-center.md).
    -   Using Comments: To communicate with the requester or other stakeholders, in the Compose section, enter your message in the **Comments** field and click **Post Comments**.
    -   Using Work notes: Communicate with the other members of the legal department, in the Compose section, enter your message in the **Work notes** field and click **Post Work notes**.

        Using response templates, you can insert predefined content into emails, chats, and legal request and legal matter form fields such as **Comments** and **Work notes**. Select the response template icon \(![Response template icon.](../../legal-request-management/image/response-template-email-icon.png)\) and find an appropriate response template based on the subject of your email. Copy and paste the template's content into the required field.

        **Note:** [Response templates configured for legal services](../../legal-request-management/task/create-lsd-response-template.md) are only available to use.

    For legal matters enabled for attorney client privilege, markers are added to the email content to indicate the privileged and confidential status.

13. Create and manage a checklist of items in the Counsel Assist section to track what should be done to resolve the legal matter.

14. [Create phases](add-phases-to-legal-matter.md) and [tasks under phases](add-tasks-to-legal-matter.md) to organize the investigation.

    You can assign these tasks to users across various departments in your organization.

15. [Add milestones](add-milestone-to-legal-matter.md) to keep a track of timelines to complete important tasks.

16. [Associate the matter with another legal request](associate-existing-matter-to-legal-request.md) that is similar in nature.

17. Either close the legal matter after you have completed the required activities or cancel it if it does not need further action.

    -   To close the matter, follow the instructions in [Close the legal matter](close-legal-matter.md).
    -   To cancel the matter, click the more actions button \(![More actions button icon.](../../legal-request-management/image/more-button-icon.png)\) and select **Cancel**.
18. If new information surfaces or further investigation is required [reopen the legal matter](reopen-legal-matter.md) after it has been closed or canceled.


-   **[Initiate an ad hoc approval for a legal matter or its artifact](initiate-approval-legal-matter.md)**  
Initiate an ad hoc approval for a legal matter or its artifacts from a user or a user group.
-   **[Engage with outside counsel](lmm-eng-outcounsel.md)**  
Engage with outside counsel to benefit from their expertise for resolving legal matters.
-   **[Approve or reject a legal matter or its artifact](approve-reject-legal-matter-artif.md)**  
Review a legal matter or its artifact's content and approve or reject it.
-   **[Communicate using emails from Legal Counsel Center](send-receive-email-legal-matter.md)**  
Compose and send emails directly from legal matter record form in the Legal Counsel Center. You can also save the email as draft to send it later.
-   **[Add a phase to a legal matter](add-phases-to-legal-matter.md)**  
Add a phase to a matter to track specific tasks to complete the matter.
-   **[Create a task for a legal matter](add-tasks-to-legal-matter.md)**  
Create a task in a legal matter or a phase of the matter that you or another user should perform to resolve the matter.
-   **[Create an artifact for a legal matter](add-artifact-to-legal-matter.md)**  
Create an artifact for a legal matter to upload and store documents, emails, and files related to the matter.
-   **[Add a milestone to a legal matter](add-milestone-to-legal-matter.md)**  
Add a milestone to a legal matter to track important calendar events related to the matter.
-   **[Associate related legal requests with a legal matter](associate-related-legal-requests-to-matter.md)**  
Associate one or more legal requests with a legal matter to organize and resolve related requests through a single matter.
-   **[Associate an existing legal matter with a legal request](associate-existing-matter-to-legal-request.md)**  
Associate an existing legal matter with a legal request that is similar to provide helpful information in resolving the request.
-   **[Disable attorney client privilege for legal matter](lmm-acp-disable.md)**  
Disable privileged and confidential status of a legal matter.
-   **[Close a legal matter](close-legal-matter.md)**  
Close a legal matter assigned to you when you complete all activities for resolving the legal matter. You can also close the matter if you find that it doesn’t need any further action.
-   **[Reopen a legal matter](reopen-legal-matter.md)**  
If a legal matter requires further investigation after it was closed or canceled, you can reopen it to work on it again.

**Parent Topic:**[Using Legal Matter Management](lmm-use-landing.md)

