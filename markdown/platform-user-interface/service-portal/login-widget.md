---
title: Login widget
description: The login widget controls user access to your site. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Example widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Login widget

The login widget controls user access to your site. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

## Using the widget

Users log in to a portal by entering their credentials in the login widget.

The widget uses credentials from the User \[sys\_user\] record. In the **User name** field, the user enters the **User ID** from their user record. In the **Password** field, the user enters the password from their user record.

![Default login widget on the Service Portal landing page](../image/WidgetLogin.png "Login widget")

The login widget by default includes a **Forgot Password?** link that enables users to reset their password using the Password Reset application. For more information about Password Reset configuration, see [Password Reset](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/password-reset/password-reset-landing-page.md).

**Note:** When the user selects **Forgot Password?**, the system redirects the user to the page value specified in the **glide.security.password\_reset.uri** system property.

If you don't want to include the **Forgot Password?** link, set the **glide.security.forgot\_password.display.link** system property to false.

## External user self-registration

External user self-registration enables a large group of users to register to a ServiceNow app without the help of an administrator. Users register to the app via a link at the bottom of the login widget screen that says ""Don't have an account? Register".

![Self-registration link.](../image/self-registration-widget.png)

For more information on external user self-registration, see [Enable external users to self-register to your ServiceNow instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/external-user-self-registration.md).

## PIV/CAC authentication

With certificate-based authentication activated in your instance, users can register their Personal Identity Verification \(PIV\) or Common Access Card \(CAC\) card for Service Portal login.

After self-registering their PIV/CAC card, a user can log in by inserting their card into a card reader and then selecting **Login with PIV/CAC card** on the login widget.

![Login page with PIV/CAC option](../image/piv-cac-login.png)

Before a user can register their PIV/CAC card, an administrator must activate certificate-based authentication and then set up PIV/CAC authentication. For more information on this setup process, see [Personal Identity Verification \(PIV\) card or Common Access Card \(CAC\) based authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/certificate-based-authentication/certificate-based-authentication.md).

For more information on how a user self-registers their PIV/CAC card, see [Register your PIV/CAC card for Service Portal login](../task/piv-cac-login.md).

## Instance options

Use the instance options to configure the login widget for a portal page.

|Field|Description|
|-----|-----------|
|Show panel|Show or hide the panel that appears behind the login widget. The panel helps the widget stand out from the page background rather than blending in.|
|Use Advanced View|Changes the widget layout. Adds the **Forgot Password?** link to the left of the **Login** button and adds field names for **User name** and **Password** instead of hint text.|

**Parent Topic:**[Example widgets](sp-example-widgets.md)

**Related topics**  


[Create and edit a page using the Service Portal Designer](../task/t_ConfigureAPage.md#)

[Configure widget instances](c_ConfigureWidgetInstances.md)

[Clone a widget](../task/t_CloneAndEditAWidget.md)

