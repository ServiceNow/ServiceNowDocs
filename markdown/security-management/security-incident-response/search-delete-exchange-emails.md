---
title: Search for and delete phishing emails
description: Deleting phishing emails can help reduce exposure to a specific attack across an organization. You can manage phishing emails on your email server by searching, granting approvals, and deleting them.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Managing security incidents and inbound requests, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Search for and delete phishing emails

Deleting phishing emails can help reduce exposure to a specific attack across an organization. You can manage phishing emails on your email server by searching, granting approvals, and deleting them.

## Before you begin

Roles required: sn\_sec\_cmn.cap\_email\_read

You can determine how many users were targeted by a phishing attack by querying an email record associated with a security incident.

Supported software:

-   Microsoft® Exchange Server 2010

Limitation: When searching the body of emails, you can search a maximum of 1,500 mailboxes.

## About this task

This feature is used by the [Security Operations Integration - Email Search and Delete flow](../../security-operations-common/task/secops-integ-email-search-delete.md) to run a query against your email server. Depending on the search criteria you select, the search identifies all emails within a phishing attack, and returns the total number of emails affected or details from the emails affected.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show Open Incidents**.

2.  Choose a security incident.

3.  If the **Email Search** related list is not visible, click the **Show All Related Links** related link.

4.  Click the **Email Search** related list.

    ![Email Search related list](../image/email-search.png)

5.  Click **New**.

6.  Fill in the fields, as appropriate.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the search query|
    |Query from criteria|A preview of the query run on the email server. Generated from all the associated active search criteria records.|
    |Description|Describe what the search query is looking for.|

7.  Right-click in the form header and select **Save**.

    ![Email Search Criteria related list](../image/email-search-criteria.png)

8.  Click the **Email Search Criteria** tab and click **New**.

9.  Fill in or edit the fields, as appropriate.

<table id="table_ujm_xzf_n1b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email search

</td><td>

Displays the name of the email search. You can change it if needed.

</td></tr><tr><td>

Search field

</td><td>

Field to search in the email server.

 The search field has the following choices:

 -   **Subject**

This criteria searches for emails that contain the Subject line text specified in the **Search text** field. For emails that meet this search criteria, the total number of phishing emails and the details of each email, including the email date received, email read status, recipient, and message ID, are returned.

-   **From**

This criteria searches for emails that contain the sender's full email address \(for example, jane.doe@abc.com\) specified in the **Search text** field. For emails that meet this search criteria, the total number of phishing emails and the details of each email, including the email date received, email read status, recipient, and message ID, are returned.

**Note:** You cannot use the **From** and **Recipient** fields in the same query.

-   **Recipient**

This criteria searches for emails that contain the recipient's full email address \(for example, john.doe@abc.com\) specified in the **Search text** field. It also searches for emails in the To, Cc, and Bcc fields. For emails that meet this search criteria, the total number of phishing emails and the details of each email, including the email date received, email read status, recipient, and message ID, are returned.

**Note:** You cannot use the **From** and **Recipient** fields in the same query.

-   **Body**

This criteria searches for emails that contain the body text specified in the **Search text** field. For emails that meet this search criteria, the total number of phishing emails is returned.

**Note:** When searching the body of emails, you can search a maximum of 1,500 mailboxes.

-   **Cc:**

This criteria searches for emails that contain the Cc full email address \(Ex: jane.doe@abc.com\) specified in the **Search text** field. For emails that meet this search criteria, the total number of phishing emails is returned.

-   **Bcc:**

This criteria searches for emails that contain the Bcc full email address \(Ex: jane.doe@abc.com\) specified in the **Search text** field. For emails that meet this search criteria, the total number of phishing emails is returned.

-   **Attachment**

This criteria searches for emails that contain either the attachment file name or attachment contents specified in the **Search text** field. For emails that meet this search criteria, the total number of phishing emails is returned.

**Note:** Only plain text attachments are supported for searching the attachment contents.

-   **Retention Policy**

This criteria searches for emails that contain retention policy numbers specified in the **Search text** field. For emails that meet this search criteria, the total number of phishing emails is returned.

</td></tr><tr><td>

Active

</td><td>

Select this check box to activate this email search query.

</td></tr><tr><td>

Operator

</td><td>

Possible values are AND and OR. You can define how search criteria are combined to run in the email server.

</td></tr><tr><td>

Order

</td><td>

The order in which the search query is built from the search criteria.

</td></tr><tr><td>

Search Text

</td><td>

The text to search for. Single quotation marks, double quotation marks, and colons are not supported.

</td></tr></tbody>
</table>10. Click **Submit**.

11. Repeat as needed to define additional search criteria.

12. You can view the results of the search by clicking the **Email Search Results** tab.

    ![Email Search Results](../image/EmailSearchResults.png)

    Each line of the Email Search Result Entries form represents a separate email.

13. After you have created a search criteria record, two buttons appear in the Email Search form: **Delete from Email Server\(s\)** and **Search on Email Server\(s\)**.

    ![Email search for phishing threats](../../security-operations-common/image/email-search-phishing.png)

14. To search for emails in the selected server that meet the search criteria you defined, click **Search on Email Server\(s\)**.


