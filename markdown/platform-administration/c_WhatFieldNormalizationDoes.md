---
title: Normal values
description: A normal value replaces similar but ambiguous field values with one standard value.
locale: en-US
release: australia
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Field normalization and transformation, Administer, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Normal values

A normal value replaces similar but ambiguous field values with one standard value.

## Field value variations

Records values can come from multiple sources such as:

-   Automated entries made by Discovery.
-   Automated entries made by importing records from external systems or files.
-   Manual entries made by users.

Each of these sources may describe the same field value in several different forms. For example, the **CPU Type** field on a computer CI form might display any of the following similar values:

-   **E3350 \(Intel\) 4.5.2234**
-   **Intel Xeon 5.4.554**
-   **Xeon L3350**
-   **L3350**

Without normalization, these variant field values results in:

-   Duplicate CPU types
-   Poor search results
-   Complex queries and conditions to apply business logic

Creating a normal value record solves these issues by consolidating on one standard value such as `Xeon`.

## Identifying variations with aliases and rules

Each Normal value record specifies how to identify variations of a normal value using a combination of aliases and rules.

-   **Aliases**

    Aliases are known variations of an input value that normalization converts to the normal value. Use aliases when there is a short list of variant values.

    For example, you could create a normal value `Xeon` that has these aliases.

    -   **E3350 \(Intel\) 4.5.2234**
    -   **Intel Xeon 5.4.554**
    -   **Xeon L3350**
    -   **L3350**
    Whenever a normalization data job or normalized query sees a field value matching an alias, it automatically replaces the field value with the normal value. Normalization data jobs and queries process aliases before rules.

    **Note:** Aliases are logically equivalent to rules using the **\[is\]** operator in a condition where **\[Field name\]\[is\]\[Alias value\]**. For example, the sample aliases are equivalent to these rules: **\[CPU Type\]\[is\]\[E3350 \(Intel\) 4.5.2234\] OR \[CPU Type\]\[is\]\[Intel Xeon 5.4.554\] OR \[CPU Type\]\[is\]\[Xeon L3350\] OR \[CPU Type\]\[is\]\[L3350\]**

-   **Rules**

    Rules specify the conditions under which normalization replaces an input value with the normal value. Use rules when there are a large number of possible variant values, or when you must create complex conditions.

    For example, the normal value `Xeon` could have this rule.

    **\[CPU Type\]\[matches regex\]\[.\*\\bxeon\\b.\*\]**

    Whenever a normalization data job or normalized query sees a field value matching a rule, it automatically replaces the field value with the normal value. Normalization data jobs and queries process rules after aliases.

    Rules and aliases can be combined to normalize a field. Make sure to test your normalization methods before applying them to all the existing records in the database.


## Normalized queries

An administrator can configure normalization to apply to queries issued against normalized fields in lists. Select the **Normalize query** check box on the Normalization form to enable this functionality. In a list containing normalized values, [Filters and breadcrumbs](https://www.servicenow.com/docs/access?context=c_UsingFiltersAndBreadcrumbs&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US) using the original \(raw\) value for the normalized field in the query condition.

The filtered list returns records with the normal value substituted for the raw value. However, the breadcrumbs for the filter display the original query conditions.

## Scripting and normalization

Scripts that update or insert records into the database \(GlideRecord\) are normalized automatically when field normalization is applied. For example, if a script to insert a CI record contains a CPU type of **Xeon L3350**, the script is normalized to insert the CI with a CPU type of **Xeon** instead. Scripts that query the database for normalized field values \(using the conditions of equals or not equals\) can be configured to return the normal value \(such as **Xeon**\) rather than the original \(raw\) value.

**Related topics**  


[GlideRecord](https://www.servicenow.com/docs/access?context=p_GlideServerAPIs&version=australia&pubname=australia-api-reference&section=c_GlideRecord&ft:locale=en-US)

