---
title: Exploring Machine Identity Console
description: Manage your service accounts, which are used for integrations with ServiceNow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-security/identity/explore-machine-identity-console.html
release: australia
product: Identity
classification: identity
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Machine Identity Console, Identity]
---

# Exploring Machine Identity Console

Manage your service accounts, which are used for integrations with ServiceNow.

Machine Identity Console enables you to manage your non-human identities \(NHIs\) that are used to identify, authenticate, and authorize different software entities to access secured resources of ServiceNow. The entities that gain access include applications, workloads, APIs, bots, and automated systems. Unlike human identities, non-human identities \(NHIs\) aren’t governed in the same manner and aren’t directly associated with a human. Their identity and verification methods are distinct from the human users, and standard human security measures are not applicable to them.

**Note:** You need the `mi_admin` role to use the Machine Identity Console.

\[Omitted video\] Description: Overview of Machine Identity Console

Here's what is available on the Machine Identity Console Overview page:

-   Total Machine identity \(integration\) accounts and the Accounts with high privilege roles.
-   Unique API calls - Last 7 days
-   Authentication method used - Last 7 days
-   Machine Identity Security score and findings related to the identity.

**Note:** Accounts that have the **Internal Integration User** field set to `true` in their `sys_user` record will not populate data in the Machine Identity Console.

## Roles and access

The `mi_admin` role gives admin access to the Machine Identity Console. It is a high privilege role because it contains other admin roles, so assign it carefully.

## How data is counted and scored

Some requests aren't counted in the Machine Identity Console, such as maintenance sessions, impersonation sessions, failed logins, MID Server traffic, and requests from internal IP addresses. For the full list, see [Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/machine-identity-metrics.md).

Request records are kept for 30 days, and user tracker records are kept for 180 days. Homepage metrics and scores are computed daily at 00:01 and don't include the current day, so they can be about a day behind the list pages.

The security score is made up of categories. Each active category has an equal share of 100 points, and any remainder goes to the UI login and integration category. For details, see [Security findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/security-score.md).

The categories are:

-   [Accounts using Basic Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/accounts-using-basic-authentication.md)
-   Unique API calls
-   High privilege accounts
-   [Accounts with no login for 100 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/accounts-with-no-login-for-100-days.md)
-   [Integration accounts with Web Service Access set to false](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/integration-accounts-wsa-false.md)
-   [Accounts performing both UI and API login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/accounts-ui-and-api-logins.md)

## Score categories

Each category below contributes to the Machine Identity Security score.

|Category|What it covers|
|--------|--------------|
|Basic authentication|Accounts that authenticate with basic authentication. See [Accounts using Basic Authentication](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/accounts-using-basic-authentication.md).|
|Unique API calls|Unique API calls made in the last 7 days. This data is collected in real time.|
|High privilege accounts|Machine integration accounts that have high privilege roles. This data is collected in real time.|
|No login for 100 days|Accounts that haven't logged in for 100 days. The list uses a 99-day window. See [Accounts with no login for 100 days](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/accounts-with-no-login-for-100-days.md).|
|Integration accounts with WSA disabled|Integration accounts where web service access is disabled. See [Integration accounts with Web Service Access set to false](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/integration-accounts-wsa-false.md).|
|UI login and integration|Accounts that log in through the UI or API. This category also receives any remainder of the score. See [Accounts performing both UI and API login](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/accounts-ui-and-api-logins.md).|

## Data that isn't displayed

The Machine Identity Console doesn't show the following requests. All other requests are shown.

-   Maintenance sessions
-   Impersonation sessions
-   Failed logins
-   Responses with status 400, 401, or 500
-   MID Server traffic
-   Requests from internal IP addresses
-   GraphQL requests
-   OAuth requests that use the authorization code grant type
-   Accounts with the **Internal Integration User** field set to `true`

To change which APIs are collected, use the `sys_mi_resource_filter` table. See [Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/machine-identity-metrics.md).

## Properties

To turn off the Machine Identity Console, set **identity.mi.enabled** to `false`.

|Property|Default|Description|
|--------|-------|-----------|
|**identity.mi.enabled**|`true`|Machine Identity Management feature flag.|
|**identity.mi.buffer.size**|`2097152`|Machine Identity buffer size.|
|**identity.mi.sampling.enabled**|`false`|Machine Identity sampling feature flag.|
|**identity.mi.sampling.window.in.minutes**|`1`|Sampling window, in minutes.|
|**identity.mi.sampling.per.window.threshold**|`500`|Sampling window threshold.|
|**identity.mi.sampling.block.ratio**|`0`|Random sampling ratio.|

## Machine Identity Console tables

|Navigation entry|Table|Retention|
|----------------|-----|---------|
|MI Requests|`sys_mi_request`|30 days|
|MI User Trackers|`sys_mi_user_tracker`|180 days|
|MI Resource Filters|`sys_mi_resource_filter`|Not stated|
|MI Resources|Not confirmed|Not stated|

## Resource filters

The MI Resource Filters table lists the APIs that the Machine Identity Console can collect data for. The **Collect** column shows whether an API is collected.

|API name|Resource|Type|Method|Collect|
|--------|--------|----|------|-------|
|now/amb|ALL|REST|ALL|false|
|now/checklist|ALL|REST|ALL|false|
|now/delegation|ALL|REST|ALL|false|
|now/graphql|ALL|REST|ALL|false|
|now/guidedtour|ALL|REST|ALL|false|
|now/ldap|ALL|REST|ALL|false|
|now/live\_feed|ALL|REST|ALL|false|
|now/map|ALL|REST|ALL|false|
|now/mobileapp|ALL|REST|ALL|false|
|now/push|ALL|REST|ALL|false|
|now/ua|ALL|REST|ALL|false|
|now/ui|ALL|REST|ALL|false|
|now/vtb|ALL|REST|ALL|false|
|sn\_codesearch/code\_search|ALL|REST|ALL|false|
|sn\_devstudio/vcs|ALL|REST|ALL|false|
|sn\_kmf/signature|ALL|REST|ALL|false|

**Related topics**  


[Activating Machine Identity Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/activate-machine-identity-console.md)

[Security findings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/security-score.md)

[Metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/machine-identity-metrics.md)

[Machine Identity Console Settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/machine-identity-console-settings.md)

[Inbound integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-security/identity/inbound-integrations.md)

