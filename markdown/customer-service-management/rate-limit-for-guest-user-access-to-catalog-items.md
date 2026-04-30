---
title: Rate limit rule form for guest user access to catalog items
description: The REST API Rate Limit Rule form enables you to set the number of API requests in an hour by guest users.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Portal reference, Reference, Customer Service Management]
---

# Rate limit rule form for guest user access to catalog items

The REST API Rate Limit Rule form enables you to set the number of API requests in an hour by guest users.

<table id="table_y41_qgq_hdb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

REST API resource

</td><td>

Rest API resource. This field is auto-populated depending on the values entered in the other fields.

</td></tr><tr><td>

Name

</td><td>

Unique name for the rate limit rule.

</td></tr><tr><td>

REST API

</td><td>

REST API selected from the list of all external-facing REST APIs for the instance.Select **Service catalog**.

</td></tr><tr><td>

Version

</td><td>

Version of the REST API. Values listed depend on the REST API selected.Select **latest**.

</td></tr><tr><td>

Resource

</td><td>

Resource for the version. Values listed depend on the Version selected.

 For example,

 -   Buy Item
-   Submit a Record Producer
-   Validate Variable Regex \(If the item consists of a variable which requires Regex Validation\)
-   Checkout Order Guide
-   Variable display value
-   Check requested for delegation on item

</td></tr><tr><td>

Active

</td><td>

Check box to indicate that the rate limit rule is active.Rate limit rules are activated by default as soon as you create them. You can deactivate rate limit rules to stop enforcing a rate limit or activate rate limit rules to resume enforcing a rate limit.

</td></tr><tr><td>

Request limit per hour

</td><td>

Maximum number of requests permitted in an hour.**Note:** Whenever you update the value of this field, the ServiceNow AI Platform resets the count of requests to 0 and deletes all violations for the current hour.

</td></tr><tr><td>

Apply to

</td><td>

Users restricted by this rule:

-   **Single user** applies the rate limit to a specific user.
-   **Users with role** applies the rate limit to all users with a specific role.
-   **All users** applies the rate limit to all users.

Select **Users with role**.

</td></tr><tr><td>

Role

</td><td>

Role to which the rate limit applies.

Select **public**.**Note:** Appears only when you select **Users with role** at the **Apply to** field.

</td></tr></tbody>
</table>