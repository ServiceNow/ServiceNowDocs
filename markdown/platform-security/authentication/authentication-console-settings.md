---
title: Authentication Console settings
description: Settings on the Settings tab of the Authentication Console control whether the policy-based login experience is active and how the identifier-first login page behaves.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/authentication/authentication-console-settings.html
release: brazil
product: Authentication
classification: authentication
topic_type: reference
last_updated: "2026-09-24"
reading_time_minutes: 2
keywords: [Authentication Console settings, identifier-first login settings, policy-based login, recent identifiers, SSO source-based IdP routing, debug logs]
breadcrumb: [Authentication Console, Authentication, Access Management]
---

# Authentication Console settings

Settings on the **Settings** tab of the Authentication Console control whether the policy-based login experience is active and how the identifier-first login page behaves.

## Accessing the settings

To view or change these settings, open the Authentication Console and select the **Settings** tab. You need the `user_authn_admin` role.

**Note:** Some settings are SSO-related and require the Multi-Provider SSO plugin. When the plugin isn't installed, those settings are unavailable and a message on the Settings tab prompts you to install the plugin.

## Policy-based login experience

|Setting|Description|Default|
|-------|-----------|-------|
|**Enable policy-based login** \(Recommended\)|Enables the policy-based login experience on this instance to determine the first authentication factor during user login.|Off|

## Identifier-first login settings

<table><thead><tr><th>

Setting

</th><th>

Description

</th><th>

Default

</th></tr></thead><tbody><tr><td>

**Enable identifier-first login**

</td><td>

When enabled, users see an identifier-first login flow that determines the authentication method based on configured policies.

</td><td>

On

</td></tr><tr><td>

**Additional login options**

</td><td>

When enabled, displays identity provider \(IdP\) tiles on the identifier-first login page. Instead of entering an identifier first, users can log in directly with a configured IdP.

</td><td>

Off

</td></tr><tr><td>

**Recent identifiers**

</td><td>

When enabled, displays previously used identifiers as clickable tiles on the identifier-first login page, so returning users can initiate login without re-entering their username or email.

</td><td>

On

</td></tr><tr><td>

**Number of recent identifiers to display**

</td><td>

Specifies how many recently used identifiers appear as tiles on the identifier-first login page. Helps returning users sign in faster, especially on shared devices.

</td><td>

3

</td></tr><tr><td>

**SSO source-based IdP routing**

</td><td>

When enabled, the identifier-first login functionality routes users to the IdP specified in the `sso_source` field. It checks the user record first; if no value is set, it falls back to the user's company record. Requires the Multi-Provider SSO plugin.

</td><td>

Off

</td></tr><tr><td>

**IdP routing evaluation order**

</td><td>

Determines whether SSO source-based IdP routing \(`sso_source`\) runs before or after identifier-first login policy evaluation. Requires the Multi-Provider SSO plugin. Choices: -   **Before policy evaluation** — Prioritizes explicit IdP assignments.
-   **After policy evaluation** — Uses `sso_source` only as a fallback when no identifier-first login policy matches.

</td><td>

Before policy evaluation

</td></tr><tr><td>

**Pre-fill identifier on the IdP login page**

</td><td>

When enabled, the identifier entered on the login page is forwarded to the identity provider, so the IdP login page is pre-populated and the user doesn't have to re-enter it.

</td><td>

On

</td></tr></tbody>
</table>## Additional login settings

This setting is SSO-related and requires the Multi-Provider SSO plugin.

|Setting|Description|Default|
|-------|-----------|-------|
|**Override cookie-based redirects**|When enabled, policies are evaluated on every login, overriding any stored IdP cookie \(`glide_sso_id`\) from a previous login on this browser.|Off|

## Debug settings

|Setting|Description|Default|
|-------|-----------|-------|
|**Debug logs**|When enabled, detailed logs for every login flow are captured, including policy evaluation, IdP routing decisions, and authentication outcomes.|Off|

