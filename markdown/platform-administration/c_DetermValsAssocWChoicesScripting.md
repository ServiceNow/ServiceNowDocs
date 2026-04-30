---
title: Values to associate with choice labels for scripting
description: When you write a script that references a choice list, you need to know the value that is associated with each choice.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Choice list field type, Field types, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Values to associate with choice labels for scripting

When you write a script that references a choice list, you need to know the value that is associated with each choice.

For example, to check whether the incident\_state field is active, you could not use the condition `current.incident_state == "active"` because the value associated with the choice labeled **Active** is the integer **2**. Instead, you would use the condition `current.incident_state == 2`.

The **Type** field on the choice list dictionary entry determines the data type of the values.

To determine the value associated with a choice, right-click the field label and select **Show Choice List**, and then locate the choice for which you need to know the value.

![](../image/ShownChoices.png "Show choices list values")

The **-- None --** option may not have a sys\_choice record associated with it. A choice list field set to **-- None --** evaluates to these values, depending on the script context as listed below.

-   For client-side scripts,such as client scripts: "" \(empty string\)
-   For server-side scripts, such as business rules: "0" \(string of the number zero\)

**Parent Topic:**[Choice list field type](c_ChoiceLists.md)

**Related topics**  


[System dictionary](../../data-dictionary-tables/concept/c_SystemDictionary.md)

