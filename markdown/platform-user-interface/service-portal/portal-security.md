---
title: Managing portal access
description: Control user access to a portal.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Managing portal access

Control user access to a portal.

Control who accesses your portal and what they can see in the following ways:

-   Authentication: Configure login and single sign on for users
-   Limit page access by role: Use roles to limit the users who can see a page.
-   Public pages: Use the public check box on a page record to make the page publicly accessible.

    **Note:** A number of portal pages that are installed by default are marked public. Filter your list of Service Portal pages for Public \[is\] true to identify these pages. Setting the Public value to false will prevent these pages from being publicly available.

-   User criteria: For a more advanced way of limiting user access, create and apply user criteria to pages, widgets, widgets instances, and search sources.
-   Multifactor authentication: If an instance is configured to require multifactor authentication, users are automatically directed to set up multifactor authentication upon initial login. For setup instructions, see [Setup multi-factor authentication upon initial login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/t_SetUpMultiFactorAuthUponLogin.md). If multifactor authentication is optional, users can still enable or disable authentication from their user profile. For setup instructions, see [Setup multi-factor authentication on your user profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/authentication/mfa-setup-profile.md).

-   **[Single sign-on, logins, and URL redirects](c_SPSSOLoginAndRedirects.md#)**  
Service Portal uses a combination of system properties and script includes to determine how the system handles URL redirects for users logging in to the portal.
-   **[Configure page security by role](../task/configure-page-security.md)**  
Set up pages to be public or filter them by role.
-   **[Configure widget security](../task/configure-widget-security.md)**  
Configure widget security to ensure that your widget is being accessed only by the intended audience.
-   **[User criteria for Service Portal](user-criteria.md)**  
User criteria enables you to allow access to users based on role, department, group, location, or company. Administrators can control access to pages, widgets, widget instances, announcements, and search sources in a portal by creating and applying user criteria.
-   **[Enable e-signature for Service Portal](../task/enable-esignature-sp.md#)**  
You can configure e-signature in Service Portal to require re-authentication from approving users.
-   **[Enable external user self-registration for Service Portal](../task/enable-self-registration.md)**  
Enable external users to register to a ServiceNow app through Service Portal.
-   **[Register your PIV/CAC card for Service Portal login](../task/piv-cac-login.md)**  
Register your Personal Identity Verification \(PIV\) or Common Access Card \(CAC\) card so that you can log in to your organization's portal without entering a password.
-   **[Deactivate a portal](../task/deactivate-portal.md)**  
Turn off access to a portal that you no longer want users to visit and optionally redirect them to another portal.

**Parent Topic:**[Configuring Service Portal](configuring-service-portal.md)

