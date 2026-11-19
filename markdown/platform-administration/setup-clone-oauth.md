---
title: Set up OAuth authentication for a clone target
description: Complete a one-time OAuth setup to register a target instance for cloning. This process generates a Client ID on the target instance and authorizes the connection from the source instance.Configure the target instance user for basic authentication when the target instance does not support OAuth authentication.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-administration/setup-clone-oauth.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Register instance for cloning, Configure, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# Set up OAuth authentication for a clone target

Complete a one-time OAuth setup to register a target instance for cloning. This process generates a Client ID on the target instance and authorizes the connection from the source instance.

## Before you begin

Both the source and target instances must be on Australia Patch 5 or later to use OAuth target authentication.

Roles required:

|Instance|Initial OAuth setup|Subsequent clone operations|
|--------|-------------------|---------------------------|
|Source|clone\_admin, oauth\_admin|clone\_admin, oauth\_user|
|Target|clone\_admin, oauth\_admin|Not required|

**Note:** The oauth\_admin role is required on both instances only to complete the one-time OAuth provider creation. Users who submit clone operations after setup is complete need the oauth\_user role on the source instance instead.

## Procedure

1.  Navigate to **All** &gt; **Clone Admin Console** &gt; **Clone Home**.

2.  Navigate to **Configuration** &gt; **Clone instances**.

3.  Select **New**.

4.  In the **Target Instance** field, enter the target instance URL and select **Continue**.

    The system runs a version compatibility check.

    If the target instance doesn't support OAuth, the system falls back to basic authentication. See [Configure basic authentication fallback for clone targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/setup-clone-oauth.md) for configuration steps.

5.  Select **Setup OAuth on Target**.

    The target instance opens in a new browser tab.

6.  On the OAuth setup page, select **Set up OAuth**.

    The page generates a Client ID.

    If the Client ID is not generated, the OAuth provider creation may have failed. This occurs when the user performing the setup does not have the oauth\_admin role on the target instance. Without this role, the system can't create the OAuth provider record and returns an authorization error.

    To resolve this, verify that the user has the oauth\_admin role on the target instance, then reload the OAuth setup page and select **Set up OAuth** again.

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

-   To submit a clone request to the new target, see [Request a clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/t_StartAClone.md).
-   To reset or re-authorize OAuth for this target, see [Reset OAuth for a clone target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/reauthorize-clone-target.md).

## Configure basic authentication fallback for clone targets

Configure the target instance user for basic authentication when the target instance does not support OAuth authentication.

### Before you begin

Role required: clone\_admin

### About this task

Basic authentication requires specific role and identity configuration on the target instance user record.

### Procedure

1.  On the target instance, verify that the user has the clone\_admin role and the soap role.

2.  On the user record, set **identity\_type** to **machine**.

    **Warning:** The **identity\_type** field may not appear on the User form by default. If it isn't visible, add it temporarily using Form Layout. Users with **identity\_type** set to **machine** can no longer log in to the instance UI. This configuration supports Basic Auth for automated and integration traffic only.


### Result

The target instance is configured for basic authentication. Clone operations can proceed using Basic Auth for automated and integration traffic.

**Related topics**  


[Troubleshooting for registering target instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-administration/register-target-instance-troubleshooting.md)

