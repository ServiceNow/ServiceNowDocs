---
title: Search a list
description: You can search a list to find information quickly. The list title bar includes options for searching the list. Administrators can enable text searches for any list.The platform supports several wildcard characters to expand and refine search results.The default search behavior in a list is to search for values that are greater than or equal to the value you enter. Administrators can add properties to change the search behavior to use either a contains search or a starts with search by default, instead of a greater than search.Change the default search behavior at the field level by adding an attribute to a field using the system dictionary.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Search a list

You can search a list to find information quickly. The list title bar includes options for searching the list. Administrators can enable text searches for any list.

## Before you begin

Role required: none

## About this task

There are two options for searching the list: for a string in a selected field, or for a text string found in any field. These options are labeled **Go to** and **Search**.

-   The **Go to** option sorts the list by the selected field and returns records where the field value is equal to or greater than the search term. For the **Number** field, which is a string type field, it finds the records that have a number ending with the number that you enter. For example, searching a list of incidents by selecting **Number** and entering `4` shows records with numbers like **INC0000004** and **INC0000014**.
-   The **Search** option appears when you select **for text**. It returns records that contain the search term in any field in the list table. If you added a related list condition, the search does not include records in the related table.

Each option in a choice list is defined with a column label and a value. For example, the incident **State** field contains several options, such as **New** and **Closed**. These labels are column labels, and each one has an underlying value. For incidents, the default value for **New** is **1** and the default value for **Closed** is **7**. You can search a column for either the column label or the value with the following results.

-   Enter the column label to list matching records, for example, all incident records in the **New** state.
-   Enter the value to find records that have a state greater than or equal to \(=&gt;\) the specified value. For example, enter **6** to list incident records in the **Resolved** and **Closed** states.

## Procedure

1.  Navigate to a list of records.

2.  If necessary, personalize the list to add the desired fields.

3.  Select a field or select **for text**.

    ![Go to](../image/GoToUI16.png)

    ![Search](../image/SearchListUI16.png)

4.  Enter the search text.

    Use wildcards to further refine list searches.

5.  Press the Enter key to execute the search.


**Parent Topic:**[Lists in the classic environment](../concept/c_UseLists.md)

## Available list search wildcards

The platform supports several wildcard characters to expand and refine search results.

<table id="table_jht_2xz_bz"><thead><tr><th>

Wildcard

</th><th>

Description

</th></tr></thead><tbody><tr><td>

\*search-term

 %search-term%

</td><td>

Search for values that contain search-term.

</td></tr><tr><td>

%search-term

</td><td>

Search for values that end with search-term.

</td></tr><tr><td>

search-term%

</td><td>

Search for values that start with search-term.

</td></tr><tr><td>

=search-term

</td><td>

Search for values that equal search-term.

</td></tr><tr><td>

!\*search-term

</td><td>

Search for values that don't contain search-term.

</td></tr><tr><td>

!%search-term

</td><td>

Search for values that start end with search-term.

</td></tr><tr><td>

!=search-term

</td><td>

Search for values that don't equal search-term.

</td></tr></tbody>
</table>**Note:** Reference fields support a different set of wildcard operators. For details on using wildcards to search reference field auto-complete values, see [Auto-complete for reference fields](https://www.servicenow.com/docs/access?context=c_AutoCompleteForReferenceFields&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

## Configure the default search behavior

The default search behavior in a list is to search for values that are greater than or equal to the value you enter. Administrators can add properties to change the search behavior to use either a contains search or a starts with search by default, instead of a greater than search.

### Before you begin

Role required: admin

### About this task

If you enter text in the search box without using a wildcard, the search is performed for values greater than or equal to the value you enter. For text data-type-fields, this means that the search first sorts the records on the selected field, then finds the first record that starts with the text and all following records. For numeric data-type-fields, this means that the search finds all records where the number field ends with the entered number.

**Note:** The system treats some string fields that contain record numbers as numeric fields. Any field named number or u\_number is treated as a numeric field.

Changing the default search behavior to contains or starts with can cause performance issues as both search options return more results than a greater than search.

### Procedure

1.  Navigate to the list of system properties by typing `sys_properties.list` into the navigation filter.

2.  Add one of the following properties depending on your default search behavior preferences.

<table id="table_s4q_pmb_qcb"><thead><tr><th>

Name

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**glide.ui.goto\_use\_contains**

</td><td>

Changes the default search behavior for a list to a contains search.-   Type: true \| false
-   Value: true


</td></tr><tr><td>

**glide.ui.goto\_use\_starts\_with**

</td><td>

Changes the default search behavior for a list to a starts with search.-   Type: true \| false
-   Value: true


</td></tr></tbody>
</table>3.  Click **Submit**.


**Related topics**  


[Add a property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US)

### Configure default search behavior using a dictionary attribute

Change the default search behavior at the field level by adding an attribute to a field using the system dictionary.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Dictionary**.

2.  Search for the field in a table that you want to apply the default search attribute to.

3.  In the Attributes field, add one of the following attributes.

    **Note:** You may need to switch to the advanced view for the dictionary entry to see the attributes field.

    |Attribute|Description|
    |---------|-----------|
    |**goto\_use\_starts\_with=true**|Changes the default search behavior to use the starts with operator for a specific field. Applying starts with to a non-text field returns any data starting with that search, which can cause performance degradation.|


