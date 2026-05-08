---
title: Configure mobile apps to use specific identity providers
description: You can configure a login experience that is specific to a mobile app and different from the web login experience. For example, Now Mobile app users can be automatically redirected to an identity provider \(IdP\) that is different from the IdP that is defined for the web session.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Mobile authentication, Configuring the Mobile Platform, Mobile Platform]
---

# Configure mobile apps to use specific identity providers

You can configure a login experience that is specific to a mobile app and different from the web login experience. For example, Now® Mobile app users can be automatically redirected to an identity provider \(IdP\) that is different from the IdP that is defined for the web session.

## Before you begin

Role required: admin

## About this task

Admins can define the login experience for mobile users by associating app-specific login pages for mobile apps. For example, admins can enforce the following authentication scenarios:

-   When an instance is enabled with single sign-on \(SSO\), admins can configure mobile users to be redirected to a specific IdP login screen on their mobile app. This login screen can be different from the automatically redirected IdP that is defined for the instance.
-   Configure the mobile app to display the ServiceNow® SSO login page where users can provide their credentials to initiate the SSO login flow.
-   Configure the mobile app to display a custom login page with buttons that redirect users to different IdPs based on their role or persona.

## Procedure

1.  Navigate to **All** &gt; **Application Registry**.

2.  Select an application of **OAuth Client** type to open it.

    For example, select **ServiceNow Agent**, which is an OAuth Client.

3.  In the **Login URL** field of the Application Registries page, enter the login URL you want to use for this mobile app.

    ![Application Registries screen showing the Login URL field.](../image/mob-auth-redirect-idp-provider.png)

    For example, enter:

    -   `oauth_login.do`

        This login URL causes the local login screen to appear.

    -   `login_with_sso.do?glide_sso_id=<*valid active IdP sys\_id*>`

        This login URL redirects the user to an external IdP that is specified with the IdP sys\_id in the **glide\_sso\_id** parameter.

    -   `login_locate_sso.do`

        This login URL displays the ServiceNow SSO login screen where users can enter their email or user ID.

        ![ServiceNow SSO login page on a mobile app screen.](../image/mob-auth-servicenow-sso-login.png)

    You can also enter the login URL for a custom login page.

    **Important:**

    If you enter **login\_with\_sso.do** for the Login URL, you must also provide a valid IdP sys\_id as a **glide\_sso\_id** parameter to the URL. For example:

    `login_with_sso.do?glide_sso_id=bc47c42887101010d00b5773e8cb0b85`

    To get the valid IdP sys\_id:

    1.  In your instance, navigate to **All** &gt; **Identity Providers**
    2.  In the Identity Providers page, select the IdP provider.
    3.  On the IdP provider page, right-click the page banner, and select **Copy sys\_id**.

        ![Right-click menu showing the option to copy the IdP's sys_id.](../image/mob-auth-redirect-copy-idp-sysid.png)

    If a valid IdP sys\_id isn’t provided, the OAuth client login URL value can't be saved.

    For information about configuring an external IdP on your instance, see Create an external identity provider.

4.  Select **Update** to save the entry.


## Result

Open the mobile app on a mobile device and select the instance. You should be redirected to the login page that was set up on the instance in the Application Registry.

**Note:** If **login\_locate\_sso.do** was saved as the Login URL and no default IdP is configured or the **sso\_source** for the user isn’t set, then an error displays when the user name is entered. This behavior is similar to web UI behavior.

**Parent Topic:**[Mobile authentication](../concept/mobile-authentication.md)

