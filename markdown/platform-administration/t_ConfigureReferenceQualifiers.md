---
title: Configure reference qualifiers
description: System administrators can configure reference qualifiers that enable filtering of the associated reference field.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Reference qualifiers, Reference field type, Field types reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Configure reference qualifiers

System administrators can configure reference qualifiers that enable filtering of the associated reference field.

## About this task

This task walks you through creating a reference qualifier in the [system dictionary](../../../administer/data-dictionary-tables/concept/c_SystemDictionary.md). When creating a reference qualifier in the system dictionary, it not only applies to that table, but also to all the children of the table.

**Note:** You can also create reference qualifiers on extended tables through [dictionary overrides](../../../administer/data-dictionary-tables/concept/c_DictionaryOverrides.md). Dictionary overrides only impact the extended table and any of its children, not the parent table.

## Procedure

1.  Navigate to the [reference field](../../../administer/field-administration/concept/c_ReferenceField.md) on the form or table on which you want to define a reference qualifier.

2.  Right-click the reference field label and select **Configure Dictionary**.

3.  Under **Related Links**, select **Advanced view**.

    The simple reference qualifier is available in both the default view and the advanced view. The dynamic and advanced reference qualifiers are available only in the advanced view.

4.  In the Reference Specification section, verify that the table in the **Reference** field contains the table that you want associated with the reference field, or select another table if necessary.

5.  From the **Use reference qualifier** choice list, select the reference qualifier to implement.

6.  Configure the qualifier based on the type of reference qualifier.

    -   **Simple**: [Build the condition](https://www.servicenow.com/docs/access?context=c_ConditionBuilder&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) using the choice lists.
    -   **Dynamic**: Either select an existing dynamic filter option or [Create a dynamic filter option](https://www.servicenow.com/docs/access?context=t_DynamicFilterOptions&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).
    -   **Advanced**: In the **Reference qual** field, enter an [Encoded query strings](https://www.servicenow.com/docs/access?context=c_EncodedQueryStrings&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US), JavaScript that returns a query string, or the name of a [script include](t_ExJSConstrainAssignmentGroupField.md) or [business rule](t_ExJavaScriptLimitAssignedToField.md) to run.
7.  Complete the **Reference Specification — Additional Customization** section, as appropriate.

<table id="table_kt2_mhd_yz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Reference key

</td><td>

[Identifies a field other than sys\_ID](../../../administer/field-administration/task/t_DefineTheReferenceKey.md) to use as the unique identifier for the reference field.

</td></tr><tr><td>

Reference cascade rule

</td><td>

[Defines what happens to a record](../../../administer/field-administration/task/t_CascadeDeleteRules.md) if the record it references is deleted. Possible options include:-   None
-   Cascade
-   Clear
-   Delete
-   Delete no workflow
-   Restrict


</td></tr><tr><td>

Reference floats

</td><td>

Flag that determines whether to [Configure the edit option](https://www.servicenow.com/docs/access?context=t_ConfigureTheEditOption&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US) for one-to-many relationships.

</td></tr><tr><td>

Dynamic creation

</td><td>

Flag that determines if the system should [create a new record](../../../administer/field-administration/task/t_EnableDynCreationForRefFields.md) when a value for the reference field does not match an existing record. If you select this option, enter a script that specifies how to create the record in the **Dynamic creation script** field.

</td></tr></tbody>
</table>8.  Click **Update**.


