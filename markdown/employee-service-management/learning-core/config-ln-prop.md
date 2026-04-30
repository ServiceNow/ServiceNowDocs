---
title: Configure properties for Learning Core
description: Configure properties for various settings used in Learning Core.
locale: en-US
release: zurich
product: Learning Core
classification: learning-core
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administration tasks, Configure, Learning Core overview, HR Service Delivery, Employee Service Management]
---

# Configure properties for Learning Core

Configure properties for various settings used in Learning Core.

## Before you begin

Role required: learning\_admin

## Procedure

1.  Navigate to **Learning** &gt; **Administration** &gt; **Properties**.

2.  Configure the name of the portal that must open when the learning task is clicked in an email.

3.  Navigate to **System Properties** and set the following property values:

<table id="table_kxp_b22_kqb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

com.glide.transform.json.max-partial-length

</td><td>

Transforms JSON objects to internal objects and sets the word limit for records fetched through an API call.-   **Type:** integer
-   **Default value:** 16384
-   **Recommended value:**1638400
 **Note:**

You must add this system property to set the desired value.

When you synchronize third-party learning content with your ServiceNow instance, if the word count of the content being pulled into your instance exceeds the value set for this property, the synchronization will fail.

</td></tr><tr><td>

com.snc.process\_flow.reporting.serialized.val\_size\_limit

</td><td>

Specify the number of bytes allowed for runtime values in each step in the flow execution details. To prevent truncation, set the value to an integer equal to or less than zero.-   **Type:** integer
-   **Default value:** 16384
-   **Recommended value:**1638400
 **Note:** When you synchronize third-party learning content with your ServiceNow instance, if the word count of the content being pulled into your instance exceeds the value set for this property, the synchronization will fail.

</td></tr></tbody>
</table>    **Note:** These properties set a word limit for records that are fetched through an API call. API call fails when the word limit goes beyond the **1638400** limit.


**Parent Topic:**[Administration tasks in Learning Core](ln-administration.md)

