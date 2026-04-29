---
title: Inbound REST API rate limiting
description: To prevent excessive inbound REST API requests, set rules that limit the number of inbound REST API requests processed per hour. You can create rules to limit requests for specific users, users with specific roles, or all users.
locale: en-US
release: australia
product: REST API Explorer
classification: rest-api-explorer
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Inbound REST API rate limiting

To prevent excessive inbound REST API requests, set rules that limit the number of inbound REST API requests processed per hour. You can create rules to limit requests for specific users, users with specific roles, or all users.

Rate limit rules are created in the Rate Limit Rules \[sys\_rate\_limit\_rules\] table.

**Note:** As requests reach an instance, each node maintains a rate limit count per user. Every 30 seconds, the count is committed to the database. As a result, a rate limit rule may not take effect for up to 30 seconds.

## Rate limiting priority

If an inbound REST API request matches multiple rate limit rules for the same resource, rate limiting priority is enforced as follows:

-   Rules set for **Single user** override rules for **All users** and rules for **Users with role**.
-   Rules set for **Users with role** override rules for **All users**.

In this example, there are four rate limit rules for the REST API resource `GET /now/v2/table/incident`.

![List of rate limit rules for GET /now/v2/table/incident.](../image/rate-limit-rules.png)

These rate limit rules are applied in the following order:

1.  **Limit incidents by user** applies to ITIL User, who can submit up to 200 requests per hour.
2.  **Limit incidents by import admin** applies to all users with the import\_admin role. Each user with the import\_admin role can submit up to 500 requests per hour.
3.  **Limit incidents by itil** applies to all users with the itil role. Each user with the itil role can submit up to 100 requests per hour.
4.  **Limit incidents** applies to all users. Each user can submit up to 100 requests per hour.

When ITIL User makes the request `GET /now/v2/table/incident`, the request matches the criteria for three rules: **Limit incidents**, **Limit incidents by itil**, and **Limit incidents by user**. Only the **Limit incidents by user** rule is applied because it takes precedence over the other rules. As a result, ITIL User can submit a maximum of 200 requests per hour.

If a user has two or more roles matching the criteria of multiple rate limiting rules for a REST API resource, the rule allowing the lowest number of requests applies to the user's requests for the resource. For the example rules in the figure above, assume that user Abel Tuter has both the import\_admin role and the itil role. When Abel Tuter submits a request, it meets the criteria for both the **Limit incidents by admin** rule and the **Limit incidents by itil** rule. Only the **Limit incidents by itil** rule is applied because it allows the lowest number of requests. As a result, Abel Tuter can submit a maximum of 100 requests per hour.

## REST API response headers

You can generate inbound REST API requests using the [REST API Explorer](use-REST-API-Explorer.md) or an HTTP client, such as Postman API platform. If the request matches a rate limit rule, several HTTP response headers provide information about rate limiting.

-   **X-RateLimit-Limit** displays the number of requests allowed per hour.
-   **X-RateLimit-Reset** displays a UNIX timestamp for the next scheduled reset of the rate limit window.
-   **X-RateLimit-Rule** displays the sys\_id of the rate limit rule \[sys\_rate\_limit\_rules\] that is being enforced.

If a request is denied because it exceeds the rate limit, the system returns a **Retry-After** response header in addition to the response headers about rate limiting. The **Retry-After** response header displays the number of seconds after which you can retry the request to avoid exceeding the rate limit. The following error response is returned:

```
{
    "error": {
        "message": "Rate limit exceeded",
        "detail": "Rate limit of 100 requests per hour for Table API exceeded"
    },
    "status": "failure"
}
```

The status code of a denied request is `429 Too Many Requests`.

-   **[Create an inbound REST API rate limit](../task/create-REST-API-rate-limits.md)**  
Create rate limit rules to limit the number of inbound REST API requests processed per hour.
-   **[Reset an inbound REST API rate limit](../task/reset-rest-api-rate-limits.md)**  
Reset a rate limit rule to reset the rate limit count to zero \(0\) and delete any violations for the current hour.
-   **[Monitor inbound REST API rate limit counts and violations](../task/monitor-request-counts.md)**  
To determine if you have set a rate limit rule appropriately, monitor the counts and violations for inbound REST API requests that are restricted by the rule.
-   **[Investigate inbound REST API rate limit violations](../task/investigate-rate-limit-violations.md)**  
Investigate rate limit violations to determine which rate limit rules are being exceeded and which users are exceeding those rate limits.

**Parent Topic:**[REST APIs](c_RESTAPI.md)

