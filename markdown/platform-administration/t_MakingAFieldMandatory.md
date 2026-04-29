---
title: Make a field mandatory
description: Fields can be marked as mandatory, meaning they must contain a value before the record can be saved. Mandatory fields are marked with a field status indicator before the label.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customize, Field administration, Forms, fields, and lists, Configure core features, Administer the ServiceNow AI Platform]
---

# Make a field mandatory

Fields can be marked as mandatory, meaning they must contain a value before the record can be saved. Mandatory fields are marked with a field status indicator before the label.

## Before you begin

Role required: personalize\_dictionary

## About this task

A mandatory field that is pre-populated by the platform with default data, such as a value from a client script, does not display the indicator. If you delete this value from the field, however, the indicator appears. The color of the indicator depends on the field state.

Using a dictionary entry to make a field mandatory does not work when using WebServices. You can use a data policy instead. For more information on data policies, see [Data policy](../concept/c_DataPolicy.md).

## Procedure

1.  Right-click the field's label in the form and select **Configure Dictionary**.

2.  In the **Dictionary** form, select the **Mandatory** check box.

3.  Click **Update**.

    The next time the form is opened, a field status indicator appears next to the field label, indicating that a value is mandatory. If the mandatory field is pre-populated for any reason, the mandatory field indicator does not appear.

    Mandatory fields are global. The field is marked as mandatory everywhere it appears in a form.

    Making a **True/False** mandatory will have no effect. **True/False** fields are always considered to have a value. A selected check box has a value of true and an unselected check box has a value of false. Either of these values satisfies the requirement of a mandatory field.

    A form can be saved with an empty mandatory field if that field is a reference field, and if the parent field is also blank. However, if the mandatory reference field shows a value from the parent field, then the form cannot be saved if this value is deleted. If the value in the referenced field is changed, the value for that field is changed everywhere it appears.

4.  Use **dictionary override&gt;override mandatory** to make a field that is mandatory only in the child table and not the parent table.


**Parent Topic:**[Customizing fields on the ServiceNow AI Platform](../concept/customize-fields-now-platform-landing.md)

**Related topics**  


[Set a CI field to be mandatory](https://www.servicenow.com/docs/access?context=t_SetCIFieldMandatory&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Define a dictionary override](../../data-dictionary-tables/task/t_DefineADictionaryOverride.md)

