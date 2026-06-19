---
title: Mobile authentication
description: Users are required to log in to an instance on their mobile device. Depending on how you configure authentication for mobile devices, users may be required to enter additional information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/mobile/mobile-platform/mobile-authentication.html
release: zurich
product: Mobile Platform
classification: mobile-platform
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring the Mobile Platform, Mobile Platform]
---

# Mobile authentication

Users are required to log in to an instance on their mobile device. Depending on how you configure authentication for mobile devices, users may be required to enter additional information.

For more information on configuring authentication for mobile devices, see Set up OAuth.

**Important:** ServiceNow mobile apps support platform authentication using OAuth 2.0. Authentication mechanisms include multi provider SSO, MFA, LDAP, Local DB, and Digest. For more information, see [Mobile security](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/mobile-security-landing.md) and [Identity and access management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/sg-mobile-ID-access-mgmt.md).

Follow the instructions for using a third-party OAuth provider.

-   **[Create a QR code for mobile login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/create-qr-login.md)**  
Create and use a QR code containing JSON to provide a method for your users to log in with pre-defined parameters.
-   **[Configure mobile app token lifespan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/configure-mobile-app-timeout.md)**  
Configure the length of time it takes for the app to time out.
-   **[Force local login in mobile apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/mobile-force-local-login.md)**  
Configure the force local login option to provide local login experience on mobile apps even when the instance is configured with Single Sign On \(SSO\) configuration. You can configure this feature independently on any available ServiceNow® app.
-   **[Mobile access to IP-restricted networks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/mob-access-ip-restrictd-netwrks.md)**  
Enable ServiceNow mobile apps to access IP-restricted networks when adaptive authentication is activated on your instance.
-   **[Configure mobile apps to use specific identity providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/config-mobapps2-use-specific-idps.md)**  
You can configure a login experience that is specific to a mobile app and different from the web login experience. For example, Now® Mobile app users can be automatically redirected to an identity provider \(IdP\) that is different from the IdP that is defined for the web session.
-   **[Configure an external authentication browser for ServiceNow mobile apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/config-ext-auth-browser-ios.md)**  
Admins can configure an external browser for mobile apps. This external browser is used during authentication so external URLs that are opened by the same browser can maintain sessions and cookies.
-   **[Securing your ServiceNow mobile instance with Zero Trust Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/mobile/mobile-platform/zero-trust-access-for-mobile.md)**  
Limit end-user access to your ServiceNow® instance by opting in to Zero Trust Access. This adjusts user roles and permissions according to security policies defined by the admin based on factors such as IP address, location, and identity provider attributes.

