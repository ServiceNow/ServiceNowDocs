---
title: Configure Workload Identity Federation for Microsoft Azure
description: Set up an outbound OAuth connection to Microsoft Azure that uses a KMF-signed JWT assertion instead of a stored client secret.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-wif-azure.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 3
keywords: [Workload Identity Federation, Microsoft Azure, Microsoft Entra, federated credential, subject identifier]
breadcrumb: [Workload Identity Federation, OAuth Outbound, OAuth authentication, Authentication, Access Management]
---

# Configure Workload Identity Federation for Microsoft Azure

Set up an outbound OAuth connection to Microsoft Azure that uses a KMF-signed JWT assertion instead of a stored client secret.

## Before you begin

Role required: oauth\_admin \(plus sn\_kmf.\* roles to reference the KMF module\).

Complete the setup in your Azure portal first — the connection requires values from the app registration to create this connection. In Azure, create an app registration and add a federated credential to it, with:

-   Issuer set to `https://<your-instance>.service-now.com`.
-   A Subject value that matches the Subject Identifier you enter in this form.
-   Audience set to `api://AzureADTokenExchange`.

From the app registration Overview page, note the Directory \(Tenant\) ID and the Application \(Client\) ID.

## About this task

This task uses the Workload Identity Federation fast-configuration UI. The UI creates the underlying OAuth entity and profile records for you, so manual configuration is not required. Related records appear on the OAuth Entity, OAuth Entity Profile, OAuth Entity Scopes, JWT Provider, and JWT Key tabs after you submit.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Workload Identity Connections**

2.  Select **New**.

3.  On the **Which cloud provider are you connecting to?** page, under **Microsoft Azure**, select **Connect to Azure using Workload Identity Federation**.

4.  Fill in the form.

    |Field|Description|
    |-----|-----------|
    |**Connection Name**|A unique name for this Workload Identity connection. Required.|
    |**Application \(Client\) ID**|The Application \(Client\) ID of your Azure app registration. Required.|
    |**Directory \(Tenant\) ID**|The Directory \(Tenant\) ID of your Azure app registration. Required.|
    |**Subject to send in the token**|The subject identifier sent in the JWT. This value must exactly match the Subject in your Azure federated credential. A mismatch causes silent authentication failure. Required.|
    |**Azure URL Override**|Optional. An override for the Azure token endpoint URL. Leave empty to use the default Azure endpoint.|

5.  Select **Submit**.

    Business rules automatically create the underlying OAuth entity and OAuth entity profile. The entity sends a `client_credentials` request to Azure, carrying the KMF-signed JWT as a `client_assertion` with `aud = api://AzureADTokenExchange`. The created records appear on the OAuth Entity and related tabs.

    \[Omitted image "wif-azure.png"\] Alt text: WIF-Azure configuration


## Result

The instance can now obtain access tokens from Azure using Workload Identity Federation. Outbound consumers that reference the created OAuth entity use it automatically.

## What to do next

Verify the connection by making a test call from an outbound REST message that uses the newly created OAuth entity.

The connection uses the following related records, shown on the tabs in the form. The fast-configuration creates the OAuth records for you; use the tabs to review them and to complete the scopes and the KMF-backed JWT key. These records hold the same configuration as a standard OAuth setup — see the OAuth outbound documentation for full field details.

|Tab|Description|What to do|
|---|-----------|----------|
|**OAuth Entity**|The OAuth application registry entity created for this Azure connection. Holds the client configuration used for the `client_credentials` request to Azure.|Created automatically on submit. No action is required. Edit only to adjust advanced OAuth settings.|
|**OAuth Entity Profile**|The profile that defines how the instance requests tokens from Azure. Configured to present the KMF-signed JWT as a `client_assertion` with `aud = api://AzureADTokenExchange`.|Created automatically on submit. No action is required.|
|**OAuth Entity Scopes**|The OAuth scopes the instance requests from Azure for the target resource.|Add the scopes required for the Azure resource you intend to call.|
|**JWT Provider**|The JWT provider that mints the signed JWT presented to Azure. References the JWT signing key on the JWT Key tab.|Confirm the JWT provider references the KMF-backed JWT signing key.|
|**JWT Key**|The JWT signing key \(`jwt_keystore_aliases`\) used to sign the client assertion.|Verify the signing key has **Key Source** set to **KMF Cryptographic Module**. See [Configure a JWT signing key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/JWT-Bearer-token-support.md).|

