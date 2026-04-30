---
title: Display function results in a database view
description: Add a function field to the output of a database view to see function results.
locale: en-US
release: xanadu
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Displaying function results in a database view, Work with database views, Table administration, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Display function results in a database view

Add a function field to the output of a database view to see function results.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Database Views**.

2.  Select a database view.

3.  Select the **Try it** related link.

4.  Add the function field to the database view output.

    See [Configure items on forms or in lists using a list collector](https://www.servicenow.com/docs/access?context=t_UseSlushbuckets&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).

5.  Review the function definition if the expected value is not returned or a returned value indicates the function definition is invalid.

    -   If the message **Invalid function** is returned, the function definition is invalid for string field types.
    -   If an empty value is returned, the function definition is invalid for other field types.
    -   If an unexpected value is returned, review the field definition in the function definition.

## Result

The function field operation is executed and the results appear in the database view output.

**Parent Topic:**[Displaying function results in a database view](displaying-function-results-in-a-database-view.md)

