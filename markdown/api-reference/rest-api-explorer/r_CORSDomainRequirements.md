---
title: CORS domain requirements
description: When you define a cross-origin resource sharing \(CORS\) rule, the value you enter in the Domain field must meet certain requirements. Each CORS rule supports a single wildcard to match incoming Origin headers.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# CORS domain requirements

When you define a cross-origin resource sharing \(CORS\) rule, the value you enter in the **Domain** field must meet certain requirements. Each CORS rule supports a single wildcard to match incoming Origin headers.

## Requirements

The value you enter in the **Domain** field must meet the following requirements.

-   Begins with `HTTP://` or `HTTPS://`.
-   Is a domain pattern or IP address.
-   Ends with alphanumeric characters preceded by a period, such as `.com`.
-   Includes at most a single wildcard character immediately following the scheme and hierarchical portion of the domain pattern.

## Wildcard

You can use a single wildcard character \(\*\) in the domain pattern. Use this wildcard immediately following the scheme and hierarchical portion of the domain pattern, such as `http://*.domain.com` to include all subdomains. The wildcard must immediately follow the scheme and hierarchical portion of the domain pattern. If you use an IP address instead of domain pattern, you must enter the full IP address without a wildcard.

**Note:** You cannot use multiple wildcards, or specify a wildcard without a domain pattern. Values such as \* or \*.\* are not supported.

## Domain matching

When evaluating the Origin header in a request, ServiceNow prioritizes rules that match the domain pattern exactly. If no exact match is found, the next closest match is used.

For example, if there are rules for the domain patterns `http://*.blog.mysite.com` and `http://*.mysite.com`, a request from `http://alice.blog.mysite.com` will match the `http://*.blog.mysite.com` pattern.

## Examples of valid and invalid domains

|Valid domain|Invalid domain|
|------------|--------------|
|`http://*.ms.net`|`https://*com`|
|`https://*.ms.com`|`http://*..com`|
|`https://*.com.au`|`http://192.168.1.*`|
|`http://192.168.1.1`|`http://*.168.1.126`|
|`http://*.service-now.com`|`http://blog.*.service-now.com`|
|`http://*.com`|`http://*com`|

**Parent Topic:**[REST APIs](../concept/c_RESTAPI.md)

