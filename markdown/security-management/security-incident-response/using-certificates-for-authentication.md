---
title: Using Certificates for authentication
description: Request an access token with a certificate credential.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Establish MS Teams Graph connection on ServiceNow AI Platform, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Using Certificates for authentication

Request an access token with a certificate credential.

## Before you begin

1.  You can either use a self-signed certificate or CA issued certificate. You can create a self-signed certificate by executing the PowerShell script as outlined in[Setting up an Azure AD app for app-only access](https://docs.microsoft.com/en-us/sharepoint/dev/solution-guidance/security-apponly-azuread#setting-up-an-azure-ad-app-for-app-only-access). The script generates two files: .PFX file and .CER file.

    **Note:** Ensure that you are aware of the password that is used to encrypt private key to generate the .PFX file and .CER file.

2.  Use the .PFX file to create a Java Key Store \(JKS\) file.

    **Note:** Ensure that you are aware of the password that is used to generate JKS file from the .PFX file.


Role required: admin

## Procedure

1.  Navigate to **App registrations** in Azure AD portal.

2.  Click **Certificates &amp; secrets** from the **Manage** section.

3.  In the **Certificates** tab, click **Upload Certificate**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Upload a certificate \(public key\) with one of the following file types: .cer, .pem, .crt|.CER file you had generated using the PowerShell script.|
    |Description|Description of the certificate.|

5.  Click **Add**.

    The certificate is uploaded and its details are displayed under the **Certificates** tab.

6.  Copy the **Thumbprint** value of the uploaded certificate.

    The **Thumbprint** value is a hexadecimal value.

    ![Thumbprint of the uploaded certificate.](../../../administer/integrationhub-store-spokes/image/ms-sharept-thumbprint.png)

7.  Encode the **Thumbprint** value to a Base64 value and record the value for later use.

    **Note:** You can use a Hexadecimal to Base64 \(Hex to Base64\) converter tool to encode the **Thumbprint** value to a Base64 value.


-   **[Attach a Java Key Store certificate for MS Teams](attach-a-java-key-store-certificate-for-ms-teams.md)**  
Enable the JWT Bearer Grant token authentication by attaching a valid Java Key Store \(JKS\) certificate.
-   **[Configure the JWT signing key for MS Teams](configure-the-jwt-signing-key-for-ms-teams.md)**  
Create a JSON Web Token \(JWT\) signing key to assign to your Java Key Store certificate.
-   **[Configure the JWT provider for MS Teams](configure-the-jwt-provider-for-ms-teams.md)**  
Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.
-   **[Establish a connection using certificates](establish-a-connection-using-certificates.md)**  
Establish a connection between newly created Microsoft Teams graph application using certificates.

**Parent Topic:**[Establish MS Teams Graph connection on ServiceNow AI Platform](../../security-incident-response/task/msim-micorsoft-team-requirements.md)

