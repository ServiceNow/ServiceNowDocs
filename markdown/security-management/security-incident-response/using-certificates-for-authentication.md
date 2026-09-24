---
title: Use certificate for authentication
description: Request an access token with a certificate credential.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/security-incident-response/using-certificates-for-authentication.html
release: brazil
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Establish Microsoft Teams Graph connection on ServiceNow AI Platform, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use certificate for authentication

Request an access token with a certificate credential.

## Before you begin

1.  A self-signed or CA-issued certificate is required, created using the PowerShell script. For more information, see: [Setting up an Azure AD app for app-only access](https://docs.microsoft.com/en-us/sharepoint/dev/solution-guidance/security-apponly-azuread#setting-up-an-azure-ad-app-for-app-only-access). The script generates two files: a .PFX file and a .CER file.

    **Note:** Confirm that you're aware of the password used to encrypt the private key to generate the .PFX and .CER files.

2.  A Java Key Store \(JKS\) file created from the .PFX file is required.

    **Note:** Confirm that you're aware of the password used to generate the JKS file from the .PFX file.


Role required: admin

## Procedure

1.  Navigate to **App registrations** in Azure AD portal.

2.  Select **Certificates &amp; secrets** from the **Manage** section.

3.  In the **Certificates** tab, select **Upload Certificate**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Upload a certificate \(public key\) with one of the following file types: .cer, .pem, .crt|.CER file you had generated using the PowerShell script.|
    |Description|Description of the certificate.|

5.  Select **Add**.

    The certificate is uploaded and its details are displayed under the **Certificates** tab.

6.  Copy the **Thumbprint** value of the uploaded certificate.

    The **Thumbprint** value is a hexadecimal value.

    \[Omitted image "ms-sharept-thumbprint.png"\] Alt text: Thumbprint of the uploaded certificate.

7.  Encode the **Thumbprint** value to a Base64 value and record the value for later use.

    **Note:** You can use a Hexadecimal to Base64 \(Hex to Base64\) converter tool to encode the **Thumbprint** value to a Base64 value.


-   **[Attach a Java Key Store certificate for MS Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/attach-a-java-key-store-certificate-for-ms-teams.md)**  
Enable the JWT Bearer Grant token authentication by attaching a valid Java Key Store \(JKS\) certificate.
-   **[Configure the JWT signing key for MS Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/configure-the-jwt-signing-key-for-ms-teams.md)**  
Create a JSON Web Token \(JWT\) signing key to assign to your Java Key Store certificate.
-   **[Configure the JWT provider for MS Teams](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/configure-the-jwt-provider-for-ms-teams.md)**  
Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.
-   **[Establish a connection using certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/establish-a-connection-using-certificates.md)**  
Establish a connection between newly created Microsoft Teams graph application using certificates.

**Parent Topic:**[Establish Microsoft Teams Graph connection on ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/security-incident-response/msim-micorsoft-team-requirements.md)

