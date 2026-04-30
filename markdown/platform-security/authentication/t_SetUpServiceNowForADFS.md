---
title: Set up the instance for ADFS
description: Configure your instance and SAML 2.0 settings to work with ADFS.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ADFS integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Set up the instance for ADFS

Configure your instance and SAML 2.0 settings to work with ADFS.

## Before you begin

Perform these steps only after you have set up ADFS for SAML. For details on that process, see [set up ADFS for SAML](../concept/c_ADFSIntegrationWithSAML2.0.md).

Role required: admin

## Procedure

1.  If not already active, [Activate Multi-Provider SSO plugin](../../single-sign-on/task/t_ActivateMultipleProviderSSO.md).

2.  Configure [SAML](../concept/c_SAML2.0WebBrowserSSOProfile.md), but when you install the IdP certificate, attach the PEM certificate you created when you [Set up ADFS for SAML](t_DefineADFSServiceURL.md).

3.  Click **Save**.

4.  Verify that the **Issue** and **Subject** fields have values and that there are no errors.

    If an error occurs, open the saved PEM formatted certificate in Notepad and copy and paste the certificate into the PEM Certificate field.

5.  Verify that the SAML2SingleSignon\_update1 installation exit is active.

6.  Continue the SAML 2.0 configuration.

    **Note:** When a certificate is updated on the ADFS server, you also need to upload an updated certificate to the instance.


