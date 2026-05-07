---
title: Table-based picklists
description: A table-based picklist lets an administrator query and retrieve data from managed tables.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure picklist extensions, CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Table-based picklists

A table-based picklist lets an administrator query and retrieve data from managed tables.

Table-based picklists allow administrators to retrieve configuration picklist field options from a managed table. This feature is particularly useful when:

-   The number of options in the picklist is large. The buyside UI representation of the table- based picklist paginates options, and thus, improves the userʼs experience of page response.
-   Several picklists make use of the same options. Picklist-specific query filters facilitate data reuse.

Managed Tables are not deployed. As a result, a picklist which references table data for its options will present the end-user with the data available in the table when it is queried, at runtime.

If the referenced managed table contains duplicate data, the application attempts to present the best picklist experience to the user at runtime. For example, consider the following three scenarios.

Scenario 1:

|Label|Value|
|-----|-----|
|Apple|apple|
|Banana|banana|
|Banana|banana|
|Chayote|chayote|

CPQ removes the second instance of Banana \[banana\], presenting the user with three picklist options.

Scenario 2:

|Label|Value|
|-----|-----|
|Apple|apple|
|Banana|banana|
|Banana|banana2|
|Chayote|chayote|

In this scenario, CPQ retrieves picklist options with four unique values. Unfortunately, two values, “banana” and “banana2” share the same label, “Banana”. The app cannot determine which value is best for label, “Banana”. Therefore, the user will be presented with a total of four options, two labeled “Banana”. Administrators must mind their managed tables data to avoid this poor end-user experience.

Scenario 3:

|Label|Value|
|-----|-----|
|Apple|apple|
|Banana|banana|
|Banana2|banana|
|Chayote|chayote|

When duplicate values are returned from a managed table, CPQ displays the label associated with the first occurrence of the value. All other labels associated with that value are eliminated and are not displayed as picklist options to the end-user.

If the referenced table returns a row with no data contained in the label or value, the application will ignore the entry, and the record will not be presented to the end-user as a picklist option.

**Note:** Table-based picklists do not support picklist extensions.

**Related topics**  


[Picklists and picklist extensions in rules](cpq-picklists-and-picklist-extensions-in-rules.md)

