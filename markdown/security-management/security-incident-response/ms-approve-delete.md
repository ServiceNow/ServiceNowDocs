---
title: Approve delete email requests for the Microsoft Exchange Online integration
description: If the approval option is enabled in your ServiceNow AI Platform instance, requests to delete emails are sent to each member of the approval group via email. You select the approval group during the configuration step. Approvals provide your organization with an additional level of control over the deletion of emails.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Microsoft Exchange Online integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Approve delete email requests for the Microsoft Exchange Online integration

If the approval option is enabled in your ServiceNow AI Platform instance, requests to delete emails are sent to each member of the approval group via email. You select the approval group during the configuration step. Approvals provide your organization with an additional level of control over the deletion of emails.

## Before you begin

Verify that you have the **Approvals** option selected on the Additional Settings tab of the Exchange Online Search and Delete Emails Configuration Settings form.

Verify that you have enabled the email **Email sending enabled**and **Email receiving enabled** options in your ServiceNow AI Platform instance for approval requests.

When the user with the sn\_si.analyst role submits delete email requests, by default, these requests are sent via email to the sn\_si.admin. If you have created an approval group, each member of the group receives a notification. Approvers can process email delete requests directly from the email notification. Alternatively, requests can be processed from the email search result records in ServiceNow AI Platform instances. This topic shows both approval methods.

The following information describe the request in the email notification:

-   **Email Search Result record number**

    Unique number assigned to the search record by the ServiceNow AI Platform as part of the audit trail.

-   **Name of the analyst who submitted the request**

    Name of the person who submitted the request as part of the audit trail.

-   **Link to the security incident**

    A link to the security incident related to the phishing event. View the security incident with the work notes, email searches, and email search results directly from the email.

-   **Approve or Reject links**

    Links to approve or reject the request from the email notification. After you click either link, the system automatically initiates the related workflow and a work note is posted to the security incident record.


Role required: sn\_si.admin or all members of an assigned approval group.

## Procedure

1.  To process the delete request from the email notification, follow these steps.

    1.  As an approver, locate the notification email in the email account that you configured in your ServiceNow AI Platform user account.

        In this example, the user with the sn\_si.analyst role \(Hans SecAnalyst\) submits a request to delete one email. Johann SecAdmin is a member of the approval group.

        ![Email notification for delete approval request.](../image/ms-122-approval-email.png)

    2.  In the email notification, choose one option to continue.

<table id="choicetable_fwm_nrk_4gb"><thead><tr><th align="left" id="d101619e170">

Option

</th><th align="left" id="d101619e173">

Description

</th></tr></thead><tbody><tr><td id="d101619e179">

**Click the Click here to approve Approve link**

</td><td>

Approve the delete request. All the email items with a status of `false` in the Was deleted column that are associated with the search result record are automatically deleted from the Microsoft Exchange Online tenant. The status of all the email items of the result set is updated to `true` in the Was deleted column of the Email search result record.

A work note is posted to the security incident record with the number of successfully deleted emails. If tagging is enabled, the `Email Delete - Completed` tag replaces the `Email Delete - Initiated` tag.

</td></tr><tr><td id="d101619e206">

**Click the Click here to reject link**

</td><td>

Reject the delete request. A work note is posted with the name of the person who rejected the request. After a request is rejected, as the user with the sn\_si.analyst role, you are required to submit a new delete request if you determine that the emails should be deleted.

</td></tr><tr><td id="d101619e218">

**Click the link to the security incident record \(SIR0010002\)**

</td><td>

Review the related security incident and any related search data prior to processing the request.

</td></tr></tbody>
</table>    The following image shows an example of the audit trail created by the work notes on the related security incident record for this example. When the request is rejected from the email notification by an approver, a work note is posted with by the person who rejected the request. Johann SecAdmin rejects this request.

    ![Work notes with audit trail for a rejected request.](../image/ms-36-jected-request-notes-new.png)

    In the ServiceNow AI Platform instance of the person who rejected the request \(Johann SecAdmin\), in **Self-Service &gt; My Approvals**, `Rejected` is displayed in the State column.

    After a request is rejected by any single member of the approval group, as the user with the sn\_si.analyst role, you are required to submit a new request to delete these emails if you determine that they should be deleted.

    For this example, after the request is rejected, the user with the sn\_si.analyst role submits a new request.

    Another member of the approval group, John Approver, receives an email similar to the one shown in the preceding example. John Approver can also process this request.

2.  Alternatively, approvers can navigate to **Self-Service &gt; My Approvals** in their ServiceNow AI Platform instances to view and process delete requests.

    To process a request from **My Approvals**, follow these steps.

    1.  Navigate to **Self-Service &gt; My Approvals**.

        ![List of approvals](../image/ms-approvals.png "My Approvals List")

    2.  In the State column, click the requested item.

        In the approval record that is displayed, data about the search, the search request, and the search results are listed.

        ![Approval record from My Approvals](../image/ms-approvals-change.png "Approval details")

    3.  On this record, click **Approve** to approve the request.

        After the request is approved, the system initiates the delete workflow to remove the emails. The following image shows an example of the audit trail created by the work notes on the related security incident record for this example. After this delete request is submitted again, it is approved. Regardless of which method is used to approve a request, the number of successfully deleted emails is posted in a work note.

        ![Work notes logging the audit trail from email search is initiated through emails are successfully deleted.](../image/ms-122-delete-approved-notes.png)

        After the emails are successfully deleted, on the related security incident record, if tagging is enabled, the `Email Delete - Completed` tag replaces the `Email Delete - Initiated` tag.

        In **Self-Service &gt; My Approvals** for the approver \(John Approver\), the state changes from `Requested` to `Approved`.

        In **Self-Service &gt; My Approvals** for other members of the approval group, for example, Johann SecAdmin, the state changes to `No Longer Required` after the request is approved.

3.  Alternatively, to confirm that emails are deleted in the Email Search Result record on the related security incident record, follow these steps.

    1.  Navigate to **Security Incidents &gt; Show All Incidents** and locate the phishing-related security incident.

        At the bottom of the record, the related lists are displayed.

    2.  Click the **Email Search** related list.

    3.  Click the name of the search in the Email search column \(`Phish "log in to your account"`\).

        The Email Search record is displayed. If the Email Search related list is not visible, click the **Show All Related Lists**link.

    4.  Click the **Email Search Results** related list.

        In the Search date column, the email search and delete actions are displayed with corresponding dates.

    5.  In the Search date column, click the item that corresponds to the delete action.

        In the Email Search Result record that is displayed, the Was deleted column status shows that the email is deleted \(`true`\).

        ![Was deleted column highlighted on Email Search Result record.](../image/ms-36-delete-confirmed-esr.png)

        You have successfully approved email delete requests from both an email notification and an approval record and confirmed that emails are deleted. For more information about locating the Email Search Result record, see [Define email search criteria and request a search on the Microsoft Exchange Online service](verify-expected-results-ms-exchange-online.md).


**Parent Topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Previous topic:**[Request delete approval for emails on Microsoft Exchange online service](ms-delete-email.md)

**Next topic:**[Recover deleted emails on the Microsoft Exchange Online service](ms-recover-deleted-emails.md)

