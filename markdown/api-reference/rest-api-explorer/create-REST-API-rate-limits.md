---
title: Create an inbound REST API rate limit
description: Create rate limit rules to limit the number of inbound REST API requests processed per hour.
locale: en-US
release: zurich
product: REST API Explorer
classification: rest-api-explorer
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Inbound REST API rate limiting, REST APIs, Web services, API implementation, API implementation and reference]
---

# Create an inbound REST API rate limit

Create rate limit rules to limit the number of inbound REST API requests processed per hour.

## Before you begin

Role required: rate\_limit\_admin

## About this task

Set rate limits for all users, users with specific roles, or all users.

**Note:** As requests reach an instance, each node maintains a rate limit count per user. Every 30 seconds, the count is committed to the database. As a result, a rate limit rule may not take effect for up to 30 seconds.

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **REST** &gt; **Rate Limit Rules**.

2.  Click **New** and enter the following field values.

<table id="table_y41_qgq_hdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

REST API resource

</td><td>

Value derived from the values entered at the following fields.

</td></tr><tr><td>

Name

</td><td>

Unique name for the rate limit rule.

</td></tr><tr><td>

REST API

</td><td>

REST API selected from the list of all external-facing REST APIs for the instance.

</td></tr><tr><td>

Version

</td><td>

Version of the **REST API**. Values listed depend on the **REST API** selected.

</td></tr><tr><td>

Resource

</td><td>

Resource for the **Version**. Values listed depend on the **Version** selected.

</td></tr><tr><td>

Table

</td><td>

Table that you want to target. Appears only when you select **Table API** as the **REST API**.

</td></tr><tr><td>

Import set table

</td><td>

Import set table that you want to target. Appears only you select **Import Set API** as the **REST API**.

</td></tr><tr><td>

Active

</td><td>

Check box to indicate that the rate limit rule is active.Rate limit rules are activated by default as soon as you create them. You can deactivate rate limit rules to stop enforcing a rate limit or activate rate limit rules to resume enforcing a rate limit.

</td></tr><tr><td>

Request limit per hour

</td><td>

Maximum number of requests allowed per hour.**Note:** Whenever you update the value of this field, the ServiceNow AI Platform resets the count of requests to 0 and deletes all violations for the current hour.

</td></tr><tr><td>

Apply to

</td><td>

Users restricted by this rule:-   **Single user** applies the rate limit to a specific user.
-   **Users with role** applies the rate limit to all users with a specific role.
-   **All users** applies the rate limit to all users.


</td></tr><tr><td>

Role

</td><td>

Role to which the rate limit applies. Appears only when you select **Users with role** at the **Apply to** field.

</td></tr><tr><td>

User

</td><td>

User to whom the rate limit applies. Appears only when you select **Single user** at the **Apply to** field.

</td></tr></tbody>
</table>3.  Click **Submit**.

    The new rate limit goes into effect.


## What to do next

After you submit the rule, the ServiceNow AI Platform adds the following related lists to the rule record:

-   **Rate Limit Counts**

    Lists, by user, the number of inbound REST API requests affected by this rate limit rule.

-   **Rate Limit Violations**

    Lists, by user, the violations of this rate limit rule.


You can use these related lists to [Monitor inbound REST API rate limit counts and violations](monitor-request-counts.md).

**Parent Topic:**[Inbound REST API rate limiting](../concept/inbound-REST-API-rate-limiting.md)

