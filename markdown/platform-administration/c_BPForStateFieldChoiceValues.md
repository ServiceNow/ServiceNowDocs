---
title: Configure state field choice values
description: State fields are a subset of choice list fields. Keep the following information in mind when you configure choice values for the state field.Follow these examples for modifying the states of incidents and change requests.Business rules in the system make assumptions about state values. You can troubleshoot business rules to see the order in which they run and see how it affects changes you make to State field values.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Choice list field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure state field choice values

State fields are a subset of choice list fields. Keep the following information in mind when you configure choice values for the state field.

-   Use a negative value to add a new active state field.
-   Search for and study the business rules that use a state number filter on the **Script** and **Conditions** fields. You can use the Debug tool to trace the order of the business rule execution.
-   New values representing inactive states should have a value above 8.

You can define any of the following attributes for a state field by configuring the dictionary. If the attributes are not defined, the system uses the default values. The TaskStateUtil API uses the following attributes. For more information on the TaskStateUtil API, see [TaskStateUtil](https://developer.servicenow.com/app.do#!/api_doc?v=paris&id=c_TaskStateUtil).

|Attribute|Definition|
|---------|----------|
|close\_states|Semicolon delimited list of state values that are inactive, used to identify whether the task should be set to active or inactive. This is a required attribute to use the TaskStateUtil functionality.|
|default\_close\_state|Optional attribute to define the state value of the default close state if you want to define business rules that automatically close a task. Defaults to 3, typically Closed Complete if attribute is not defined.|
|default\_work\_state|Optional attribute to define the state value of the default working state if you want to define business rules that automatically set a task for working. Defaults to 2, typically Work in Progress if the attribute is not defined.|

## State modification examples

Follow these examples for modifying the states of incidents and change requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Choice Lists**.

2.  At the top of the list, construct a list filter like the following:

    -   **Table**: incident
    -   **Element**: incident\_state
3.  Run the filter.

    Notice that the **Closed** state has a value of **7** and the **Resolved** state has a value of **6**. Any state greater than or equal to **7** is assumed to be inactive. Therefore, you should use a positive integer greater than **7** if you want to add a new inactive-type of state. Use a negative value like **-1** or **-2** if you wish to add a new active-type of state field, such as **Awaiting Vendor**.

4.  Navigate again to **System Definition** &gt; **Choice Lists**.

5.  At the top of the list, construct a list filter like the following:

    -   **Table**: change\_request
    -   **Element**: phase\_state
6.  Run the filter.

    Notice that the **Complete** state has a value of **8**. Any state greater than or equal to **8** is assumed to be inactive. Therefore, you should use a positive integer greater than **8** if you want to add a new inactive-type of state, such as **Cancelled**. Use a negative value like **-1** or **-2** if you wish to add a new active-type of state field, such as **Pending**.


## Troubleshoot change states and business rules

Business rules in the system make assumptions about state values. You can troubleshoot business rules to see the order in which they run and see how it affects changes you make to **State** field values.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Business Rules**.

2.  Construct a filter like this one to view the scripts and conditions that pertain to the Resolved incident\_state of 6 or the Closed incident\_state value of 7:

    The **Script** field contains 7 OR the **Condition** field contains 7 OR the **Script** field contains 6 OR the **Condition** field contains 6 AND the **Table** field is incident AND the **Active** field is true.


### What to do next

See Debug Business Rule for information on how to trace the order of business rule execution. You can click **Debug All**, resolve an incident, and then check the trace at the bottom of form to watch the business rules execute. These two line examples show that the mark\_closed business rule code is entered `==>` and then exited `<==`.

```

==> 'mark_closed' on incident
<== 'mark_closed' on incident

```

