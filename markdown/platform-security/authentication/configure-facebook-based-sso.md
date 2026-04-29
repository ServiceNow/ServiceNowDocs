---
title: Configure a Facebook-based Single Sign-On \(SSO\)
description: Configure a Facebook-based SSO to your ServiceNow instance.
locale: en-US
release: australia
product: Authentication
classification: authentication
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [OIDC as a SSO identity provider, Multi-Provider single sign-on \(SSO\), Authentication, Access Management]
---

# Configure a Facebook-based Single Sign-On \(SSO\)

Configure a Facebook-based SSO to your ServiceNow instance.

## Before you begin

Have a valid Client ID that is configured as an IdP from Facebook.

Enable the following properties:

-   Enable multiple provider SSO.
-   Enable debug logging for the multiple provider SSO integrations.

Role required: sso\_config\_admin, business\_rule\_admin, script\_include\_admin

## Procedure

1.  Navigate to **All** &gt; **Multi-Provider SSO** &gt; **Identity Providers**.

2.  To create a new Facebook identity provider, click **New**.

3.  Click **OpenID Connect**.

4.  On the form, fill in the fields.

    |Fields|Description|
    |------|-----------|
    |Name|Unique name for the OIDC identity provider configuration.|
    |Client ID|The client ID of the application registered in the third-party OIDC identity provider.|
    |Client Secret|The client secret of the application registered in the third-party OIDC identity provider.|
    |Well known Configuration URL|The URL that contains metadata about the third-party OIDC identity provider.|

5.  Click **Import**.

    The Facebook-based IdP is created.

6.  Select the Facebook IdP.

7.  In the Facebook idP, do the following:

    1.  Validate all the fields such as **Name**, **OIDC Entity Profile**, **External logout redirect**, and **ServiceNow Homepage**.

    2.  Provide your **SSO label**.

8.  In the **User Provisioning** tab, specify the fields that you need to configure users to specific user provisioning and roles.

    Only the mandatory fields are required. You can specify the remaining fields depending on what you need.

9.  In the **OIDC Entity** tab, do the following:

    1.  Click the entity.

    2.  Set the **Redirect URL** field to your Facebook redirect URL.

10. In the **OAuth Entity Profiles** tab, do the following:

    1.  In the profile details, click a profile.

    2.  Select a scope and verify the details.

        For example, select **scope-1**

11. In the **OAuth Entity Scopes** tab, click the **scope-1** link and add the scope as `email`.

12. To save the configuration, right-click the header and click **Save**.

13. To set the configuration as active, select **Active**.


## Result

Users are displayed with the Facebook SSO option on the login form.

