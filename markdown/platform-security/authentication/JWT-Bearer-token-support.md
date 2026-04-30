---
title: Set up OAuth provider with JWT Bearer grant type
description: JSON Web Tokens \(JWTs\) enable the capability to configure server-to-server API interactions between ServiceNow and external API providers without requiring any user intervention. This support enables Integration Hub or other automated tasks using JWTs to configure API and Service integrations with different providers.You can attach a Java KeyStore \(JKS\) certificate to your instance to use to enable the JWT client authentication.Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore \(JKS\) certificate,Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [JWT Bearer, OAuth outbound, OAuth authentication, Authentication, Access Management]
---

# Set up OAuth provider with JWT Bearer grant type

JSON Web Tokens \(JWTs\) enable the capability to configure server-to-server API interactions between ServiceNow and external API providers without requiring any user intervention. This support enables Integration Hub or other automated tasks using JWTs to configure API and Service integrations with different providers.

## Before you begin

Role required: admin

## About this task

The following tasks show how ServiceNow can be set up to use JWTs for OAuth 2.0 client authentication and authorization grants. ServiceNow is the OAuth client, and you can configure an OAuth provider, such as Box or Docusign.

## Procedure

1.  [Upload Java Key Store certificate](JWT-Bearer-token-support.md#)

    Attach a JKS certificate to your instance to use to enable the JWT client authentication.

2.  [Configure a JWT signing key](JWT-Bearer-token-support.md#)

    Create a JWT signing key to assign to your Java KeyStore \(JKS\) certificate.

3.  [Create a JWT provider with a JWT signing key](JWT-Bearer-token-support.md#)

    Add a JWT provider to your ServiceNow instance.

4.  [Connect to a third-party OAuth provider](connect-3rd-party-oauth-provider.md)

    Create a third-party OAuth provider with a JWT Bearer as the default grant type in the ServiceNow Application Registry.

5.  [Specify an OAuth profile](https://www.servicenow.com/docs/access?context=t_SpecifyAnOAuthProfile&version=zurich&pubname=zurich-api-reference&ft:locale=en-US)

    Open the OAuth entity profile of the OAuth provider and assign a JWT provider.


## Upload Java Key Store certificate

You can attach a Java KeyStore \(JKS\) certificate to your instance to use to enable the JWT client authentication.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **x509 Certificate**.

2.  Fill in the form as needed.

<table id="choicetable_yqx_5f2_1gb"><tbody><tr><td id="d218346e198">

**Name**

</td><td>

A unique name for your certificate.

</td></tr><tr><td id="d218346e207">

**Notify on expiration**

</td><td>

Designate whom to notify when the certificate expires.

</td></tr><tr><td id="d218346e216">

**Warn in days to expire**

</td><td>

Send an email notification to your certificate manager before your certificate expires.

</td></tr><tr><td id="d218346e225">

**Active**

</td><td>

Enables the certificate to use for token requests.

</td></tr><tr><td id="d218346e234">

**Type**

</td><td>

The type of certificate you are uploading.

</td></tr><tr><td id="d218346e244">

**Expires in days**

</td><td>

The amount of days until the certificate expires.

</td></tr><tr><td id="d218346e253">

**Key store password**

</td><td>

The password associated with the certificate.

</td></tr><tr><td id="d218346e262">

**Short description**

</td><td>

 

</td></tr></tbody>
</table>3.  Click **Submit**.


## Configure a JWT signing key

Create a JSON Web Token \(JWT\) signing key to assign to your Java KeyStore \(JKS\) certificate,

### Before you begin

Role required: admin

**Note:** If you want to add **X.509 Certificate SHA-1 Thumbprint int \(x5t\)** to the header as part of the JWT Key, you must configure the form and add the **X.509 Certificate SHA-1 Thumbprint int \(x5t\)** field.

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Keys**.

2.  Fill in the form as needed.

<table id="choicetable_yqx_5f2_1gb"><tbody><tr><td id="d218346e351">

**Name**

</td><td>

A unique name for your JWT Key signing configuration.

</td></tr><tr><td id="d218346e360">

**Signing Keystore**

</td><td>

The keystore designated when signing the JWT.

</td></tr><tr><td id="d218346e369">

**Key ID**

</td><td>

The Key ID \(kid\) helps identify which key is used when multiple keys are used to sign tokens.**Note:** If you configure this field, the Key ID claim is included in the JWT. If you do not configure this field, your JWT will not have a Key ID claim.

</td></tr><tr><td id="d218346e381">

**Signing Algorithm**

</td><td>

The algorithm to use to sign with the JWT key. RSA 256 is the only algorithm available.

</td></tr><tr><td id="d218346e390">

**Signing Key Password**

</td><td>

The password associated with the signing key.

</td></tr><tr><td id="d218346e400">

**Active**

</td><td>

Designate that the JWT key alias is actively referenced from a JWT provider.

</td></tr></tbody>
</table>3.  Click **Submit**.


## Create a JWT provider with a JWT signing key

Add a JSON Web Token \(JWT\) provider to your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **JWT Provider**.

2.  Fill in the form and click **Submit**.

<table id="choicetable_yqx_5f2_1gb"><tbody><tr><td id="d218346e489">

**Name**

</td><td>

A unique name for your JWT provider configuration.

</td></tr><tr><td id="d218346e498">

**Expiry Interval \(sec\)**

</td><td>

The lifespan of the tokens, in seconds, generated by the JWT provider.

</td></tr><tr><td id="d218346e507">

**Signing Configuration**

</td><td>

The ServiceNow JWT signing key configuration to apply.

</td></tr></tbody>
</table>
