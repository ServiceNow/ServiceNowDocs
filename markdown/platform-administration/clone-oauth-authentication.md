---
title: OAuth 2.0 authentication for clone targets
description: OAuth 2.0 authenticates clone requests to target instances without requiring a local admin account, enabling you to use your existing login credentials.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/clone-oauth-authentication.html
release: australia
topic_type: concept
last_updated: "2026-06-10"
reading_time_minutes: 2
breadcrumb: [Explore, Instance Clone, Configure core features, Administer the ServiceNow AI Platform]
---

# OAuth 2.0 authentication for clone targets

OAuth 2.0 authenticates clone requests to target instances without requiring a local admin account, enabling you to use your existing login credentials.

## Why OAuth 2.0 replaces basic authentication

Previously, Instance Clone used basic authentication to confirm access to a target instance. This required maintaining a local admin account specifically for cloning and entering those credentials for each clone request.

The OAuth 2.0 Authorization Code Flow enhances security and convenience by providing the following benefits:

-   No local admin account required - use your existing login credentials, including SSO.
-   One-time target instance registration.
-   Automatic token generation and expiration for each clone request.

## How it works

The source instance acts as the OAuth client, and the target instance acts as the OAuth authorization server. Authentication happens once per target instance during setup and repeats only if the session expires or is revoked.

During setup, the target instance generates a Client ID that uniquely identifies the source instance as an authorized OAuth client. Administrators copy this Client ID and return it to the source instance to complete registration.

After setup is complete, Instance Clone uses a short-lived JSON Web Token \(JWT\) access token to authenticate each clone request to the target. The source instance obtains this token automatically before each clone operation.

The clone\_admin role is required on the source instance to request clones. The oauth\_admin role is required on the target instance during initial setup only.

## Token lifecycle

The JWT access token has a short time-to-live \(TTL\) and expires automatically after each use. If a token expires, the system automatically redirects the user to reauthorize on the target instance from the Clone Admin Console before a clone can be requested.

## Basic Auth fallback

Basic Auth is available only as a fallback when the OAuth flow fails. Because of recent platform-wide authentication changes, using Basic Auth to authenticate the clone target requires that the target-instance user have:

-   the clone\_admin role
-   the soap role
-   identity\_type set to machine on the user record

**Warning:** Users with **identity\_type** = machine can no longer log in to the instance UI. This configuration supports Basic Auth for automated and integration traffic only. The **identity\_type** field may not appear on the User form by default. If it isn't visible, add it temporarily using Form Layout.

## One-time setup per target instance

OAuth setup is required once per target instance. No re-registration is required for routine clone requests. If a token expires, the system prompts you to select **Authorize** on the target instance before you can place a clone request.

For more information, see [Set up OAuth authentication for a clone target](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/setup-clone-oauth.md).

