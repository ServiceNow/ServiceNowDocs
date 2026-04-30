---
title: Increase payload limit through system properties in AI Desktop Actions
description: By default, maximum 10 MB of file size is allowed in a scripted REST API request payload. Increase the payload limit to 15 MB by creating system properties in the global scope.
locale: en-US
release: zurich
topic_type: task
last_updated: "2026-02-02"
reading_time_minutes: 1
breadcrumb: [Design desktop actions, AI Desktop Actions, Enable AI experiences]
---

# Increase payload limit through system properties in AI Desktop Actions

By default, maximum 10 MB of file size is allowed in a scripted REST API request payload. Increase the payload limit to 15 MB by creating system properties in the global scope.

## Before you begin

You must do this procedure in the ServiceNow instance.

Role required: system admin

## About this task

If you already have these properties configured for your instance, you can update the value to 15 MB to increase the limit.

## Procedure

1.  Navigate to **All**.

2.  In the filter navigator, enter `sys_properties.list`.

3.  In the System Properties table, select **New** to add the glide.rest.max\_content\_length property.

    1.  On the form, fill in the fields.

        |Field|Description|Value|
        |-----|-----------|-----|
        |Name|Name of this system property|glide.rest.max\_content\_length|
        |Description|Explanation for this property|For example: `Revised payload for a scripted REST request body.`|
        |Type|Data type of this system property|integer|
        |Value|The maximum size, in megabytes, for a scripted REST request body. The default value is 10 MB.|15|

    2.  Select **Submit**.

4.  In the System Properties table, select **New** to add the glide.rest.scripted.max\_inbound\_content\_length\_mb property.

    1.  On the form, fill in the fields.

<table id="table_lj2_vpz_d3c"><thead><tr><th>

Field

</th><th>

Description

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of this system property

</td><td>

glide.rest.scripted.max\_inbound\_content\_length\_mb

</td></tr><tr><td>

Description

</td><td>

Explanation for this property

</td><td>

For example: `Revised payload for a scripted REST request body.`

</td></tr><tr><td>

Type

</td><td>

Data type of this system property

</td><td>

integer

</td></tr><tr><td>

Value

</td><td>

The maximum size, in megabytes, for a scripted REST request body. The default value is 10 MB.**Note:** Even if glide.rest.scripted.max\_inbound\_content\_length\_mb is set, the request body is limited to the value of glide.rest.max\_content\_length.

</td><td>

15

</td></tr></tbody>
</table>    2.  Select **Submit**.


