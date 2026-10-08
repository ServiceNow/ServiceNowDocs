---
title: Create a change model attribute
description: Create a custom change model attribute that you can assign to states in a change model and check in scripts to control behavior for each state.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/change-management/create-change-model-attribute.html
release: brazil
product: Change Management
classification: change-management
topic_type: task
last_updated: "2026-09-30"
reading_time_minutes: 1
keywords: [change model attributes, create attribute, change model]
breadcrumb: [Change model attributes, Create a Change model, Configure, Change Management, IT Service Management]
---

# Create a change model attribute

Create a custom change model attribute that you can assign to states in a change model and check in scripts to control behavior for each state.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Change** &gt; **Models** &gt; **Change Model Attributes**.

    The list shows the existing attributes, including the Allow CI Modification and Allow Implementation attributes from the base system.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Label|Display name of the attribute.|
    |Name|Unique name used by scripts to check for the attribute. Use underscores instead of spaces, for example, `this_is_my_new_attribute`.|
    |Description|Description of the behavior that the attribute controls.|
    |Application|Application scope of the attribute. This field is automatically set to the current application scope.|
    |Table name|Table that the attribute applies to. You can select only the Change Request \[change\_request\] table or a table that extends it. The attribute is available for all extensions of the selected table.|

4.  Select **Submit**.

    The attribute appears in the **Change Model Attributes** list.


## What to do next

Assign the attribute to one or more states in a change model. Until you assign it, the attribute doesn't affect any change request.

**Parent Topic:**[Change model attributes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-service-management/change-management/change-model-attributes.md)

