---
title: Test IdP connections
description: Testing the connection to an IdP validates the settings before enabling external authentication.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Multi-Provider SSO configurations, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Test IdP connections

Testing the connection to an IdP validates the settings before enabling external authentication.

## Before you begin

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## About this task

The Jakarta release supports the test connection within a pop-up window. If your IdP does not work correctly with this option, you can turn off this default setting.

Refresh MultiSSO IDP Metadata job fetches and updates the certificate for the IdP while create, update, or testing the connection.

**Note:** For some idp cases, If test connection is failed, they need to create glide.authenticate.multisso.test.connection.mandatory with the value as false and you can activate the idp without the test connection.

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  Select a defined IdP or click **New** to define a new IdP.

3.  Configure an identity provider if setting up a new IdP.

4.  Click **Test Connection**, enter login credentials for the IdP to check login.

    You cannot activate the IdP until you have a successful test connection. If the test fails, you can update to save your configuration information, but you cannot activate this configuration.

5.  Verify results using the **SSO Test Results/Summary** or the **Testing SSO Logs** section to see log messages.

    If there are any errors, refer to the [Multi-SSO \(SAML 2.0\) errors and fixes](../../saml/reference/saml-errors.md)

6.  Click **Cancel** when testing is complete.

    ![Sample test connection](../image/Test_connection.png)


