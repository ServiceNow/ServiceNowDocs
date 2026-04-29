---
title: Add transactions by user related list
description: This example adds a relationship, Last 20 transactions, to the user form.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Create defined related lists, Related lists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Add transactions by user related list

This example adds a relationship, Last 20 transactions, to the user form.

## Before you begin

Role required: admin

## About this task

The new relationship creates a list of task records opened by the current user.

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Relationships**.

2.  Click **New**.

3.  Create a relationship with the following values.

<table id="choicetable_inp_1qj_5r"><tbody><tr><td id="d123262e84">

**Name**

</td><td>

Last 20 transactions

</td></tr><tr><td id="d123262e93">

**Applies to table**

</td><td>

User \[sys\_user\]

</td></tr><tr><td id="d123262e102">

**Queries from table**

</td><td>

Task \[task\]

</td></tr><tr><td id="d123262e111">

**Queries with**

</td><td>

```
current.addQuery('opened_by', parent.sys_id);
```

</td></tr></tbody>
</table>4.  Click **Submit**.

5.  Navigate to **User Administration** &gt; **Users**.

6.  Select any user.

    For example, select David Loo.

7.  Configure the related lists for the user form and add the related list **Last 20 transactions**.

8.  Navigate to **User Administration** &gt; **Users**.

9.  Select any user.

    For example, select David Loo.

10. The **Last 20 transactions** related list displays all task records opened by the current user.


## What to do next

Notes and limitations:

-   This query returns all task records opened by the user. The related list defaults to displaying 20 task records per page.
-   The parent variable refers to the **Applies to table**. In this case, it applies to the User \[sys\_user\] table.
-   Querying against a record sys\_id is a common query method for relationships.

**Parent Topic:**[Create defined related lists](t_CreateDefinedRelatedLists.md)

**Related topics**  


[Add a related list to a form](https://www.servicenow.com/docs/access?context=configure-form-layout&version=australia&pubname=australia-platform-administration&section=t_AddARelatedList&ft:locale=en-US)

