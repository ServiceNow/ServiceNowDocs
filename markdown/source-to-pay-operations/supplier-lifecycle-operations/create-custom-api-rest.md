---
title: Create a REST message for a custom API
description: Create a REST message request and send it to a custom API endpoint to fetch the latest supplier news.
locale: en-US
release: yokohama
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configuring a custom API to dynamically fetch supplier news, News Integration for Supplier Lifecycle Operations, Integrating Supplier Lifecycle Operations with other applications, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Create a REST message for a custom API

Create a REST message request and send it to a custom API endpoint to fetch the latest supplier news.

## Before you begin

-   Install the News Integration for Supplier Lifecycle Operations plugin \(com.snc.sn\_supplier\_news\).
-   Set the application scope to News Integration for Supplier Lifecycle Operations using the application picker.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Web Services** &gt; **Outbound** &gt; **REST Message**.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name for this message.|
    |Endpoint|Endpoint that this REST message is sent to.|
    |Authentication type|Authentication to use, if any, and the profile record that contains the user credentials.|

4.  Right-click the form header and select **Save**.

    After creating the REST message, a GET HTTP method is created automatically using the values from the REST message record.

5.  In the HTTP Methods related list, select **Default GET**.

6.  In the **Name** field, specify a name for the GET HTTP method.

7.  Select the **HTTP Request** tab.

8.  In the HTTP Headers embedded list, select **Insert a new row**.

9.  In the **Name** field, enter the name of the header.

    Supported headers depend on the REST web service provider that you want to connect to.

10. Double-click the **Value** field for the new row and enter the value that you want to assign to this header.

    You can use a variable in the format $\{variable\} instead of a static value. You can assign a value to the variable when sending a REST request.

11. In the HTTP Query Parameters embedded list, select **Insert a new row**.

12. In the **Name** field, enter the name of the query parameter.

13. Double-click the **Value** field for the new row and enter the value that you want to assign to this query parameter.

    You can use a variable in the format $\{variable\} instead of a static value. You can assign a value to the variable when sending a REST request.

14. Select **Update**.


## What to do next

[Add and configure the Get News data resource in UI Builder](add-config-news-data-resource.md).

**Parent Topic:**[Configuring a custom API to dynamically fetch supplier news](../concept/config-supplier-news-api.md)

**Previous topic:**[Configuring a custom API to dynamically fetch supplier news](../concept/config-supplier-news-api.md)

**Next topic:**[Add and configure the Get News data resource in UI Builder](add-config-news-data-resource.md)

