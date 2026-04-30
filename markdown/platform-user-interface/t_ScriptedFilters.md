---
title: Create scripted filters
description: The condition builder alone cannot create some filters, such as displaying a record set that depends on an unrelated table. If you know JavaScript, you can create JavaScript functions for use in advanced filters.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Filter admin functions, Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create scripted filters

The condition builder alone cannot create some filters, such as displaying a record set that depends on an unrelated table. If you know JavaScript, you can create JavaScript functions for use in advanced filters.

## Before you begin

Role required: admin

## Procedure

1.  Create a new script include.

    1.  Navigate to **All** &gt; **System Definition** &gt; **Script Includes**.

    2.  Click **New**.

    3.  Fill out the form, and then select **Submit**.

2.  Open the script include and, in the **Script** field, create a JavaScript function that returns an array of `sys_ids`.

    -   Ensure that the function uses the same name as the script include.
    -   Ensure that the script include is **Active** and **Client callable**.
3.  Call the JavaScript function from the condition builder.

    For more information, see [GlideRecord](https://www.servicenow.com/docs/access?context=p_GlideServerAPIs&version=yokohama&pubname=yokohama-api-reference&section=c_GlideRecord&ft:locale=en-US) queries and [Script includes](https://www.servicenow.com/docs/access?context=c_ScriptIncludes&version=yokohama&pubname=yokohama-api-reference&ft:locale=en-US).

    **Note:** Grouped lists with a script include in the filter may cause slowness.


## Example

A company provides intensive care for a group of customers. To track these services, the service manager needs a high-level journal and links to all incidents that the customers raise.

The company creates an application, Intensive Care, and a table, \[u\_intensive\_care\]. While the table contains a reference field for the customer name, there is no direct link to the user table. Thus, the manager cannot set up an incident list filter using the condition builder for customers who are under intensive care.

The solution is to write a JavaScript function that uses a GlideRecord query to build an array of user sys\_ids in the \[u\_intensive\_care\] table, as shown in the sample code below. Call the function from the condition builder in the Incident table \(**\[Caller\] \[is\] \[javascript:myFunction\(\)\]**\).

```
function myFunction(){ 
    var arrUsers = [];
    var gr = new GlideRecord('u_intensive_care');
    gr.query(); 
    while(gr.next()){
        arrUsers.push(gr.u_customer.toString()); 
    }
    return arrUsers;
}
```

**Parent Topic:**[Filter admin functions](../concept/filter-admin-functions.md)

**Related topics**  


[Create and edit filters](t_EditingSavedFilters.md)

[Delete filters](t_DeletingFilters.md)

[Create a dynamic filter option](t_DynamicFilterOptions.md)

