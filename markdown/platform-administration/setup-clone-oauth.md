---
title: Set up OAuth authentication for a clone target
description: Complete a one-time OAuth setup to register a target instance for cloning. This process generates a Client ID on the target instance and authorizes the connection from the source instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/setup-clone-oauth.html
release: australia
topic_type: task
last_updated: "2026-06-10"
reading_time_minutes: 1
breadcrumb: [Register instance, Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up OAuth authentication for a clone target

Complete a one-time OAuth setup to register a target instance for cloning. This process generates a Client ID on the target instance and authorizes the connection from the source instance.

## Before you begin

The target instance must run an OAuth-capable version of the Clone Admin Console.

Roles required:

-   Source instance: clone\_admin
-   Target instance: clone-admin and oauth\_admin

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Navigate to **Configurations** &gt; **Clone instances**.

3.  Select **New**.

4.  In the **Instance URL** field, enter the target instance URL and select **Next**.

    The system runs a version compatibility check.

    If the target instance doesn't support OAuth authentication, the system falls back to basic authentication. See [Troubleshooting for registering target instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/register-target-instance-troubleshooting.md).

5.  Select **Setup OAuth on Target**.

    The target instance opens in a new browser tab.

6.  On the OAuth setup page, select **Set up OAuth**.

    The page generates a Client ID.

    If the Client ID is not generated, verify that you have the oauth\_admin role on the target instance and that the page loaded completely before selecting **Set up OAuth**.

7.  Copy the **Client ID**.

8.  Return to the source instance browser tab.

9.  In the **Client ID** field on the Add Clone Target form, paste the Client ID.

10. Select **Add Target**.

    The browser redirects to the target instance to complete authorization.

11. Select **Allow** to grant consent.

    If your session has expired, log in to the target instance before granting consent.

    The browser redirects to the source instance.

    If the browser doesn't redirect to the source instance, return to the Clone Admin Console and select **Reset OAuth or Retry** to restart the authorization.


## Result

The target instance is registered and authorized for clone requests.

## What to do next

To submit a clone request to the new target, see [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md).

