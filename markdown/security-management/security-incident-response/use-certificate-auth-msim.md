---
title: Use certificates for authentication
description: Request an access token with a certificate credential.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/security-incident-response/use-certificate-auth-msim.html
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [certificate, authentication, azure-ad, thumbprint]
breadcrumb: [Integrate Major Security Incident Management with Microsoft SharePoint, Integrate, Major Security Incident Management, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Use certificates for authentication

Request an access token with a certificate credential.

## Before you begin

1.  A self-signed or CA-issued certificate is required, created using the PowerShell script outlined in [Setting up an Azure AD app for app-only access](https://docs.microsoft.com/en-us/sharepoint/dev/solution-guidance/security-apponly-azuread#setting-up-an-azure-ad-app-for-app-only-access). The script generates two files: a .PFX file and a .CER file.

    **Note:** Confirm that you're aware of the password used to encrypt the private key to generate the .PFX and .CER files.

2.  A Java Key Store \(JKS\) file created from the .PFX file is required.

    **Note:** Confirm that you're aware of the password used to generate the JKS file from the .PFX file.


Role required: admin

## Procedure

1.  Navigate to **App registrations** in Azure AD portal.

2.  Select **Certificates &amp; secrets** from the **Manage** section.

3.  In the **Certificates** tab, click **Upload Certificate**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Upload a certificate \(public key\) with one of the following file types: .cer, .pem, .crt|.CER file you had generated using the PowerShell script.|
    |Description|Description of the certificate.|

5.  Select **Add**.

    The certificate is uploaded and its details are displayed under the **Certificates** tab.

6.  Copy the **Thumbprint** value of the uploaded certificate.

    **Note:** The **Thumbprint** value is a hexadecimal value.

7.  Encode the **Thumbprint** value to a Base64 value and record the value for later use.

    **Note:** You can use a Hexadecimal to Base64 \(Hex to Base64\) converter tool to encode the **Thumbprint** value to a Base64 value.


## What to do next

**Note:** The same certificate can be uploaded to a single shared App Registration and used across all three environments.

**Parent Topic:**[Integrate Major Security Incident Management with Microsoft SharePoint](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/security-incident-response/integrate-msim-sharepoint.md)

