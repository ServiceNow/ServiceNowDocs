---
title: Configure Microsoft SharePoint Online connection record
description: Integrate your ServiceNow instance with the Microsoft SharePoint Online by setting up the Microsoft SharePoint Online and a connection record.Generate a digital certificate file in the .cer format to upload it to Microsoft Azure.Generate a digital certificate file in the .cer format to upload it to Microsoft Azure.Create a custom app using your Azure portal to authenticate requests.Enable the JWT Bearer Grant token authentication by attaching a valid Java Key Store \(JKS\) certificate.Create a JSON Web Token \(JWT\) signing key to assign to your Java Key Store certificate.Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.Use the information generated during Microsoft SharePoint Online account configuration to register Microsoft SharePoint Online as an OAuth provider and allow the instance to request OAuth 2.0 tokens.Create Credential records to the Microsoft SharePoint Online custom OAuth application you created during Microsoft SharePoint Online account configuration. The Microsoft SharePoint Online spoke connection and credential aliases use these credentials to authorize actions.Create Connection records to your Microsoft SharePoint Online account. The Microsoft SharePoint Online spoke connection and credential alias uses these connections to perform actions on Microsoft SharePoint Online.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 9
breadcrumb: [Microsoft SharePoint Online Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Configure Microsoft SharePoint Online connection record

Integrate your ServiceNow instance with the Microsoft SharePoint Online by setting up the Microsoft SharePoint Online and a connection record.

## Before you begin

-   Request Integration Hub subscription
-   Activate [Microsoft SharePoint Online Spoke](../concept/sharepoint-online-spoke.md)
-   Create an OAuth application on Microsoft Azure portal.
-   Access to Microsoft Azure portal
-   Role required: admin

## Generate certificate for Windows

Generate a digital certificate file in the .cer format to upload it to Microsoft Azure.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to [https://learn.microsoft.com/en-us/sharepoint/dev/solution-guidance/security-apponly-azuread\#setting-up-an-azure-ad-app-for-app-only-access](https://learn.microsoft.com/en-us/sharepoint/dev/solution-guidance/security-apponly-azuread#setting-up-an-azure-ad-app-for-app-only-access).

2.  Execute the PowerShell script.

    The script generates two files with .PFX and .CER extensions.

    **Note:** Store or remember the password that is used to encrypt private key to generate the .PFX file and .CER files.

3.  Use the .PFX file to create a Java Key Store \(JKS\) file.

    **Note:** Store or remember the password that is used to generate the .JKS file from the .PFX file.


## Generate self-signed certificate for Mac

Generate a digital certificate file in the .cer format to upload it to Microsoft Azure.

### Before you begin

Role required: admin

### Procedure

1.  Open the terminal on your Mac machine.

2.  Replace the placeholder `<filename>` with a file name of your choice and execute this script `keytool -genkey -keyalg RSA -alias selfsigned -keystore <filename>.jks -storepass <enter password for keystore> -validity 720 -keysize 2048`.

    **Note:** The password to the keystore must contain at least six characters.

    The keystore asks you to enter certain information.

3.  Enter your custom information, as given in the image for illustration.![Keystore custom information.](../image/MS-sharepoint-spoke-sponline-certificate-mac.png)

4.  Press **Return**.

    You are advised to migrate to PKCS12 format.

5.  Replace the placeholder `<filename>` with a file name of your choice and execute this script `keytool -importkeystore -srckeystore <filename>.jks -destkeystore <filename>.jks -deststoretype pkcs12`.

6.  Enter the source keystore password.

    The migration to PKCS12 is successful.

7.  Replace the placeholder `<filename>` with a file name of your choice and execute this script `keytool -exportcert -keyalg RSA -alias selfsigned -keystore <filename>.jks -storepass <password to the keystore> -rfc -file <filename>.cer`.

    The script generates the .cer file.

8.  To locate the .cer file, navigate to the location on your local disk.

    ![Location of the .cer file.](../image/MS-sharepoint-spoke-sponline-cer-file-generated.png)


## Configure an application in Microsoft Azure

Create a custom app using your Azure portal to authenticate requests.

### Before you begin

-   Access to Microsoft Azure portal
-   Role required: admin

### Procedure

1.  Upload the certificate to Microsoft Azure portal.

    1.  Log in to [https://portal.azure.com/](https://portal.azure.com/).

    2.  Select **App registrations**.

        ![App registration button.](../image/MS-sharepoint-spoke-app-reg-button.png)

    3.  Select **All applications** or **Owned applications.**

        ![OAuth application selection options.](../image/ms-sharepoint-spoke-graph-select-app.png)

    4.  In the search field, enter the name of the OAuth application you had created.

        To learn how to configure an OAuth application, see [Configure OAuth application in Microsoft Azure](configure-oauth-application-in-microsoft-azure.md).

    5.  On the left panel, under Manage heading, select Certificates &amp; secrets.

        ![Certificates & secrets.](../image/MS-sharepoint-sponline-upload-certificate.png)

    6.  Under Certificates &amp; secrets, select Certificates.

        ![Certificate section.](../image/MS-sharepoint-sponline-certificate-section.png)

    7.  Select **Upload certificate**.

    8.  In the Upload certificate window, select the folder icon \(![Folder icon.](../image/MS-sharepoint-spoke-sponline-upload-certificate-icon.png)\) to navigate to the .cer file you had generated.

    9.  In the Description field, enter a description of the certificate.

    10. Select **Add**.

        The certificate is uploaded.

    11. Under the **Thumbprint** column, copy the thumbprint value and store it at a secure place.

        ![Thumbprint value.](../image/MS-sharepoint-spoke-sponline-copy-thumbprint.png)

        **Note:** Ensure that you copy the entire value of **Thumbprint**.

        Alternatively, you can copy the **Thumbprint** by clicking **Manifest**.

        ![Copy value of Manifest.](../image/ms-exchng-ol-manifest.png)

    12. Encode the Thumbprint value to a Base64 value and record the value for later use.

    **Note:** You can use a Hexadecimal to Base64 \(Hex to Base64\) converter tool to encode the **Thumbprint** value to a Base64 value.

2.  Obtain permissions to access the REST APIs that the spoke needs to automate actions.

    1.  On the left panel, under the Manage heading, select API permissions.

        ![API permissions link.](../image/MS-sharepoint-spoke-graph-api-permissions-link.png)

    2.  Under the Configured permissions heading, select **+ Add a permission**.

    3.  In the Request API permissions window, select **SharePoint**.

        ![SharePoint API button.](../image/MS-sharepoint-spoke-sponline-sharepoint-api.png)

    4.  Select **Application permissions**.

        ![Application permissions button.](../image/MS-sharepoint-spoke-sponline-application-permission.png)

    5.  Expand the Sites list.

    6.  Select Sites.FullControl.All.

        Your ServiceNow instance now has full control of all sites in Microsoft SharePoint Online.

    7.  Select **Add permissions**.

        The permissions are added.

        ![SharePoint online permissions granted.](../image/MS-sharepoint-spoke-sponline-permissions-granted.png)

    8.  To grant admin consent, select **Grant admin consent for ServiceNow**.

    9.  In the Grant admin consent confirmation window, select **Yes**.

        The admin consent is granted.

        ![Admin consent granted status.](../image/MS-sharepoint-sponline-admin-consent.png)

        **Tip:** If you want to use other permissions apart from `Sites.FullControl.All`, contact your SharePoint and Azure administrators to determine the exact permissions that are needed for your organisational policies.


## Attach a Java Key Store certificate

Enable the JWT Bearer Grant token authentication by attaching a valid Java Key Store \(JKS\) certificate.

### Before you begin

-   Valid Java Key Store certificate
-   Role required: admin

### Procedure

1.  Navigate to **System Definition** &gt; **Certificates**.

2.  Open the record **Microsoft SharePoint Online Certificate**.

    **Note:** Ensure that you use the default record **Microsoft SharePoint Online Certificate** only.

3.  Enter the password associated with the JKS file in **Key store password**.

4.  Select **Java Key Store** as the **Type**.

5.  Click the attachments icon \(![Attachments icon](../image/attachments-icon.png)\) and attach the JKS certificate you had generated.

    For more information, see [Configure OAuth application in Microsoft Azure](configure-oauth-application-in-microsoft-azure.md).

6.  Click **Validate Stores/Certificates**.

7.  Click **Update**.


## Configure the JWT signing key

Create a JSON Web Token \(JWT\) signing key to assign to your Java Key Store certificate.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **System OAuth** &gt; **JWT Keys**.

2.  Open the record **Microsoft SharePoint Online JWT Keys**.

3.  Enter the password that is used to encrypt private key to generate the .PFX file and .CER file in **Signing Key Password**.

4.  Click **Update**.


## Configure the JWT provider

Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.

### Before you begin

-   Copy and record the value of **Application \(client\) ID** and **Directory \(tenant\) ID** of the application you had registered in the Azure portal.

    ![Copy the values of Client ID and Tenant ID.](../image/ms-sharept-clientid.png)

-   Role required: admin

### Procedure

1.  Navigate to **System OAuth** &gt; **JWT Providers**.

2.  Open the record **Microsoft SharePoint Online JWT Provider**.

3.  Enter values for **iss**, **sub**, and **aud** in the Standard Claims related list.

    |Field|Value|
    |-----|-----|
    |aud|Microsoft Online URL in this format: `https://login.microsoftonline.com/<tenant-id>/oauth2/token`. Replace `<tenant-id>` with **Directory \(tenant\) ID** value of your application had registered in the Azure portal.|
    |iss|**Application \(client\) ID** of the application you had registered in Azure portal.|
    |sub|**Application \(client\) ID** of the application you had registered in Azure portal.|

4.  Click **Update**.


## Register Microsoft SharePoint Online as OAuth provider

Use the information generated during Microsoft SharePoint Online account configuration to register Microsoft SharePoint Online as an OAuth provider and allow the instance to request OAuth 2.0 tokens.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message **What kind of OAuth application?**

3.  Select **Connect to a third party OAuth Provider**.

    The system displays a blank Application Registries form.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Name to uniquely identify the record. For example, enter `SharePoint OAuth profile`.|
    |Client ID|Client ID in this format: `<ClientID>`.|
    |Client Secret|Client Secret you created during the Microsoft SharePoint Online account configuration.|
    |OAuth API Script|Select **OAuthUtilSPJWTOnline**.|
    |Default Grant type|Select **Client Credentials**.|
    |Token URL|Token URL in this format: `https://login.microsoftonline.com/<tenant-id>/oauth2/token`. Replace `<tenant-id>` with **Directory \(tenant\) ID** value of your application had registered in the Azure portal.|

5.  In the OAuth Entity Scopes related list, insert a record with these values.

    |Name|OAuth scope|
    |----|-----------|
    |scope|`https://<MS-SharePoint-tenant-name>.sharepoint.com/.default`|

    ![Insert the OAuth entity scope record.](../image/ms-sharept-scopes.png)

6.  Right-click the form header, and click **Save**.

    The system validates the OAuth credentials and creates the OAuth Entity Profiles related list.


### Result

The instance can request OAuth 2.0 tokens for the spoke.

## Create credential records for the Microsoft SharePoint Online spoke

Create Credential records to the Microsoft SharePoint Online custom OAuth application you created during Microsoft SharePoint Online account configuration. The Microsoft SharePoint Online spoke connection and credential aliases use these credentials to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message **What type of Credentials would you like to create?**.

3.  Select **OAuth 2.0 Credentials**.

    The pop-up window displays a blank OAuth 2.0 Credentials form.

4.  Enter these values.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the record. For example, enter `SharePoint Credentials`.|
    |Active|Enable|
    |OAuth Entity Profile|Select the OAuth profile you created when you registered the custom Microsoft SharePoint Online application as an OAuth provider. For example, select **SharePoint OAuth profile**.|
    |Applies to|Select the MID Servers that can use this credential. For example, select **All MID Servers**.|
    |Order|Select the order to apply this credential. For example, enter `100`.|

5.  Save the record.


## Create connection records for the Microsoft SharePoint Online spoke

Create Connection records to your Microsoft SharePoint Online account. The Microsoft SharePoint Online spoke connection and credential alias uses these connections to perform actions on Microsoft SharePoint Online.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the connection and credential alias record for MicrosoftSharePointOnline.

3.  From the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  On the form, fill in the fields.

    |Field|Value required|
    |-----|--------------|
    |Name|Enter any name to uniquely identify the connection record. For example, enter `SharePoint Connection`.|
    |Credential|Select the Credential record you created for Microsoft SharePoint Online. For example, select **SharePoint Credentials**.|
    |Connection alias|Select the Connection alias record you created for Microsoft SharePoint Online.|
    |Active|Enable|
    |Connection URL|Enter the root SharePoint URL. For example, `https://<SiteName>.sharepoint.com`.|

5.  In the **Attributes** tab, enter the Base64 encoded value of **Thumbprint**.

    **Note:** The **Thumbprint** value is a hexadecimal value. You can use a Hexadecimal to Base64 \(Hex to Base64\) converter tool to encode the **Thumbprint** value to a Base64 value.

6.  Click **Submit**.

    The Microsoft SharePoint Online account is integrated with your ServiceNow instance and the spoke is ready to be used.

    **Note:** If the single sign-on is setup, configure your flows to retrieve the user details from Microsoft SharePoint Online using the spoke action, Look Up User Information By Login Name, to verify if the user is authorised to perform the required actions.


### What to do next

1.  Navigate to **Connections &amp; Credentials** &gt; **Credentials**.
2.  Open the credential record you had created. For example, **SharePoint Credentials**.
3.  From Related Links, click **Get OAuth Token**.

    The system displays a confirmation message that the OAuth token flow is completed successfully. Review the details if the flow is not completed successfully.

    **Note:** Ensure that you allow pop-up windows in your browser.

    -   Confirm that you allow pop-up windows in your browser.
    -   Confirm that the thumbprint has been defined in the connection record.
    The spoke setup is completed and you can use the flows as per your requirement.

    **Note:** If the generated token doesn't work after the spoke setup, open your OAuth application in the Azure portal and select the two checkboxes under **Implicit grant and hybrid flows**.![Select the tokens in the Azure portal.](../image/ms-exchng-ol-tokens.png)


