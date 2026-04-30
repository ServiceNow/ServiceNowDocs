---
title: Define email search criteria and request a search on the Microsoft Exchange Online service
description: As a user with the sn\_si.analyst role, define search criteria and submit an email search request based on incident details on a security incident record.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 12
breadcrumb: [Microsoft Exchange Online integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Define email search criteria and request a search on the Microsoft Exchange Online service

As a user with the sn\_si.analyst role, define search criteria and submit an email search request based on incident details on a security incident record.

## Before you begin

Role required: sn\_si.analyst

The figures in this procedure are shown with **Tabbed forms** selected in System Settings. For more information about selecting and clearing tabbed forms, see the section titled, Display tabbed forms in Configuring the form layout on the [ServiceNow Product Documentation website](https://servicenow.com/docs).

Role required: sn\_si.analyst

## About this task

The status of individual messages that match the search query and the results of the search are reported on the security incident record. If email notifications are enabled, you can view the search results from an email message.

Search criteria may include message sender addresses, recipient addresses, or subject names. The following combinations of message Subject, Sender, and Recipient search parameters are often used for finding phishing-related email messages that may be part of a single phish campaign:

-   Find all original emails sent by a phishing account: Search by sender.
-   Find all original emails for a single phishing campaign: Search by subject and sender.
-   Find all emails received for a single phishing campaign \(original and forwarded, any sender\): Search by subject.
-   Find all forwarded emails for a single phishing email from a single user: Search by recipient + subject.
-   Find all phishing-related emails sent to a single user: Search by sender + recipient.

**Note:** Searches are conducted on emails sent or received within last 30 calendar days, unless a shorter search window is configured during the initial setup. A successful email search is required before you can delete emails.

The following example shows you how to initiate a search from a ServiceNow AI Platform security incident. A security incident is created based on the original email of a suspected phishing attack in the Microsoft Exchange Online server of your organization. For this example, the search criteria is Sender \(From\) plus Subject, where From is `phisher@cbazyx.com`, and the Subject is `log in to your account`.

Results for searches on subjects are returned when the search finds text strings that contain key words that match the entered search criteria. In this example, the subject is `log in to your account`. Use the **AND** operator to separate the From and Subject search conditions to return results for all the email messages that contain these given search criteria. The following steps describe how to set up a search that finds only emails that contain subject line text sent by a specific phishing account.

## Procedure

1.  Navigate to **All** &gt; **Security Incident** &gt; **Show All Incidents** and locate the security incident that you are working with.

2.  Alternatively, follow these steps to set and run a filter so that only security incidents created by phishing events are displayed.

    1.  Navigate to **Security Incident** &gt; **Show All Incidents** to open the Security Incidents list.

    2.  In the upper-left corner of the list that is displayed, click the filter icon.

        ![Filtering.](../image/ms-924-si-list-prefilter1.png)

    3.  In the fields that are displayed, select **Short description** &gt; **contains** from the choice lists, then enter **user reported phishing** and click **Run**.

        The phishing-related security incidents are displayed.

        ![Short description column in the Security Incidents list highlighted.](../image/ms-924-si-phishing.png)

    4.  Use the text in the Short description column to help you locate the security incident that you are working with.

    5.  In the Number column, click a security incident to open a record.

3.  Scroll to the bottom of the Security Incident record and click the Email Search related list.

    If the Email Search related list is not displayed, click the **Show All Related Lists** related link to display this related list.

    ![Email Search related list in a security incident record highlighted.](../image/ms-924-si-10009.png)

4.  In the Email Search related list, click **New** to create a new email search record.

    The Email Search form is displayed. If you determine that you want to rerun this search query for the same phishing-related incident with minor modifications, you can use this search query record again. However, it is unlikely that you would use this search for a different phishing-related incident, because phishing campaigns are dynamic and the sender and message fields often change.

5.  To edit an existing search query record, click **Edit**.

6.  On the Email Search form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Information to describe the type of search. For this example, a name for a From + Subject search is `Phish "log in to your account"`.|
    |Description|Information about the search in the email server. An example for this search is `From=phisher@cbazyx.com + Subject=log in to your account`.|

    ![A completed form.](../image/ms-122-new-search-rcd-cmplt.png)

7.  Click **Submit**.

    The security incident is displayed and the name of the email search is displayed in the Email search column in the Email Search related list. Before you can use this new search query, search criteria must be defined for the search record.

8.  To define search criteria, with the Email Search related list selected, in the Email search column, click **Phish "log in to your account"**.

    ![Email Search tab with Email search column highlighted on a security incident.](../image/ms-122-si-new-search-listed.png)

9.  On the Email search record that is displayed, click the Email Search Criteria related list, and click **New**.

    ![New button highlighted.](../image/ms-122-search-criteria-new.png)

10. On the Email Search Criteria form, fill in the fields.

    An example of a completed form follows the table.

<table id="simpletable_a24_ydv_zgb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Email search

</td><td>

Field is populated automatically with the name that you entered for the Email Search record.

</td></tr><tr><td>

Search icon

</td><td>

Lookup using list. A list of saved searches. Click the icon to open a list of saved email searches. Click an item in this list to remove the current search and select a previously saved email search.

</td></tr><tr><td>

Information icon

</td><td>

Icon used to view the Email Search record. Click the icon to view the email search record.

</td></tr><tr><td>

Search field

</td><td>

Search criterion \(**Subject**, **From**, or **Recipient**\). Select the search criterion from the choice list and define a value that you want to search for in the text field. For this example, start with From `phisher@cbazyx.com` \(the email address of the sender of the phishing email\).

</td></tr><tr><td>

Active

</td><td>

Option for activating the search.The search is activated by default.

 If you clear this option, this record is not included in a search.

</td></tr><tr><td>

Operator

</td><td>

Operators \(**AND**, **OR**\) to further define your search. **AND**: The system searches for the conditions separated by **AND** and returns results only if all the conditions are met. For the sender-plus-subject search, use the **AND** operator so that both search conditions are met during the email search.

 For this example, use the **AND** operator so that the query is From \(Sender\) = `phisher@cbazyx.com` **AND** Subject = `log in to your account`.

 **OR**: The system searches and returns results if any of the conditions separated by **OR** are met.

 An example is From \(Sender\) = `phisher@cbazyx.com` **OR** From \(Sender\) = `phisher-2@cbazyx.com`.

</td></tr><tr><td>

Order

</td><td>

If you enter more than two search conditions, use Order to prioritize the conditions. 100 is the default. Enter a value between 1 and 100 for each condition, for example, 100, 95, 90, 80. The condition with the lowest number assigned has the highest search priority within a group of conditions.

</td></tr><tr><td>

Search text

</td><td>

The text values \(key words\) for the search \(email addresses or subject lines\).The search field contains the text used in the search, for example, `phisher@cbazyx.com`.

 For the search to return results accurately for Sender \(From\) and recipient searches, the search strings must match exactly. For subject searches, the search string can contain key words that are part of a larger string. For example, a subject may contain the exact search string that is matched in a forwarded or a response message header such as `FW: log in to your account and change your password immediately`.

For example, `Log in to your account` are exact key words in the string `log in to your account and change your password immediately`. No wildcard \(\*\) designation is required to support a contains type of search. Currently, no filtering method exists for matching an exact search string that is not part of a larger text string.

</td></tr></tbody>
</table>    ![Email Search Criteria form](../image/ms36-search-criteria-from.png)

11. Click **Submit**.

    The Email Search record is displayed. In the **Query from criteria** field, the search criteria you added for the Sender \(From\) is displayed.

    ![Email Search record](../image/ms36-from-criteria.png)

12. To update this email search criteria with more information so that the query includes the subject-plus-sender condition that you want, follow the steps to add another search condition.

    1.  In the Email Search Criteria related list, click **New**.

        ![Email Search Criteria related list](../image/ms36-search-criteria-new-button-subj.png)

    2.  From the **Search field**list on the Email Search Criteria record that is displayed, select **Subject**.

    3.  From the Operator list, select**AND** or **OR**.

        If you select **OR**, the search returns results if either key words in the subject line text string are matched, or the email address condition is matched. **AND** is selected for this example so that the search returns results only for emails that contain the key words of the subject text string and that match the email address of the sender.

    4.  In the **Search text** field, enter the value for subject line text, `log in to your account`.

        ![Search text field with text string.](../image/ms-122-subj-search-criteria.png)

    5.  Click **Submit**.

        The new condition is displayed in the Email Search Criteria related list, and both conditions are displayed in the **Query from criteria** field separated by the **AND** operator.

        ![New condition is displayed in the Email Search Criteria related list](../image/ms36-subj-plus-search-criteria.png)

    6.  If you have more than two search conditions, and you select **AND** to separate each condition, set the order value to prioritize them.

    7.  Continue to add, modify, or remove search criteria as desired and click **Update** to save your changes to the record.

13. Choose one option to continue.

<table id="choicetable_uyx_fxn_l2b"><thead><tr><th align="left" id="d311021e891">

Option

</th><th align="left" id="d311021e894">

Description

</th></tr></thead><tbody><tr><td id="d311021e900">

**Update**

</td><td>

Update and save your changes to the record.

</td></tr><tr><td id="d311021e909">

**Search on Email Server\(s\)**

</td><td>

Initiate a search on the servers with the criteria that you saved on the Email Search Criteria record.

</td></tr><tr><td id="d311021e918">

**Delete**

</td><td>

Delete this Email Search record from your ServiceNow AI Platform instance. This action does not delete the actual email messages. It only deletes the search record used for finding messages.A dialog box is displayed. If you click **Delete**, the email search results and email search criteria for this search record are deleted.

 ![Confirmation dialog box to delete an email search record.](../image/ms-924-confirm-delete-rcd.png)

 If a record has search results, the following warning is displayed.

 ![Confirmation dialog box for search result record.](../image/ms-warning-dialog.png)

</td></tr></tbody>
</table>14. To initiate an email search, on the email search record, click **Search on Email Servers\(s\)**.

    A message is displayed that indicates the search request is submitted.

    On the Security Incident record, a work note is displayed indicating that a search has been initiated.

    ![Work note logs that a search is initiated.](../image/ms-122-search-initiated-note.png)

    If tagging is enabled, at the top of the Security Incident record, the `Email Search - Initiated` security tag is displayed.

    ![Email search initiated security tag highlighted.](../image/ms-122-si-initiate-search-tag.png)

    After the search is successfully completed, if email notifications are enabled, an email is sent to the email address of the individual who initiated the search.

    In this example, the user with the sn\_si.analyst role, `Hans SecAnalyst`, submitted this search. The following image shows that this notification is sent to an account in Microsoft Exchange Online. However, these notifications can be sent to a different email service, as required.

    This notification lets you view any matched results that require follow-up and deletion. The following example shows that there is one email that matched the search criteria. An Email search result link to the email search result record in your ServiceNow AI Platform instance is also provided. If you want to view the search record, click this link.

    ![Email notification for email search submitted by security analyst.](../image/ms-122-email-notification.png)

15. From this email, to view the search results, click the **Email search result** link.

    The email search result record is displayed. On this record, you can verify and review the following data.

    -   In the **Raw data** field, the email count for the number of emails that matched the search criteria `{"count":1}`, and the mailbox addresses where the emails were found are displayed \["`JuanCustomer@nowsecopslab.onmicrosoft.com"]`.
    -   In the Recipients column, the recipient is \(`JuanCustomer@nowsecopslab.onmicrosoft.com`\).
    -   In the `Sender` column, the source of the email is displayed.
    -   In the `Email date received` column, the date and time the email was received is displayed to help you track phishing campaign time lines.
    -   In the `Email read status` column, the email in this example has not been read \(`false`\). If an email has been read, `true` is displayed.
    -   In the `Was deleted` column, the email in this example has not been deleted. If an email has been deleted, `true` is displayed.
    ![Raw data field](../image/ms36-search-results2.png)

16. Alternatively, to view the search results from the security incident, follow these steps.

    1.  Navigate to **Security Incident** &gt; **Incidents** and open the security incident that you are working with.

        At the top of the record, when the search is successfully completed, the `Email Search - Completed` security tag replaces the `Email Search - Initiated` security tag.

        ![Email Search Completed security tag highlighted.](../image/ms-122-search-cmplt-tag.png)

        Work notes are displayed that the search is successfully completed and that one matching email was found.

        ![Work notes logging matched emails are found.](../image/ms-notes-search-cmplt.png)

    2.  Scroll to the bottom of the Security Incident record and click the Email Search related list.

        If the Email Search related list is not displayed, click the**Show All Related Lists** related link to display this related list.

        ![Email Search related list on the Security Incident record.](../image/ms-122-email-search-tab-populated.png)

    3.  With the Email Search related list selected, in the Email search column, click the name of your search.

        ![Email search column with name of search highlighted.](../image/ms-122-search-selected.png)

    4.  In the Email Search record, click the Email Search Results related list.

    5.  In the Search date column, click the date of your search to display the data.

        The email search result record is displayed.

        ![The email search result record is displayed.](../image/ms36-search-results2.png)

    After an email search is successfully completed, evaluate the results. If you determine that emails require remediation, you are now ready to delete emails, or request delete approval.


**Parent Topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Previous topic:**[Configure the Microsoft Exchange Online integration](msx_configure.md)

**Next topic:**[Request delete approval for emails on Microsoft Exchange online service](ms-delete-email.md)

