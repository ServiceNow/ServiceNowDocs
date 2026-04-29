---
title: Set up OAuth 2.0 Authorization Code for Bitbucket Cloud
description: Set up OAuth 2.0 Authorization Code credentials for Bitbucket in DevOps Change Velocity to use a more secure authentication method.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Bitbucket, Integrate, DevOps Change Velocity, IT Service Management]
---

# Set up OAuth 2.0 Authorization Code for Bitbucket Cloud

Set up OAuth 2.0 Authorization Code credentials for Bitbucket in DevOps Change Velocity to use a more secure authentication method.

## Before you begin

The OAuth consumer must be created in the Bitbucket tool with the required permissions before creating the OAuth credential record. You can navigate to **Workspace settings &gt; OAuth consumers &gt; Add consumer** in Bitbucket to add the OAuth consumer. The following permissions must be selected when you create the credentials for OAuth 2.0.

-   Account: Read
-   Projects: Read
-   Webhooks: Read and write
-   Pull requests: Read

The **This is a private consumer** option must be deselected. You must enter your ServiceNow instance URL in the **Callback URL** field in the following format.

```
https://<instanceurl>/oauth_redirect.do
```

![Permissions for Bitbucket OAuth 2.0 - Authorization Code](../image/bitbucket-oauth-permissions-auth-code.png)

You need the **Client Id** and **Client secret** values of your Bitbucket workspace. Client ID of your Bitbucket tool is available in the OAuth consumers section of your workspace settings \(**Workspace settings &gt; OAuth consumers &gt; Add consumer**\) in the **Key** field. Client secret of your Bitbucket tool is available in the OAuth consumers section of your workspace settings \(**Workspace settings &gt; OAuth consumers &gt; Add consumer**\) in the **Secret** field.![OAuth consumer page](../image/bitbucket-oauth-consumer.png)

Role required: admin

## About this task

When you select the credential type as OAuth 2.0 - Authorization Code for Bitbucket Cloud, the repositories for all the workspaces are discovered. This is a limitation from Bitbucket side.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

    The system displays the message **What kind of OAuth application?**

3.  Select **Connect to a third party OAuth Provider**.

    The system displays an empty Application Registries form.

4.  Fill the following fields in the form.

<table id="table_fd2_2xr_4mb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of your Bitbucket tool, which is available in the OAuth consumers section of your workspace settings in the **Key** field of Bitbucket cloud.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of your Bitbucket tool, which is available in the OAuth consumers section of your workspace settings in the **Secret** field of Bitbucket cloud.

</td></tr><tr><td>

Default Grant type

</td><td>

Select **Authorization Code**.

</td></tr><tr><td>

Authorization URL

</td><td>

Enter `https://bitbucket.org/site/oauth2/authorize`

</td></tr><tr><td>

Token URL

</td><td>

Enter `https://bitbucket.org/site/oauth2/access_token`

</td></tr></tbody>
</table>5.  Leave the rest of the form fields as default.

    ![Application Registry form for Bitbucket OAuth credential](../image/bitbucket-oauth-application-registry.png)

6.  Select and hold \(or right-click\) the form header, and select **Save**.

    -   The system validates the OAuth credentials and populates the **Redirect URL** \(Hint: It should match the **User authorization callback URL** previously provided in your Bitbucket Cloud configuration\).
    -   The system populates **OAuth Entity Profile** with **Grant Type** as **Authorization Code**. For example, **OAuth Entity Profile** is created with default **Name**, **My Bitbucket App Provider default\_profile**
7.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

8.  Select **New**.

    The system displays the message **What type of Credentials would you like to create?**.

9.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays an empty OAuth 2.0 Credentials form.

10. Fill in these values.

<table id="table_sxv_zgp_gfb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the record.

</td></tr><tr><td>

Active

</td><td>

Enable

</td></tr><tr><td>

OAuth Entity Profile

</td><td>

Select the default OAuth Entity profile that you created in step 6.

</td></tr><tr><td>

Applies to

</td><td>

Select the MID Servers that can use this credential. For example, select **All MID Servers**.**Note:** You must connect to your Bitbucket tool instance using MID Server to use this credential.

</td></tr><tr><td>

Order

</td><td>

Select the order to apply this credential. For example, enter `100`.

</td></tr></tbody>
</table>11. Save the record.

12. Select the **Get OAuth Token** related link to generate the OAuth token.


**Parent Topic:**[Bitbucket integration with DevOps Change Velocity](../concept/bitbucket-integration-dev-ops.md)

