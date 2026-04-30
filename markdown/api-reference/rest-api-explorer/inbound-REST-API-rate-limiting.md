---
title: Inbound REST API rate limiting
description: To prevent excessive inbound REST API requests, set rules that limit the number of inbound REST API requests processed per hour. You can create rules to limit requests for specific users, users with specific roles, or all users.
locale: en-US
release: xanadu
product: REST API Explorer
classification: rest-api-explorer
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [REST APIs, Web services, API implementation, API implementation and reference]
---

# Inbound REST API rate limiting

To prevent excessive inbound REST API requests, set rules that limit the number of inbound REST API requests processed per hour. You can create rules to limit requests for specific users, users with specific roles, or all users.

**Note:** As requests reach an instance, each node maintains a rate limit count per user. Every 30 seconds, the count is committed to the database. As a result, a rate limit rule may not take effect for up to 30 seconds.

## Rate limiting priority

If an inbound REST API request matches multiple rate limit rules for the same resource, rate limiting priority is enforced as follows:

-   Rules set for **Single user** override rules for **All users** and rules for **Users with role**.
-   Rules set for **Users with role** override rules for **All users**.

In this example, there are four rate limit rules for the same REST API resource: `GET /now/v2/table/incident`:

![Rate Limit Rules](../image/rate-limit-rules.png)

These rate limit rules are applied in the following order:

1.  **Limit Incidents by User** applies to ITIL User, who can submit up to 10 requests per hour.
2.  **Limit Incidents by import admin Role** applies to each user with the import\_admin role. Each user with the import\_admin role can submit up to three requests per hour.
3.  **Limit Incidents by itil Role** applies to each user with the itil role. Each user with the itil role can submit up to five requests per hour.
4.  **Limit Incidents** applies to all users. Each user can submit up to two requests per hour.

When ITIL User makes the request `GET /now/v2/table/incident`, the request matches the criteria for three rules: **Limit Incidents**, **Limit Incidents by itil Role**, and **Limit Incidents by User**. Only the **Limit Incidents by User** rule is applied because it takes precedence over the other rules. As a result, ITIL User can submit a maximum of 10 requests per hour.

If a user has two or more roles matching the criteria of multiple rate limiting rules for a REST API resource, the rule allowing the lowest number of requests applies to the user's requests for the resource. For the example rules in the figure above, assume that user Abel Tuter has both the import\_admin role and the itil role. When Abel Tuter submits a request, it meets the criteria for both the **Limit Incidents by admin Role** rule and the **Limit Incidents by itil Role** rule. Only the **Limit Incidents by admin Role** rule is applied because it allows the lowest number of requests. As a result, Abel Tuter can submit a maximum of three requests per hour.

## REST API response headers

You can generate inbound REST API requests using the [Use the REST API Explorer](use-REST-API-Explorer.md) or an HTTP client, such as Postman. If the request matches a rate limit rule, several HTTP response headers provide information about rate limiting:

-   **X-RateLimit-Limit** displays the number of requests allowed per hour.
-   **X-RateLimit-Reset** displays the Unix time until the next scheduled reset.
-   **X-RateLimit-Rule** displays the sys\_id of the rate limit rule that is being enforced.

    ![Rate limit response headers](../image/rest-api-request-headers-processed.png)


If a request is denied because it exceeds the rate limit, the system returns a **Retry After** response header in addition to the response headers about rate limiting. The **Retry After** response header displays the number of seconds after which you can retry the request to avoid exceeding the rate limit. The following error response is returned:

```
{
    "error": {
        "message": "Rate limit exceeded",
        "detail": "Rate limit of 10 requests per hour for Table API exceeded"
    },
    "status": "failure"
}
```

The status of a denied request is `429 Too Many Requests`.

![REST response status 429 Too Many Requests](../image/rest-api-request-headers-denied.png)

-   **[Create an inbound REST API rate limit](../task/create-REST-API-rate-limits.md)**  
Create rate limit rules to limit the number of inbound REST API requests processed per hour.
-   **[Reset an inbound REST API rate limit](../task/reset-rest-api-rate-limits.md)**  
Reset a rate limit rule to reset the rate limit count to zero \(0\) and delete any violations for the current hour.
-   **[Monitor inbound REST API rate limit counts and violations](../task/monitor-request-counts.md)**  
To determine if you have set a rate limit rule appropriately, monitor the counts and violations for inbound REST API requests that are restricted by the rule.
-   **[Investigate inbound REST API rate limit violations](../task/investigate-rate-limit-violations.md)**  
Investigate rate limit violations to determine which rate limit rules are being exceeded and which users are exceeding those rate limits.

**Parent Topic:**[REST APIs](c_RESTAPI.md)

