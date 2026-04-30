---
title: Create a SAML logout endpoint
description: Create a SAML logout endpoint to allow single logout.
locale: en-US
release: zurich
product: Authentication
classification: authentication
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [ADFS integration with SAML 2.0, Integrating SAML 2.0 with other features, SAML, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Create a SAML logout endpoint

Create a SAML logout endpoint to allow single logout.

## Before you begin

Role required: admin

## About this task

See [this article on ADFS signout](https://social.technet.microsoft.com/Forums/windowsserver/en-US/b562c9a5-6d05-4a19-bd39-cb1bf9f77c4a/adfs-and-google-apps-sso-signout-url?forum=winserverDS) for more information.

## Procedure

1.  Go to **ADFS manager** &gt; **Trust Relationships** &gt; **Relying Party Trusts** &gt; **properties**.

2.  Under the Endpoints tab, click **Add SAML**.

3.  Configure the settings:

    -   **Endpoint Type**: SAML Logout
    -   **Binding**: POST
    -   **Trusted URL**: The URL of your ADFS server. For example,

        ```
        https://myadfsserver.domain.net/adfs/ls/?wa=wsignout1.0
        ```

    -   **Response URL**: The application logout URL. For example,

        ```
        https://{instancename}.service-now.com/external_logout_complete.do
        ```


