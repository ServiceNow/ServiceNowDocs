---
title: Encoded query strings
description: An encoded query string represents a complex filter on a list of records.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Filters and breadcrumbs, Lists in the classic environment, Working in the classic environment, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Encoded query strings

An encoded query string represents a complex filter on a list of records.

Use encoded query strings to include a filter as part of a URL parameter, such as the [Navigate to a record or module using a URL](../../navigation/task/navigate-using-url.md), or as a [reference qualifier](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ReferenceQualifiers.md) to restrict the data that is selectable for a reference field.

To construct an encoded query string, generate a list query and then [copy it from the list filter](../task/t_GenEncodQueryStringFilter.md). This is the preferred method because the alternative is to create the string manually.

In order to create an encoded query string manually, you need to know the relevant table and field names and [operators](../../common-ui-elements/reference/r_OpAvailableFiltersQueries.md).

<table id="table_hkc_kvp_pq"><thead><tr><th>

Title

</th><th>

Example

</th></tr></thead><tbody><tr><td>

Referring to Boolean or string values

</td><td>

To create a query string on Boolean fields, use this syntax: field=true or field=false. For example, to return only active records in a table, use:```
active=true
```

 To create a query string with a field that has a specific string value, use this syntax: field=value. For example, to return incident records where the category is network, use:

 ```
category=network
```

</td></tr><tr><td>

Referring to reference fields

</td><td>

To create a query string that refers to a reference field in another table, use this syntax: field\_in\_referenced\_table=value. For example, to return users with the itil role in the **Assigned to** reference field on the Incident form, use:```
Assigned_to.roles=itil
```

</td></tr><tr><td>

Referring to choice list values

</td><td>

To create a query string that refers to a [choice list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_ChoiceLists.md) option, use the value of the choice list, not the label, with this syntax: choice list field=value. For example, to return configuration items \(CIs\) with the status **Installed**, which has a value of 1 in the choice list, use:```
install_status=1
```

 See [Values to associate with choice labels for scripting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/c_DetermValsAssocWChoicesScripting.md) to find the options for the values.

</td></tr><tr><td>

Using multiple conditions

</td><td>

To use two conditions joined by an AND operator, use the carat ^ symbol in this syntax: field1=value1^field2=value2. For example, to return all active users with the "itil" role, use:```
active=true^roles=itil
```

 To use two conditions joined by an OR operator, use the carat symbol with OR with this syntax: field1=value1^ORfield1=value2. For example, to return all users with either the "itil" or "admin" roles, use:

 ```
roles=itil^ORroles=admin
```

 To use condition by the LIKE operator, use the syntax:fieldLIKEsubstring. For example, to return all users with roles containing the string "it", use:

```
rolesLIKEit
```

To use condition by an IN operator, use the syntax: fieldINvalue1,value2,value3. For example, to return all users with roles that are either "itil", "admin", or "user", use:

```
rolesINitil,admin,user
```

To add multiple conditions where one condition is a JavaScript function, use this syntax: javascript:'field=value^' + function\(\). The function must return a string that can be concatenated with the first string to produce a valid query string. For example, to return all active users and meet the conditions of the getGroupQualifier\(\) function, use:

 ```
javascript:'active=true^' + getGroupQualifier()
```

</td></tr><tr><td>

Listing values in order

</td><td>

To sort data by a specific field, use the ORDERBY condition with the following syntax: field1=value^ORDERBYfield2.For example, to return the days of the week in order from the Day of the Week \[sys\_cal\_unit\] table, use:

 ```
unit_name=day^ORDERBYvalue
```

 In the Day of the Week table, unit\_name is the field that specifies day, week, or month, and value is a numerical value for each day from 1 \(Monday\) to 7 \(Sunday\). The query string returns a list of the days of the week in order from the lowest value, which represents Monday, to the largest value, which represents Sunday.

 **Note:** Reference qualifiers do not support the ORDERBY condition. In reference qualifiers, you can sort the reference lookup list by using standard list controls. To specify the order of an auto-complete list for a reference field, use the ref\_ac\_order\_by dictionary attribute.

</td></tr><tr><td>

Including a related list query

</td><td>

At the end of the query statement, enclose the related list information with ^RLQUERY and ^ENDRLQUERY and the quantity. For example, in a query on the Problem table that includes problems with at least one related incident, use:```
^RLQUERYincident.problem_id,>=1^ENDRLQUERY
```

 You can also specify conditions on the related table. For example, to include the condition that at least one of the related incidents is critical priority, use:

 ```
^RLQUERYincident.problem_id,>=1,priority=1^ENDRLQUERY
```

 **Note:** Related list queries must be enabled in **System Properties** **List v3**. Select the **Allow related list query conditions to be added through the filter** check box to enable it.

You can build a related list query for a list that uses List v2, however, the filter conditions cannot be modified until you removed the related list condition in the breadcrumb.

</td></tr><tr><td>

Including a search term query

</td><td>

To include a search term in a query, use the 123TEXTQUERY321 reserved variable. For example, to return results with the 'email' search term, use this encoded query string.

 ```
123TEXTQUERY321=email
```

</td></tr><tr><td>

Including a text index group query

</td><td>

To include a text index group in a query, use the 123TEXTINDEXGROUP321 reserved variable. For example, to return results within the portal\_index\_group text index group in the Text Index Groups \[ts\_index\_group\] table, use this encoded query string.

 ```
123TEXTINDEXGROUP321=portal_index_group
```

</td></tr></tbody>
</table>-   **[Generate an encoded query string through a filter](../task/t_GenEncodQueryStringFilter.md)**  
You can generate an encoded query string through a filter on any list and paste the string into a URL query or a reference qualifier.

**Parent Topic:**[Filters and breadcrumbs](c_UsingFiltersAndBreadcrumbs.md)

