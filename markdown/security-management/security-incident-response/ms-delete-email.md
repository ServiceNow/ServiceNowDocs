---
title: Request delete approval for emails on Microsoft Exchange online service
description: After an email search is successfully completed and matching messages are identified, you can permanently delete all the suspicious emails from the Microsoft exchange online service that are related to the security incident and phishing campaign.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Microsoft Exchange Online integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Request delete approval for emails on Microsoft Exchange online service

After an email search is successfully completed and matching messages are identified, you can permanently delete all the suspicious emails from the Microsoft exchange online service that are related to the security incident and phishing campaign.

## Before you begin

Role required: sn\_si.analyst

The system performs deletions on your latest successful search results.

## About this task

If the approvals and email notifications are enabled, send a request to delete emails to an approval group prior to email removal.

Email search results are displayed with any messages that have been received. To ensure that phishing emails are successfully deleted, the delete results are posted to the work notes of the associated security incident. If tagging is enabled, a security tag is also displayed on the related security incident. If the email is not successfully deleted, you are also notified in the work notes.

Depending on your organizational policies, you may need to request approval prior to deleting phishing emails. The delete approval process requires information on the number of emails to be deleted and, potentially, access to other message details. For processing the delete request, in an email notification, an approver is provided with the matching email message count, the security incident link for access to complete message details, and approve or reject links. The links in this email permit an approver to accept or reject the delete request from the email notification. A full audit trail with a time stamp is also available that tracks when the approval status changed in work notes. If an approval group is assigned, one user in the group may process the request for the entire group. Each member of the approval group receives an email notification for the request.

As a user with the sn\_si.analyst role, if you determine that emails require remediation, follow the required steps to delete emails. If approvals are enabled, request approval to delete emails from the Microsoft Exchange Online service.

## Procedure

1.  Navigate to **All** &gt; **Security Incident &gt; Show All Incidents**.

2.  Click the **Email Search** related list.

3.  With the Email Search related list selected, in the Email search column, click the name of your search.

    The search results are displayed in the Email Search Results related list.

    For this example, this search has found emails that match your search criteria. There are two search actions listed on the record. One search has no matches \(0\), and the other search has one matching email \(1\).

    ![Email search record with Result set size highlighted.](../image/ms-email-search-results.png "Email Search Result set size")

4.  To delete email items associated with a search, to the left of the Search Date column, select the check box of a search result set.

    You can select a single result set, or multiple result sets from the list.

5.  Select the result sets that you want to delete.

    ![Actions on selected rows choise list expanded and Delete Emails from Exchange Online highlighted.](../image/ms-email-delete-search.png "Delete Emails from Exchange Online")

6.  At the bottom of the Email Search Results related list, from the Actions on selected rows list, select **Delete Emails from Exchange Online** to delete all the email items associated with one or more result sets from the Exchange Online server.

    If a result set contains more than one email, you are not required to open the Email Search Result record and select individual emails to delete them. All emails items with a status of `false` in the Was deleted column in the Email Search Result record are deleted after you select **Delete Emails from Exchange Online**.

    If an email item in a result set has already been deleted, the status in the Was deleted column in the Email Search Result record is `true`. These items are not deleted again.

    If the approval option is disabled during the configuration step, after you select **Delete Emails from Exchange Online**, the emails associated with the result set are deleted. The result set itself is not deleted. However, the status of all the deleted email items of the result set is updated to `true` in the Was deleted column of the Email Search Result record. For more information on the approval feature, see [Configure the Microsoft Exchange Online integration](msx_configure.md).

    ![Was deleted column on Email Search Result record highlighted.](../image/ms-email-search-false.png "Email deletion details")

    These emails are deleted from the Microsoft Exchange Online tenant that you performed the searches on. A work note is displayed if the emails are successfully deleted.

    On the security incident record, the `Email Delete - Completed` security tag is displayed.

    ![Security incident with Email Delete Completed security tag highlighted.](../image/ms-email-search-completed.png "Email Delete - Completed security tag")

    If approvals are disabled for delete requests, you have successfully deleted emails from the Microsoft Exchange Online tenant.

    If approvals are enabled for delete requests during the configuration step, after you select **Delete Emails from Exchange Online**, an email notification is sent to each member of the approval group that you selected during the configuration step.

    If tagging is enabled during the configuration step, the `Email Delete - Initiated` security tag is displayed on the related security incident record. For more information on tagging, see [Configure the Microsoft Exchange Online integration](msx_configure.md).

    Work notes are displayed that a request to delete emails is submitted by the user with the sn\_si.analyst role \(`Hans SecAnalyst`\).

    ![Work notes with request submitted and audit trail.](../image/ms-36-notes-delete-request.png)

    If approvals are enabled, the next step is to process the delete request.

7.  Alternatively, if you want to view the details and individual email items of a search record prior to deleting it or submitting a delete request, follow these steps.

    1.  With the Email Search Results related list selected, in the Search date column, click the date of a search that you want to review.

        ![Search date highlighted on Email Search Results related list.](../image/ms-email-search-details.png "Email search details")

        The following information about the emails is displayed:

        -   Recipients
        -   Sender
        -   Email date received
        -   Email read status \(`true` or `false`\)
        -   Was deleted \(`true` or `false`\)
        -   Deleted By Integration \(`true` or `false`\)

            **Note:**

            Value is set to true when the email is deleted when the analyst initiates the Delete from Email Server\(s\).

            The work notes is updated with the total number of deleted records which includes the records deleted by integration and user.

    2.  After you have reviewed the data, to delete all the emails, or send a request to delete all the emails, click **Delete from Email Server\(s\)**.

        As described in the previous example, if there is more than one email listed on the search result record, you do not need to select the individual emails to remove them. The delete request removes any emails associated with the search when `false` is displayed in the Was deleted column from the latest search results.

        ![Delete from Email Servers button highlighted and callout arrow for check box on Email Search Result record.](../image/failure-notification-delete.png)

    If approvals are enabled, you have successfully submitted a request to delete emails. The security tags and work notes are displayed on the related security incident record as described in the previous example. As an approver, the next step is to process the delete request.


**Parent Topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Previous topic:**[Define email search criteria and request a search on the Microsoft Exchange Online service](verify-expected-results-ms-exchange-online.md)

**Next topic:**[Approve delete email requests for the Microsoft Exchange Online integration](ms-approve-delete.md)

