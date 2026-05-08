---
title: Build the data model
description: Create tables and fields on the tables to support the application’s data model.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Define and build the data model, Build your application, Exploring professional development, Building pro-code applications, Developing your application, Building applications]
---

# Build the data model

Create tables and fields on the tables to support the application’s data model.

**Note:** Consider creating applications with help from agentic AI. For more information, see [Vibe coding and AI app development on the ServiceNow AI Platform](../../ai-capabilities/concept/use-ai-capabilities-in-custom-apps.md).

ServiceNow automatically adds five fields to each new table. The new fields contain auto-populated information about the table.

|Field name|Database name|Description|
|----------|-------------|-----------|
|Created by|sys\_created\_by|User who created the record.|
|Created|sys\_created\_on|Date/time when the record was created.|
|Updated by|sys\_updated\_by|User who last updated the record.|
|Sys ID|sys\_id|Unique identifier for the record. It is unique throughout the instance.|
|Updates|sys\_mod\_count|Numeric field that counts the number of updates to the record since record creation.|

New tables can extend an existing table to inherit fields and functionality from the table being extended. Add to and modify the components of the extended table. The most commonly extended ServiceNow table is the task table. For more information, see [When to create a new table vs. when to extend](https://www.servicenow.com/community/in-other-news/when-to-create-a-new-table-vs-when-to-extend/ba-p/2277550) and Exploring ServiceNow AI Platform® tables.

Add fields to the table to support the data model required by the application. ServiceNow has many different field types with built-in validation. Select the field type that best fits the field’s data.

**Note:** String \(plain text\) fields are the easiest to configure. However, because users can enter anything, string fields can result in bad and inconsistent data that is difficult to use.

In the example, a string field type is used for a user's name. Notice the Caller field is different for each Incident record, but the caller may be the same person. Do not use a string field type for a user's name in tables.

![Do not use a string field for users' names. It increases the chance of errors.](../image/string-field.png)

Instead, use a reference field type that references the User table instead of a String field. Users then need to select a single consistent record in the Caller field.

![Use reference fields for users' names for consistency](../image/reference-field.png)

Reference fields ensure consistent data by normalizing date in another table in ServiceNow. ServiceNow has over 2000 baseline tables available to reference. The [Appendix](https://developer.servicenow.com/dev.do#!/guides/rome/now-platform/pro-dev-guide/pro-dev-guide-page-9) lists some commonly used tables for building an app.

While a reference field can normalize data, other fields can be used for specific types of data. Some common field types are:

|Field type|Descriptions|
|----------|------------|
|Integer|Stores number values and can be used in calculations.|
|Currency|Holds a currency value and will show values in the currency of the logged in user.|
|Phone number|Includes validation and formatting for E164-compliant phone numbers.|
|Reference|Displays a record from another table and helps to normalize data.|
|Choice|Displays a select box with a predefined list of choices. Choice lists should include fewer than ten items.|
|Date|Stores a date value selected with a date picker. Use Date if you do not need a specific time.|
|Date/Time|Stores date and time values selected with a date and time picker. Use Date/Time to compare specific times or if the exact time is important.|
|String|Holds freeform text. Use String if no other field type matches the values stored in the field.|

**Note:** Field types should not be changed after a field is created.

## Choice lists or reference fields

Choice lists and Reference fields both offer users a way to choose a value from a list. Choice lists are name/value pairs. Users select from the names and the field stores the value of the selected choice. Scripts use the value. Add and remove name/value pairs from the choices to manage the list of options.

Reference fields point to a table. Manage choices in the table. The value stored in the reference field is the sys\_id of the referenced record.

Choice lists do not require a reference table and are easier to configure than reference fields. Use Choice lists when the field has ten or fewer options and the options will not change. Consider using a reference field and table when:

-   The field requires more than ten choices.
-   The choices will regularly change.
-   Someone other than an administrator needs to manage the choices.
-   The value of the field has an impact on decision logic. For example, decision tables in Flow Designer.
-   The data has multi-level dependencies between different fields that can lead to complex and unwieldy choice field combinations.
-   The choices require more than a name/value pair. For example, referencing a user record gives the referencing table access to other user details, such as email and department.
-   A table already exists that includes the data needed for the field.

When using reference fields, review the tables available in the instance to reference before creating a table. If creating a new table, check the list of exempt tables in section 2 of the [Custom Table Guide](https://www.servicenow.com/content/dam/servicenow-assets/public/en-us/doc-type/legal/custom-table-guide.pdf). If appropriate, extend the new table from one of these.

**Note:** Before creating new fields on an extended table, check for an existing field inherited from the base table that has a similar purpose. If a field is found, override the extended table's label.

**Parent Topic:**[Define and build the data model](define-and-build-data-model.md)

