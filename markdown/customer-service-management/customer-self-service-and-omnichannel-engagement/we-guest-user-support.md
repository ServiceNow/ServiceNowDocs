---
title: Guest user access for Web Embeddables
description: Enable unauthenticated users to access Web Embeddables components on your third-party website without logging in.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/customer-self-service-and-omnichannel-engagement/we-guest-user-support.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Guest user access for Web Embeddables

Enable unauthenticated users to access Web Embeddables components on your third-party website without logging in.

## Overview of Web Embeddables for guest users

Provide unauthenticated users with access to Web Embeddables components on your website without requiring them to log in. Currently, the following components are available for guest users:

-   Knowledge article view component
-   Catalog item component

The components display content only if the content such as article or catalog items are explicitly made public. As an administrator, you can ensure the guest session is created by human \(not bots\) through CAPTCHA and on a trusted third-party website through JWT. Here is how you can set up web embed for guest user using following options:

-   Install the guest plugin
-   Enable the component ACLs
-   Set the system property
-   Implement the global code on your third-party website
-   Embed the component on your third-party website page. For more information, see [Embed ServiceNow components instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-web-components-third-party-website.md).
-   Make content displayed in components public

## Guest users support activation

Activate the Web components for Guest Embeddables \(sn\_guest\_component\) plugin to enable guest user support on your website. For more information on how to activate the plugin, see [Activate Web Embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/act-web-embeddables.md).

## Enable the component ACLs

For guest user to view or interact with the components on your third-party website, you must enable the guest ACLs of the components . For more information, see [Configure ACL for guest access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customer-self-service-and-omnichannel-engagement/we-config-acl-guest-user.md).

## Guest users system properties

Set the following system property to control how guest sessions are created and verified for Web Embeddables.

<table id="we_guest_user_sys_prop"><thead><tr><th>

Property

</th><th>

Description

</th><th>

Behavior

</th></tr></thead><tbody><tr><td>

**glide.embedded.session.trust.verification.enabled**

</td><td>

Enable verification to check that the guest embeddable session is created on a trusted third-party website. The verification happens through JWT token.

</td><td>

When set to true, the system checks for a JWT token before creating an embedded guest session. When set to false, the system creates a guest embedded session without verification. By default, the property is set to true.

Pass the JWT token using the value for the key: `guestTokenCallback` available in the global code.

</td></tr></tbody>
</table>## Global code implementation

For pages supporting both guest and authenticated sessions, the global code implementation is as follows:

-   On page load: Uncomment to call `await startGuestSession()` function. This establishes an anonymous session so guest components \(for example, a public-facing knowledge view component\) render without requiring the user to sign in.
-   After user logs in: Uncomment to call `await login()` function. This upgrades the session to an authenticated one, causing authenticated components to load for that user. Guest components are replaced or supplemented by the logged-in experience depending on your configuration.
-   On logout: Uncomment to call `await logout()` function to suspend down the authenticated session and return to the guest state if needed.

**Note:** `guestTokenCallback` function is required in `init()` function for guest sessions to work. This callback must return a valid guest JWT token for your instance. Without it, `startGuestSession()` function fails validation.

To display content in the guest components, make knowledge articles and catalog items public.

Guest users can access the Web Embeddables components designated as public on your website without logging in.

