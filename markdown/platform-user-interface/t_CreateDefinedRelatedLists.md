---
title: Create defined related lists
description: You can add default related lists to the form for all users to see when viewing records.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Related lists, Forms in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Create defined related lists

You can add default related lists to the form for all users to see when viewing records.

## Before you begin

Role required: admin

## About this task

For example, you may include a list of related incidents at the bottom of a problem record, or a list of members at the bottom of a group record. This functionality depends on reference fields or many-to-many table relationships. If two tables are related via the system dictionary, one can appear as a related list on the other.

Defined related lists allow relationships between arbitrary tables to be expressed as a related list. Any two tables that can have a logical relationship can appear as a parent/child pair via a related list. The following are some examples.

-   On an incident record, show all incidents opened by the same caller.
-   On a user record, show the last 20 transactions that user has made.
-   On an incident record, show all problems opened on the reported CI.

These relationships are beyond the relationships normally defined in the system dictionary through reference fields and many-to-many relationships.

Every related list requires a relationship record. Before creating a relationship, verify that there is not an existing relationship record that already provides the needed information. Use the following steps to create a relationship record.

## Procedure

1.  Click **System Definition** &gt; **Relationships**.

2.  Click **New**.

3.  Specify the relationship record fields.

<table id="table_rqf_w5c_xp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Type the name of the related list. The form configuration page displays this name in the list of available lists.

</td></tr><tr><td>

Advanced

</td><td>

Select this check box to use JavaScript in place of the **Applies to table** and **Queries from table** fields.

</td></tr><tr><td>

Applies to table

</td><td>

Select the table on which the related list appears. For example, to add a related list to the user form, select the User \[sys\_user\] table.

This field is hidden in Advanced relationship records.

</td></tr><tr><td>

Queries from table

</td><td>

Select the table from which this related list retrieves data. For example, to add related task records to the related list, select the Task \[task\] table.

This field is hidden in Advanced relationship records.

</td></tr><tr><td>

Apply to

</td><td>

Type a script that sets the *answer* variable to **true** when a user opens a form on the desired table. This field is only visible with the **Advanced** check box selected.

</td></tr><tr><td>

Query from

</td><td>

Type a script that sets the *answer* variable to the name of the table from which the related list retrieves data. This field is only visible with the **Advanced** check box selected.

</td></tr><tr><td>

Query with

</td><td>

Specify the records to include by typing a script.For example:

```
current.addQuery('opened_by', parent.sys_id);
```

-   The `current` object specifies the current record on which the script is triggered.
-   The `addQuery` method adds a filter that returns records meeting a specified condition.
-   The `opened_by` variable is the field name you're querying in the table from **Queries from table**.
-   The `parent.sys_id` variable refers to the **Applies to table** and the ID of the record being displayed.


</td></tr><tr><td>

Insert Callback

</td><td>

Type a script to run after a successful insert action. This field is only visible with the **Advanced** check box selected.

</td></tr></tbody>
</table>4.  Click **Submit**.


-   **[Add incidents by same caller related list](t_ExampleIncidentsBySameCaller.md)**  
This example adds the existing relationship, Incidents by Same Caller, to incident forms.
-   **[Add transactions by user related list](t_ExampleTransactionsByUser.md)**  
This example adds a relationship, Last 20 transactions, to the user form.

**Parent Topic:**[Related lists](../../../use/using-forms/concept/c_RelatedLists.md)

**Related topics**  


[Select or create records in a related list](../../../use/using-forms/task/t_SelectRelatedRecords.md)

[Configure when a related list loads](../../../use/using-forms/task/t_ConfigureWhenARelatedListLoads.md)

[Create a default filter for a related list](../../../use/using-forms/task/t_CreateADefaultFilter.md)

[Configure the edit option](../../../use/using-forms/task/t_ConfigureTheEditOption.md)

[Add fields to selections in a related list](t_AddingFieldsToARelatedList.md)

[Create a default filter for list selector records](t_CreateDefaultRelatedRecSecFilter.md)

