---
title: Configure the Microsoft Exchange Online integration
description: After you’ve installed the application from the ServiceNow Store, configure it to connect to your ServiceNow AI Platform instance. This activation activates the search and delete workflows.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Microsoft Exchange Online integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Configure the Microsoft Exchange Online integration

After you’ve installed the application from the ServiceNow Store, configure it to connect to your ServiceNow AI Platform instance. This activation activates the search and delete workflows.

## Before you begin

Role required: sn\_si.admin

## Procedure

1.  In your ServiceNow AI Platform instance, navigate to **Security Operations** &gt; **Integrations** &gt; **Integration Configurations**.

2.  Locate the Microsoft Exchange Online tile.

3.  Click **Configure**.

    ![Microsoft Exchange Online configuration tile.](../image/ms-7-24-config.png)

4.  In the Microsoft Exchange Online Configuration dialog that is displayed, click **Configure Exchange Online**.

    An example of a completed and validated form follows the table.

    ![Configure Exchange Online link highlighted.](../image/ms-configure-tile.png "Configure Microsoft Exchange Online")

<table id="choicetable_erq_lmy_c2b"><thead><tr><th align="left" id="d290064e141">

Option

</th><th align="left" id="d290064e144">

Description

</th></tr></thead><tbody><tr><td id="d290064e150">

**__Connection Settings tab__**

</td><td>

 

</td></tr><tr><td id="d290064e161">

**Tenant**

</td><td>

The Microsoft Exchange Online tenant that you want to perform searches on. This text is the unique name that appears after @ for email addresses for your organization. For this example, `snowsecops.onmicrosoft.com` is the tenant \(domain\).

</td></tr><tr><td id="d290064e176">

**Certificate Thumbprint**

</td><td>

A certificate thumbprint is a hash of a certificate, computed over all certificate data and its signature. Thumbprints are used as unique identifiers for certificates, in applications when making trust decisions, in configuration files, and displayed in interfaces.

</td></tr><tr><td id="d290064e188">

**OAuth Application ID**

</td><td>

The Application \(client\) ID that was generated for the account that you created in the Microsoft Azure portal. For more information, see [Set up your Microsoft Azure account](ms-azure-account.md).

</td></tr><tr><td id="d290064e217">

**OAuth Client Secret**

</td><td>

Password \(client secret\) for the account that you created in the Microsoft Azure portal. For more information, see [Set up your Microsoft Azure account](ms-azure-account.md).

</td></tr><tr><td id="d290064e245">

**__Additional Settings tab__**

</td><td>

 

</td></tr><tr><td id="d290064e256">

**Email Search Window \(days\)**

</td><td>

The email search history range in number of days. The integration searches for email messages that have been sent or received in the Microsoft Exchange Online server for the number of calendar days that you enter. You’re required to enter a value between 1-30. 30 days is the default and the maximum number of days you can enter for a search. Entering a low number of days in the search window range improves response time, but you may not capture all matched messages as a result. This global setting is for all searches.

Prior to executing the email search, there are no parameters that permit you to change this value for individual searches.

</td></tr><tr><td id="d290064e273">

**Maximum Search Duration**

</td><td>

Use this option to set the search timeout threshold. If the timeout threshold is reached, the search ends and no results are displayed. You can specify a default value of 90 minutes and a maximum value of 240 minutes. By setting this threshold, you can avoid endless search loops that could cause performance issues on the Microsoft Exchange Online tenant and the ServiceNow instance.

</td></tr><tr><td id="d290064e288">

**Tagging**

</td><td>

Security tag. Default is selected.

 When enabled, security tags are automatically applied to related security incidents when search and delete capabilities are initiated and successfully completed.

 The default tag names are displayed, but tag names and colors can be edited.

 For more information, see [Edit security tags for the Microsoft Exchange Online integration](ms-edit-tags.md).

</td></tr><tr><td id="d290064e323">

**Recover Deleted Emails**

</td><td>

Default is selected. This item only applies to emails that you have deleted using this integration. If you don’t want users in your organization to have access to the emails that you’ve deleted, verify that this check box is cleared.

If the check box is cleared, the emails that you delete using the workflow of this integration are permanently deleted and placed in the Purges folder. This folder is a sub folder within the Recoverable Items folder on Microsoft Exchange Online that a user normally can’t access.

If you want users to recover the emails you delete, select this check box.

If this check box is selected, depending on how the user's account is configured in Microsoft Exchange Online, the emails you delete using the workflow of this integration are placed in the Deleted Items folder in the mailbox of the user. If an account is configured so that the user can view the Deleted Items folder in their mailbox, the user can recover the emails you delete from their Microsoft Exchange Online account. For more information, see [Recover deleted items or email in Outlook Web App](https://support.office.com/en-us/article/recover-deleted-items-or-email-in-outlook-web-app-c3d8fc15-eeef-4f1c-81df-e27964b7edd4?ui=en-US&rs=en-US&ad=US).

</td></tr><tr><td id="d290064e352">

**Search Completion Notification**

</td><td>

Select this option to enable notifications when the search is completed. If the **Enable** check box is selected, you’ll receive notifications if any matching emails are found. If the check box is cleared, search completion notifications aren’t sent.

</td></tr><tr><td id="d290064e367">

**Approvals**

</td><td>

Request approval to delete emails. Default is cleared.

 When the check box is cleared, the optional approval process for requesting prior permission before deleting emails from the Microsoft Exchange Online service is disabled.

 Verify that this check box is cleared if you want to grant your security incident analyst permission to delete emails without requesting prior permission.

 If enabled, a request is submitted via email to each member of an approval group. From the list, select an approval group from the list.

 After a request is submitted to an approval group, only one approval is required from the group to complete the request. Any member of the approval group has approval authority. Having a group with more than one person with approval permission ensures that these requests are processed in a timely way.

</td></tr><tr><td id="d290064e394">

**Failure Notifications**

</td><td>

Select the check box to enable failure notifications when the search or delete action fails due to invalid OAuth credentials. If Enabled, failure notifications are sent through email to each member of the failure notifications group when OAuth credentials are invalid. If the check box is cleared, no failure notifications are sent.

</td></tr><tr><td id="d290064e406">

**Email Result Threshold**

</td><td>

From version 10.3 or later, you can specify an email delete threshold for approvals. If the number of emails being deleted is greater than or equal to the value specified here, the Delete request must be approved before the Delete action is invoked. If the threshold value is set to 1, every Delete request must be approved.

</td></tr></tbody>
</table>    ![Configure the Connection Settings tab](../image/ms-exchange-online-config.png "Microsoft Exchange Online Connection Settings")

    ![Configure the Additional Settings tab.](../image/security-tags-failure-notifi.png "Microsoft Exchange Online Additional Settings")

5.  Choose one to continue.

    |Option|Description|
    |------|-----------|
    |**Save**|Save your edits. This action doesn’t verify your connection.|
    |**On the Connection Settings tab, click Validate.**|This action validates your Certificate authentication, your MID server connection, and OAuth credentials. If your credentials are valid, the **Validate** button and both indicators are green.|


If an error message is displayed, or one or more of the indicators to the right of the Validate button are red, verify that the user account credentials you entered are valid. Enter your credentials and click **Save** again.

![Validation unsuccessful with red indicator.](../image/ms-validatation-colors.png "Validation unsuccessful")

Refer to the following table for more information about the **Validate** button and the colored icons.

<table id="table_pwz_zdc_sgb"><thead><tr><th>

State of Validate button and indicators

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Validate button is green and all the small colored indicators are green.

</td><td>

Indicates that the MID Server connection and the credentials are valid.

</td></tr><tr><td>

Validate button is light red with a blue border and one or all the small colored indicators are orange.

</td><td>

The validation is in process. Validation may take a few more moments to complete.

</td></tr><tr><td>

Validate button is light red and one or all of the small colored indicators are red.

</td><td>

-   Exchange Online certificate-based authentication or OAuth credentials button is red: Indicates that the Exchange Online certificate-based authentication or OAuth credentials are invalid.
-   Exchange Online certificate-based authentication and MID Server Ready buttons are red: Indicates that the MID Server isn’t reachable and therefore, Exchange Online certificate-based authentication through the MID Server has failed.
-   Exchange Online certificate-based authentication indicator is red but MID Server Ready button is green: Indicates that the MID Server is active and configured correctly, but the Exchange Online certificate-based authentication are incorrect.

</td></tr></tbody>
</table>**Parent Topic:**[Microsoft Exchange Online integration](../concept/ms-exchange-online-lookups.md)

**Previous topic:**[Install Microsoft Exchange Online application](install-and-configure-ms-exchange-online.md)

**Next topic:**[Define email search criteria and request a search on the Microsoft Exchange Online service](verify-expected-results-ms-exchange-online.md)

