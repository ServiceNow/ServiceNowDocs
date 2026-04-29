---
title: OAuth 2.0 credentials for GitHub Apps - JWT
description: Perform the following steps to integrate your GitHub Apps using the JWT bearer token.Create a custom GitHub App from your GitHub account to enable OAuth 2.0 authentication with your ServiceNow instance.Generate a Java KeyStore \(JKS\) certificate for the JWT authentication.Enable the JWT Bearer Grant token authentication by attaching the valid GitHub Java KeyStore \(JKS\) certificate to your ServiceNow instance.Create a JSON Web Token \(JWT\) signing key to assign to your GitHub Java KeyStore certificate.Add a JSON Web Token \(JWT\) provider to your ServiceNow instance for GitHub.Use the information generated during GitHub App account configuration to register GitHub as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create a credential record to the GitHub App provider previously created to authorize actions.
locale: en-US
release: australia
product: DevOps Change Velocity
classification: devops-change-velocity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Setting up GitHub OAuth 2.0 credentials for DevOps Change Velocity, GitHub, Integrate, DevOps Change Velocity, IT Service Management]
---

# OAuth 2.0 credentials for GitHub Apps - JWT

Perform the following steps to integrate your GitHub Apps using the JWT bearer token.

**Before you begin**

Role required:

-   oauth\_admin in DevOps Change Velocity.
-   Admin account in GitHub.

    **Note:** The OAuth 2.0 JWT grant type is supported for GitHub &amp; GitHub Enterprise with MID server.


## Configure the GitHub App in your GitHub account \(JWT\)

Create a custom GitHub App from your GitHub account to enable OAuth 2.0 authentication with your ServiceNow instance.

### Before you begin

GitHub requirement: GitHub App configured to integrate with ServiceNow

Role required: No instance role required

### About this task

Complete these steps from your GitHub account. See [Building GitHub Apps](https://developer.github.com/apps/building-github-apps/) on the GitHub Developer site for instructions on creating and configuring custom applications.

### Procedure

1.  From your GitHub account, create your GitHub App by navigating to **Developer Settings** &gt; **GitHub Apps**.

2.  In the **Homepage URL** field, enter `https://<instance-name>.service-now.com`.

3.  In the **User authorization callback URL** field, enter `https://<instance-name>.service-now.com/oauth_redirect.do`.

4.  In the **Identifying and authorizing users** section, deselect the **Expire user authorization tokens** field.

5.  In the **Webhook** section, select the **Active** field.

6.  In the **Webhook URL** field, enter `https://<instance-name>.service-now.com/api/sn_devops/v2/devops/tool/apps?toolId=<Tool ID>`, where Tool Id is your GitHub tool id \(sys\_id\) from DevOps Change Velocity.

    **Note:**

    If you are newly creating the tool and don't have the Tool ID, you can enter the webhook URL without the Tool ID and configure it later. To configure later:

    1.  Navigate to the connected tool's tool record page.
    2.  Select **Configure GitHub App**, then select **Auto configure with existing token**.

        ![Auto configure with existing token.](../image/github-jwt-config-01.png)

    This configures the Webhook URL of the GitHub App automatically.

    You can get the Tool ID in one of the following ways:

    -   While connecting with the tool in DevOps Change Velocity, the Tool Id is available in the page URL. For example, `https://<instance-name>.service-now.com/.../sn_devops_tool/<Tool ID>/...`.
    -   You can copy the webhook URL from the GitHub tool record page in DevOps Change Velocity, from **Configure** &gt; **Configure manually** &gt; **Webhook URL**.
7.  Leave the remaining fields empty \(default\).

8.  In the **Repository permissions** section, configure the following settings.

<table id="table_j5m_wcs_4mb"><tbody><tr><td>

Action

</td><td>

Read-only

</td></tr><tr><td>

Checks

</td><td>

Read-only

</td></tr><tr><td>

Contents

</td><td>

Read-only

</td></tr><tr><td>

Deployments

</td><td>

Read and write

</td></tr><tr><td>

Environments

</td><td>

Read-only

</td></tr><tr><td>

Metadata

</td><td>

Read-only

</td></tr><tr><td>

Pull requests

</td><td>

Read-only

</td></tr><tr><td>

Secrets

</td><td>

Read-only

</td></tr><tr><td>

Webhooks

</td><td>

Read and write**Note:** Read and write permissions are required to configure webhooks from ServiceNow.

</td></tr></tbody>
</table>    **Note:** If you are already using a GitHub App and you update any of the permissions, you must review and accept those permissions for your GitHub App. You can navigate to your app, and select **Configure &gt; Review request &gt; Accept new permissions**.

9.  Leave the remaining permissions as `No access` \(default\).

10. In the **Subscribe to events** section, select the **Deployment protection rule** option.

11. Save the changes.

12. After creating the GitHub App, generate a new private key and save it to your machine.

13. Install the newly created GitHub App on the accounts of your choice.

    1.  From the GitHub Apps settings page, select your app.

    2.  In the left sidebar, select **Install App**.

    3.  Select **Install** next to the organization or personal account containing the correct repository.

    4.  Install the app on all repositories or select repositories.

        For more information, see [Installing GitHub Apps](https://docs.github.com/en/developers/apps/managing-github-apps/installing-github-apps).


## Generate the Java KeyStore certificate for GitHub

Generate a Java KeyStore \(JKS\) certificate for the JWT authentication.

### Before you begin

Role required: admin

### Procedure

1.  Create a CA signed certificate using the GitHub App private key:

    ```
    openssl req -new -x509 -key <file-name>.pem -out <certificate-name>.pem -days 1095
    ```

2.  Enter the required details.

3.  Create the PKCS 12 file using the GitHub App private key and CA signed certificate:

    ```
    openssl pkcs12 -export -in <certificate-name>.pem -inkey <file-name>.pem -certfile <certificate-name>.pem -out <PKCS-12-file-name>.p12 
    ```

4.  Provide the export password.

5.  Create the JKS file:

    ```
    keytool -importkeystore -srckeystore <PKCS-12-file-name>.p12 -srcstoretype pkcs12 -destkeystore <JKS-certificate-filename>.jks -deststoretype JKS
    ```

6.  Provide the destination and source keystore passwords.


## Attach the GitHub Java KeyStore certificate to your instance

Enable the JWT Bearer Grant token authentication by attaching the valid GitHub Java KeyStore \(JKS\) certificate to your ServiceNow instance.

### Before you begin

Ensure the availability of a valid Java KeyStore certificate.

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Certificates**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the record. For example, `My GitHub App Certificate`.|
    |Notify on expiration|Option to specify the users to be notified when the certificate expires.|
    |Warn in days to expire|Number of days to send a notification before the certificate expires.|
    |Active|Option to enable the certificate.|
    |Type|Option to select the type of the certificate. Select **Java Key Store**.|
    |Expires in days|Number of days until the certificate expires.|
    |Key store password|Password associated with the certificate \(hint: the destination KeyStore password previously created\).|
    |Short description|Summary about the certificate.|

4.  Select the attachments icon \(![Attachments icon](../image/dev-ops-attachments-icon.png)\) and attach a JKS certificate.

5.  Select **Validate Stores/Certificates**.


## Create a JWT signing key for the GitHub JKS certificate

Create a JSON Web Token \(JWT\) signing key to assign to your GitHub Java KeyStore certificate.

### Before you begin

Role required: admin, sn\_devops.admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the JWT signing key. For example, `My GitHub App JWT Key`.|
    |Signing Keystore|Valid JKS certificate attached in the previous task. For example, `My GitHub App Certificate`.|
    |Key Id|Unique Id to identify which key is used when multiple keys are used to sign tokens.|
    |Signing Algorithm|Algorithm to sign with the JWT key \(hint: RSA 256\).|
    |Signing Key Password|Password associated with the signing key \(hint: the source keystore password previously created\).|
    |Active|Option to enable the key.|

4.  Select **Submit**.


## Create a JWT provider for your GitHub signing key

Add a JSON Web Token \(JWT\) provider to your ServiceNow instance for GitHub.

### Before you begin

Role required: admin, sn\_devops.admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Providers**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the JWT provider. For example, `My GitHub App JWT Provider`.|
    |Expiry Interval \(sec\)|Number in seconds to set the lifespan of JWT provider tokens \(Hint: You can leave it as default\).|
    |Signing Configuration|Valid JWT signing key previously created. For example, `My GitHub App JWT Key`.|

4.  Right-click the form header, and select **Save**.

5.  Enter your GitHub App **App ID** \(available in the **About** section of your GitHub App configuration in GitHub \) as the value of the **iss** claim, in the Standard Claims related list.

6.  Leave **aud** and **sub** values blank \(default\).


## Register GitHub as an OAuth Provider \(JWT\)

Use the information generated during GitHub App account configuration to register GitHub as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin, sn\_devops.admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

    The **What kind of OAuth application?** message is displayed.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill in the fields.

<table id="table_fd2_2xr_4mb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to uniquely identify the record. For example, enter `My GitHub App Provider`.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of your GitHub App \(hint: available in the **About** section of your GitHub App configuration in GitHub \).

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of your GitHub App \(hint: available in the **About** section of your GitHub App configuration in GitHub \).

</td></tr><tr><td>

OAuth API script

</td><td>

Option that enables you to reference an amended OAuthUtil script include. Select **OAuthDevOpsGitHubJWTHandler**.

</td></tr><tr><td>

Default Grant type

</td><td>

Type of grant associated with application registry. Select **JWT Bearer**.

</td></tr><tr><td>

Token URL

</td><td>

The location of the token endpoint that the instance uses to retrieve and refresh tokens. For cloud version, enter: `https://api.github.com/app/installations/<installation_id>/access_tokens`.

For enterprise version, enter: `https://<HOST_URL>/api/v3/app/installations/<installation_id>/access_tokens`.

For the installation id, go to Install App section in your GitHub App configuration in GitHub and select the gear icon to configure your app. The installation id will be in the webpage URL. For example, https://github.com/settings/installations/&lt;installation\_id&gt;.

</td></tr></tbody>
</table>5.  Leave the rest of the form fields as default.

    ![Application Registry form](../image/github-oauth-jwt-app-registries.png)

6.  Right-click the form header, and select **Save**.

7.  Open the default profile created in the **OAuth Entity Profiles** related list.

8.  Populate the **JWT Provider** field with the JWT provider previously created and save the form.

9.  Navigate to **Key Management &gt; Module Access Policies &gt; All**.

10. Select the policy that has **com\_snc\_platform\_security\_oauth\_glideencrypter** as the **Crypto module** field value and **Script Include: OAuthDevOpsGitHubJWTHandler** as the **Target script** field value.

11. Ensure the **Result** field is set to **Track** and save the changes.

    ![Form that shows the result field is set to track.](../image/github-oauth-provider.png)


## Create a credential record for GitHub App provider \(JWT\)

Create a credential record to the GitHub App provider previously created to authorize actions.

### Before you begin

Role required: admin, sn\_devops.admin

### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The **What type of Credentials would you like to create?** message is displayed.

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, enter `My GitHub App Credential`.|
    |Active|Option to enable the record.|
    |OAuth Entity Profile|Default OAuth Entity profile created in the Application Registry.|

5.  Save the record.

6.  Select the **Get OAuth Token** related link to generate the OAuth token.


**Related topics**  


[GitHub Actions configurations](github-actions-integration-with-devops.md#)

[ServiceNow DevOps custom actions from GitHub marketplace](servicenow-devops-custom-actions-from-github-marketplace.md#)

[GitHub Deployment Gates for ServiceNow DevOps Change](github-deployment-gate-for-servicenow-devops-change.md)

