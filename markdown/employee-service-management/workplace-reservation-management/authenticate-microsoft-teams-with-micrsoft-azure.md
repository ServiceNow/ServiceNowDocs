---
title: Authenticate Microsoft Teams with Microsoft Azure
description: Set up authentication with Microsoft Azure to connect Microsoft Teams with Workplace Reservation Management application.
locale: en-US
release: australia
product: Workplace Reservation Management
classification: workplace-reservation-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Connect Workplace Reservation Management with Microsoft Teams, Configure Workplace Reservation Management portal, Workplace Reservation Management, Workplace Service Delivery, Employee Service Management]
---

# Authenticate Microsoft Teams with Microsoft Azure

Set up authentication with Microsoft Azure to connect Microsoft Teams with Workplace Reservation Management application.

## Before you begin

Role required: Azure Active Directory administrator

## About this task

In order for Workplace Reservation Management to be able to generate Microsoft Teams meeting link and get the recordings, via Microsoft Graph API, permissions must be added.

## Procedure

1.  Log in to the Microsoft Azure portal.

2.  Navigate to **Azure Services** &gt; **Azure Active Directory** &gt; **Manage** &gt; **App registrations**.

3.  If you do not have an app registration, click **New registration**.

    1.  On the form, enter the **Name** of the registration.

    2.  Select the **Supported account types** of your choice.

    3.  Specify the **Redirect URL**.

        Specify the following details:

        1.  Select the platform as **Web**.
        2.  Enter the URL in the following format: https://&lt;instance-Name&gt;.service-now.com/oauth\_redirect.do
4.  If you already have an app registration, select the app registration.

    1.  Navigate to **Manage** &gt; **Authentication**.

    2.  Navigate to **Add a platform** &gt; **Web applications** &gt; **Web**.

    3.  On the Configure Web form, fill the fields.

        |Field|Description|
        |-----|-----------|
        |Redirect URL|Enter a URL in the format: https://\[instance\].service-now.com/oauth\_redirect.do|
        |Implicit grant|Check **Access tokens**, and **ID tokens**|

    4.  Click **Configure**.

5.  Add a client secret.

    1.  Navigate to **Manage** &gt; **Certificates and secrets**.

    2.  Click **New client secret**

    3.  In the **Description** field, enter a short description about the secret.

    4.  Under **Expires**, select an expiry.

    5.  Click **Add**.

    6.  After adding, in the Client secrets section, copy the value by clicking **Copy to clipboard**.

6.  Add a permission.

    1.  Navigate to **Manage** &gt; **API permissions**.

    2.  Click **Add a permission**.

    3.  Select **Microsoft Graph**.

    4.  Select **Application permissions**.

<table id="table_qph_d2q_rfc"><thead><tr><th>

Permission name

</th><th>

Description

</th><th>

Required to

</th></tr></thead><tbody><tr><td>

User.Read.All

</td><td>

Read all users profiles

</td><td>

Create virtual meeting link

</td></tr><tr><td>

OnlineMeetings.ReadWrite.All

</td><td>

Read and create online meetings

</td><td>

Create virtual meeting link

</td></tr><tr><td>

Directory.Read.All

</td><td>

Read directory data

</td><td>

Create virtual meeting link

</td></tr><tr><td>

Chat.Read.All

</td><td>

Read all chat messages**Note:**

This is optional and is required only to retrieve meeting recordings.

</td><td>

Retrieve meeting recording

</td></tr></tbody>
</table>    5.  Select **Chat.Read.All**, **Directory.Read.All**, **OnlineMeetings.ReadWrite.All** and **User.Read.All**.

        **Note:** Select **Chat.Read.All** to retrieve the meeting recordings.

    6.  Click **Add permissions**.

    7.  On the Configured permissions screen, click **Grant admin consent for ServiceNow**.

    8.  Click **Yes**.

        A confirmation message is displayed that admin consent is granted for the requested permissions.

7.  Configure application access policy and allow applications to access online meetings.

    1.  Open the Windows' PowerShell as an administrator to run scripts.

    2.  Identify the app's application \(client\) ID and the user IDs of the users on whose behalf the app is authorized to access online meetings.

    3.  Connect to Skype for Business PowerShell with an administrator account.

    4.  Create an application access policy containing a list of app IDs.

        Run the following cmdlet, replacing the Identity, AppIds, and Description \(optional\) arguments.

        ```
        New-CsApplicationAccessPolicy -Identity Test-policy -AppIds "ddb80e06-92f3-4978-bc22-a0eee85e6a9e", "ccb80e06-92f3-4978-bc22-a0eee85e6a9e", "bbb80e06-92f3-4978-bc22-a0eee85e6a9e" -Description "description here"
        ```

    5.  Grant the policy to the user to allow the app IDs contained in the policy to access online meetings on behalf of the granted user.

        Run the following cmdlet, replacing the PolicyName and Identity arguments.

        ```
        Grant-CsApplicationAccessPolicy -PolicyName Test-policy -Identity "748d2cbb-\
        3b55-40ed-8c34-2eae5932b22a"
        ```

    6.  Grant the policy to the whole tenant \(Applies to users who don’t have an application access policy assigned\).

        Run the following cmdlet, replacing the PolicyName argument.

        ```
        Grant-CsApplicationAccessPolicy -PolicyName Test-policy -Global
        ```

    **Note:** All employees who can create or update reservations must be included in the application access policy.


## Result

The Microsoft Teams is set up with Microsoft Azure.

**Note:** For more information about allowing applications to access online meetings, see [Microsoft documentation](https://learn.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy#configure-application-access-policy).

**Parent Topic:**[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

**Previous topic:**[Connect Workplace Reservation Management with Microsoft Teams](connect-rsv-mgmt-with-teams.md)

**Next topic:**[Setup OAuth connectivity with Microsoft Teams Connections spoke for virtual meeting](setup-connectivity-between-servicenow-and-microsoft-teams-connection-spoke.md)

