---
title: Configure Workload Identity Federation for Google Cloud
description: Set up an outbound OAuth connection to Google Cloud that uses the OAuth 2.0 token exchange grant with a KMF-signed subject token instead of a stored client secret.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/configure-wif-gcp.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-24"
reading_time_minutes: 3
keywords: [Workload Identity Federation, Google Cloud, GCP, Workload Identity Pool, token exchange]
breadcrumb: [Workload Identity Federation, OAuth Outbound, OAuth authentication, Authentication, Access Management]
---

# Configure Workload Identity Federation for Google Cloud

Set up an outbound OAuth connection to Google Cloud that uses the OAuth 2.0 token exchange grant with a KMF-signed subject token instead of a stored client secret.

## Before you begin

Role required: `oauth_admin` \(plus `sn_kmf.*` roles to reference the KMF module\).

Complete the setup in your Google Cloud project first — you need values from there to create this connection. In Google Cloud IAM, create a Workload Identity Pool and an OIDC provider within that pool. Then note the following:

-   Project Number — found in the Google Cloud console under your project &gt; Dashboard.
-   Identity Pool Name — the Workload Identity Pool you created in Google Cloud IAM.
-   Identity Provider Name — the OIDC provider configured within your Workload Identity Pool.

Scopes are specific to each target resource you want to access — for example, `https://www.googleapis.com/auth/cloud-platform`.

## About this task

This task uses the Workload Identity Federation fast-configuration UI. The UI creates the underlying OAuth entity and profile records for you, including an OAuth entity profile configured for the Token Exchange grant type. Related records appear on the OAuth Entity, OAuth Entity Profile, OAuth Entity Scopes, JWT Provider, and JWT Key tabs after you submit.

## Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Workload Identity Connections**

2.  Select **New**.

3.  On the **Which cloud provider are you connecting to?** page, under **Google Cloud Platform \(GCP\)**, select **Connect to GCP using Workload Identity Federation**.

4.  Fill in the form.

    |Field|Description|
    |-----|-----------|
    |**Connection Name**|A unique name for this Workload Identity connection. Required.|
    |**Project Number**|The numeric Google Cloud project number. Found in the Google Cloud console under your project &gt; Dashboard. Required.|
    |**Identity Provider Name**|The OIDC provider configured within your Workload Identity Pool. Required.|
    |**Identity Pool Name**|The Workload Identity Pool you created in Google Cloud IAM. Required.|

5.  Select **Submit**.

    Business rules automatically create the underlying OAuth entity and OAuth entity profile. The profile is configured for the Token Exchange grant type and sends a token-exchange request to Google's STS endpoint, carrying the KMF-signed JWT as the `subject_token`. The created records appear on the OAuth Entity and related tabs.

    \[Omitted image "wif-gcp.png"\] Alt text: WIF - GCP configuration


## Result

The instance can now obtain federated access tokens from Google Cloud STS and use them for calls to Google APIs, scoped to the resources you specify.

## What to do next

Verify the connection by making a test call from an outbound REST message that uses the newly created OAuth entity.

The connection uses the following related records, shown on the tabs in the form. The fast-configuration creates the OAuth records for you; use the tabs to review them and to complete the scopes and the KMF-backed JWT key. These records hold the same configuration as a standard OAuth setup — see the OAuth outbound documentation for full field details.

|Tab|Description|What to do|
|---|-----------|----------|
|**OAuth Entity**|The OAuth application registry entity created for this Google Cloud connection. Holds the client configuration used for the token exchange with Google's STS endpoint.|Created automatically on submit. No action is required. Edit only to adjust advanced OAuth settings.|
|**OAuth Entity Profile**|The profile that defines how the instance requests tokens from Google Cloud. Configured for the Token Exchange grant type, presenting the KMF-signed JWT as the `subject_token`.|Created automatically on submit. No action is required.|
|**OAuth Entity Scopes**|The OAuth scopes the instance requests from Google Cloud. Scopes are specific to each target resource you want to access.|Add the scopes for the Google resource you intend to call — for example, `https://www.googleapis.com/auth/cloud-platform`.|
|**JWT Provider**|The JWT provider that mints the signed JWT used as the subject token in the token exchange. References the JWT signing key on the JWT Key tab.|Confirm the JWT provider references the KMF-backed JWT signing key.|
|**JWT Key**|The JWT signing key \(`jwt_keystore_aliases`\) used to sign the subject token.|Verify the signing key has **Key Source** set to **KMF Cryptographic Module**. See [Configure a JWT signing key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/JWT-Bearer-token-support.md).|

