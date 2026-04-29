---
title: Display a reference field as a choice list
description: You can display a reference field as a choice list instead of opening a lookup window.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Add a reference field, Reference field type, Reference, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Display a reference field as a choice list

You can display a reference field as a choice list instead of opening a lookup window.

## Before you begin

Role required: personalize\_dictionary

## About this task

**Note:** A choice reference field with a defined reference key won't function.

## Procedure

1.  In the form, right-click the label for the reference field and select **Configure Dictionary**.

2.  In the Choice List Specification section, select one of the following options in the **Choice** field.

    -   **Dropdown with --None--**
    -   **Dropdown without --None--**
3.  Right-click the form header and click **Save**.

4.  Under **Related Links**, click **Advanced view**.

5.  In the **Attributes** field, add the following attribute, separated from other attributes by a comma.

    ```
    ref_auto_completer=AJAXReferenceChoice
    ```

6.  Click **Update**.

    The form reopens, with the reference field as a choice list.

    ![Reference choices](../image/Referencechoice.png)

    **Note:**

    The **glide.ui.max\_ref\_dropdown** system property determines whether a reference field is displayed as a choice list or a reference icon. When the number of available choices exceeds the value of this property, a reference icon displays instead of a choice list. The default value of this property is 25. This property affects the entire instance, however you can override this property on an individual field by using the **max\_ref\_dropdown** dictionary attribute. Modifying dictionary attributes requires the personalize\_dictionary role.

    The **glide.xmlhttp.max\_choices** system property determines how many choices display on a choice list. This property has a value of 15 by default, however, when the property is not present on the instance, the instance uses a hard coded value of 10.


**Related topics**  


[System dictionary](../../data-dictionary-tables/concept/c_SystemDictionary.md)

