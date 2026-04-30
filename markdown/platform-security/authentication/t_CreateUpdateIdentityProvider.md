---
title: Create an external identity provider
description: After you have configured the multi-provider SSO properties, you can update or create new SAML 2.0 or digest token identity provider.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Multi-Provider SSO configurations, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Create an external identity provider

After you have configured the multi-provider SSO properties, you can update or create new SAML 2.0 or digest token identity provider.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  To edit an identity provider record, click the record.

    -   For digest token configurations, manually update the properties.
    -   For SAML2 Update 1 configurations, automatically update the identity provider metadata with the **Import Identity Provider Metadata** related link or update the properties manually.
    -   For OpenID Connect configurations, manually update the properties.
3.  To create a new identity provider, click **New**.

    -   For digest token configurations: Click **Digest SSO** and enter the digest properties for multi-provider single sign-on.
    -   For SAML2 configurations: Click **MultiSSOV2\_SAML2\_custom** and import the identity provider metadata from a URL, as XML, or manually enter the identity provider information.

        ![Importing identity provider metadata](../image/Import_metadata.png)

    -   For OpenID Connect: Click **OpenID Connect** and enter client ID, client secret, and well known configuration URL.
4.  To make the IdP the failover IdP that is used when the default IdP is not available, select the **Default** check box.

    If you have SAML 2 Update 1 active and you upgrade to the Fuji release, the SAML 2 Update 1 IdP is selected as the default failover. No default failover IdP is selected for new instances or if you are upgrading from a release on which SAML 2 Update 1 is not active.

    **Note:** The metadata import process automatically creates a certificate record for the identity provider. Navigate to the **x509 Certificate** module to see the certificate.

    **Note:** Certificates for single-sign on should always be in PEM format to work with SAML certificates.

5.  If E-Signature is active, configure the Identity Provider form and add the **Assertion Consumer URL for eSignature authentication** field.

    In most cases, this URL is: `https://YOURINSTANCE.service-now.com/consumer.do`. However, if you employ a customized method of handling the SAML authentication for E-Signature, you can set up your own consumer URL. If you are only using SAML 2.0 Update 1 and not using Multi-Provider Single Sign-on, configure the assertion consumer URL with [E-signature SAML properties](../../saml/concept/c_AddingSupportForESignature.md).


