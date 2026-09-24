---
title: Set up OAuth provider with JWT Bearer grant type
description: JSON Web Tokens \(JWTs\) enable the capability to configure server-to-server API interactions between ServiceNow and external API providers without requiring any user intervention. This support enables Integration Hub or other automated tasks using JWTs to configure API and Service integrations with different providers.You can attach a Java KeyStore \(JKS\) certificate to your instance to use to enable the JWT client authentication.Create a JSON Web Token \(JWT\) signing key. The key can be a certificate uploaded to the instance, or a private key managed by the Key Management Framework \(KMF\).Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/JWT-Bearer-token-support.html
release: brazil
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 4
breadcrumb: [JWT Bearer, OAuth Outbound, OAuth authentication, Authentication, Access Management]
---

# Set up OAuth provider with JWT Bearer grant type

JSON Web Tokens \(JWTs\) enable the capability to configure server-to-server API interactions between ServiceNow and external API providers without requiring any user intervention. This support enables Integration Hub or other automated tasks using JWTs to configure API and Service integrations with different providers.

## Before you begin

Role required: oauth\_admin

## About this task

Configure your ServiceNow instance to use JWTs for OAuth 2.0 client authentication and authorization grants. Your ServiceNow instance acts as the OAuth client, and you configure an OAuth provider such as Box or Docusign.

## Procedure

1.  [Upload Java Key Store certificate](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/JWT-Bearer-token-support.md)

    Attach a JKS certificate to your instance to use to enable the JWT client authentication.

2.  [Configure a JWT signing key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/JWT-Bearer-token-support.md)

    Create a JWT signing key to assign to your JKS certificate.

    **Note:** Starting in the Brazil release, ES256 \(ECDSA with SHA-256\) is available as a signing algorithm option. Select **ES256** in the **Signing Algorithm** field when your third-party OAuth provider requires an ECDSA-signed JWT. The default is RS256.

3.  [Create a JWT provider with a JWT signing key](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/JWT-Bearer-token-support.md)

    Add a JWT provider to your ServiceNow instance.

4.  [Connect to a third-party OAuth provider](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/authentication/connect-3rd-party-oauth-provider.md)

    Create a third-party OAuth provider with a JWT Bearer as the default grant type in the ServiceNow Application Registry.

5.  [Specify an OAuth profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/api-reference/web-services/t_SpecifyAnOAuthProfile.md)

    Open the OAuth entity profile of the OAuth provider and assign a JWT provider.


## Upload Java Key Store certificate

You can attach a Java KeyStore \(JKS\) certificate to your instance to use to enable the JWT client authentication.

### Before you begin

Role required: oauth\_admin

### Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **x509 Certificate**.

2.  Fill in the form as needed.

<table id="choicetable_yqx_5f2_1gb"><tbody><tr><td id="d264425e213">

**Name**

</td><td>

A unique name for your certificate.

</td></tr><tr><td id="d264425e222">

**Notify on expiration**

</td><td>

Designate whom to notify when the certificate expires.

</td></tr><tr><td id="d264425e231">

**Warn in days to expire**

</td><td>

Send an email notification to your certificate manager before your certificate expires.

</td></tr><tr><td id="d264425e240">

**Active**

</td><td>

Enables the certificate to use for token requests.

</td></tr><tr><td id="d264425e249">

**Type**

</td><td>

The type of certificate you are uploading.

</td></tr><tr><td id="d264425e259">

**Expires in days**

</td><td>

The amount of days until the certificate expires.

</td></tr><tr><td id="d264425e268">

**Key store password**

</td><td>

The password associated with the certificate.

</td></tr><tr><td id="d264425e277">

**Short description**

</td><td>

 

</td></tr></tbody>
</table>3.  Click **Submit**.


## Configure a JWT signing key

Create a JSON Web Token \(JWT\) signing key. The key can be a certificate uploaded to the instance, or a private key managed by the Key Management Framework \(KMF\).

### Before you begin

Role required: `oauth_admin`

When Key Source is KMF Cryptographic Module, you also need the `sn_kmf.*` roles required to reference the KMF crypto module.

### About this task

**Note:** You must have a single entry in the keystore. The system reads the keystore and selects the first alias, so make sure the associated keystore's first entry is the certificate you intend to use.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Fill in the form as needed.

<table id="table_q41_y42_fkc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Name**

</td><td>

A unique name for the JWT Key signing configuration. Required.

</td></tr><tr><td>

**Key Source**

</td><td>

Choice to select the key either directly from a keystore or from the Key Management Framework. Required. Choices: -   **Signing Keystore** — Use a certificate uploaded to the instance. The Signing Keystore field is required. Signing Algorithm is read-only when this option is selected.
-   **KMF Cryptographic Module** — Use a private key managed by the Key Management Framework \(KMF\). The KMF Crypto Module field is required. The Signing Algorithm is set automatically from the module's asymmetric crypto specification. Fields that only apply to Signing Keystore \(Signing Keystore, Key Id\) are hidden.


</td></tr><tr><td>

**Signing Keystore**

</td><td>

Reference to the keystore to use when signing the JWT. Required when Key Source is Signing Keystore.

</td></tr><tr><td>

**Key Id**

</td><td>

The key identifier to send in the `kid` claim.If you configure this field, the Key Id claim is included in the JWT. If you don't configure this field, the JWT does not include a Key Id claim.

</td></tr><tr><td>

**X.509 Certificate SHA-1 Thumbprint \(x5t\)**

</td><td>

Include the `x5t` claim \(X.509 certificate base64url-encoded SHA-1 thumbprint\) in the JWT header. To use this field, configure the form to add it.

</td></tr><tr><td>

**Signing Algorithm**

</td><td>

The signing algorithm to use. Read-only when Key Source is KMF Cryptographic Module — the algorithm is derived from the selected KMF Crypto Module. Choices: -   **RSA 256** \(default\) — RSA signature with SHA-256.
-   **ES256** — ECDSA signature using the P-256 curve with SHA-256.


</td></tr><tr><td>

**Signing Key**

</td><td>

The shared secret or password associated with the signing key. Applies to Signing Keystore.

</td></tr><tr><td>

**KMF Crypto Module**

</td><td>

Reference to a KMF cryptographic module that manages the signing for this alias. Required when Key Source is KMF Cryptographic Module. When you select a module, the instance reads the module's asymmetric crypto specification and sets the Signing Algorithm accordingly. If the selected module has no asymmetric crypto specification, an error appears at the top of the form and the record can't be saved.

</td></tr><tr><td>

**Application**

</td><td>

The application scope for the JWT Key record. Defaults to **Global**.

</td></tr><tr><td>

**Active**

</td><td>

Whether the JWT Keystore Alias is active and referenced from a JWT provider.

</td></tr></tbody>
</table>3.  Select **Submit**.


## Create a JWT provider with a JWT signing key

Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.

### Before you begin

Role required: oauth\_admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Provider**.

2.  Fill in the form and click **Submit**.

<table id="choicetable_yqx_5f2_1gb"><tbody><tr><td id="d264425e628">

**Name**

</td><td>

A unique name for your JWT provider configuration.

</td></tr><tr><td id="d264425e637">

**Expiry Interval \(sec\)**

</td><td>

The lifespan of the tokens, in seconds, generated by the JWT provider.

</td></tr><tr><td id="d264425e646">

**Signing Configuration**

</td><td>

The ServiceNow JWT signing key configuration to apply.

</td></tr></tbody>
</table>
