---
title: Test the SAML integration
description: Test the SAML integration after you complete all the other setup tasks.
locale: en-US
release: xanadu
product: Authentication
classification: authentication
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [SAML, Multi-Provider Single sign-on \(SSO\), Authentication, Access Management]
---

# Test the SAML integration

Test the SAML integration after you complete all the other setup tasks.

## Before you begin

Role required: admin

## Procedure

1.  Log in to the instance as a user with the admin role.

2.  Navigate to **SAML 2 Single Sign-on** &gt; **Properties**.

3.  In the property Enable external authentication, select **Yes**.

    **Note:**

    Enabling external authentication requires all users to use SAML 2.0 single sign-on. If anyone tries to access the application in an unauthenticated state, the instance automatically sends an authentication request to the \(IdP\) and redirects the user to the SAML IdP Authentication page.

4.  Click **Save**.

5.  Log out of the instance.

6.  Browse to the instance URL.

    If the integration is functioning properly, the IdP should ask for the user's credentials.


**Related topics**  


[Multi-SSO \(SAML 2.0\) errors and fixes](../reference/saml-errors.md)

