---
title: Setting up an SFTP user account in Salesforce Marketing Cloud
description: Set up an SSH File Transfer Protocol \(SFTP\) user account to access your Salesforce Marketing Cloud FTP files.Create user accounts for SFTP users in Salesforce Marketing Cloud to access the Contacts Counts report.Set up a file location to connect to an external FTP site when transferring files. The file location contains the site URL, port, and login details that Salesforce Marketing Cloud uses to access your site.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-08-28"
reading_time_minutes: 2
breadcrumb: [Integrating with Salesforce Marketing Cloud, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Setting up an SFTP user account in Salesforce Marketing Cloud

Set up an SSH File Transfer Protocol \(SFTP\) user account to access your Salesforce Marketing Cloud FTP files.

Creating an SFTP user account enables you to access the Contacts Counts reports that are saved at an FTP location. The Contacts Counts report displays the total number of billable contacts in your Salesforce Marketing Cloud account.

## Create an SFTP User Account in Salesforce Marketing Cloud

Create user accounts for SFTP users in Salesforce Marketing Cloud to access the Contacts Counts report.

### Before you begin

Salesforce Marketing Cloud Role required: admin with privileges to create users and roles

### About this task

**Note:** You can create a limited number of active SFTP user accounts per member ID \(MID\). For more information, see [Salesforce documentation](https://help.salesforce.com/s/articleView?id=mktg.mc_overview_add_ftp_accounts.htm&type=5).

### Procedure

1.  From a web browser, open your Salesforce Marketing Cloud instance.

2.  Log in using your admin credentials.

3.  On the page header of your instance, select your profile icon and then select **Setup**.

4.  In the **Quick Find** box, enter `ftp` and then select **FTP Accounts**.

5.  Select **Create User**.

6.  Enter the email address and password for the new user.

7.  In the Authentication Options window, select **Select Password** as the authentication method for the user.

8.  In the Permissions window, select the permissions to apply to each directory.

    **Important:** Each directory inherits the permissions of its subdirectories. Select all the permissions that provide you access to all the folders for viewing, downloading, and managing files.

9.  Permit SFTP connections only from a specific IP address by entering the address in the **Allowlist IPs** field.

10. Select **Add**.

11. Repeat step 9 for each IP address that you want to permit.

    **Note:** If you don't enter any IP addresses, SFTP connections can be opened from any IP address.

12. In the Folders window, select a home directory for the user.

    The user is allowed to access only the selected directory and its subdirectories. You can select the Root folder to see all the directories and subdirectories.

13. Save your changes.

    You can also exclude an SFTP user from password expiration. For more information, see [Salesforce documentation](https://help.salesforce.com/s/articleView?id=000390420&type=1).


## Set Up an External FTP File Location in Salesforce Marketing Cloud

Set up a file location to connect to an external FTP site when transferring files. The file location contains the site URL, port, and login details that Salesforce Marketing Cloud uses to access your site.

### Before you begin

Role required: admin

### Procedure

1.  In your Salesforce Marketing Cloud instance, navigate to **Setup**.

2.  In the **Quick Find** box, enter `file` and then select **File Locations**.

3.  Select **Create**.

4.  In the Properties section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|A unique name that you can recognize when you create an activity in Salesforce Marketing Cloud.|
    |External Key|A unique key that identifies the file location when using the API.|
    |Description|Details to identify the file location when you create an activity in Salesforce Marketing Cloud.|

5.  Select **Enhanced FTP Site Import Directory** as the location type.

6.  Save the file.


**Related topics**  


[Integrate Salesforce Marketing Cloud using basic authentication](integrate-sfmc-basicauth.md#)

[Integrate Salesforce Marketing Cloud using OAuth 2.0](integrate-sfmc-oauth.md#)

