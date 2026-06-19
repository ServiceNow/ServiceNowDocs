---
title: Identity Center for users
description: View the details about your active sessions, login history, and trusted devices with the Identity Center.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/identity/identity-center-for-user.html
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Identity Center, Identity]
---

# Identity Center for users

View the details about your active sessions, login history, and trusted devices with the Identity Center.

Identity Center is a collection of user attributes, devices, login history, security activity and much more. It provides a single pane view of all the data with additional security controls and notification capabilities.

With the Identity Center you can view the details about your active sessions, login history, and trusted devices.

**Note:** Roles required to access Identity Center features are as follows:

-   `user_login_history_viewer`: View login history details in the Identity Center, including login timestamps, browser information,IP address, and login status. Supports security investigations by enabling filtered views of login actions and helps identify suspicious activity.
-   `role_viewer`: View the records in the **sys\_icenter\_role\_config** table.

To access the Identity Center for users, navigate to one of the following:

-   On ServiceNow AI Platform, navigate to **All** &gt; **Self-Service** &gt; **My Profile** and select **View Identity Center** under the Related Links section.

    **Note:** You can also access your profile by selecting your user name in the instance header.

    \[Omitted image "user-banner.jpg"\] Alt text: Profile in the instance header

-   On Now Support, select the profile, select **View Identity Center** at the bottom of the page.

The Identity Center page is displayed as follows:

\[Omitted image "identity-center-for-user.png"\] Alt text: Identity Center for User Home page

Identity Center has the following tabs:

-   [Active Sessions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/identity/active-sessions.md)
-   [Login History](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/identity/login-history.md)
-   [Registered Mobile Devices](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/identity/registered-mobile-devices.md)

You can select these tabs to view the details such browser, IP Addressees, session relation information, login information, your registered mobile devices.

