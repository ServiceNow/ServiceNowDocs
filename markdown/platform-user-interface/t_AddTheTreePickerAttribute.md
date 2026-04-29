---
title: Add the tree picker attribute
description: A limit of 1000 has been placed on the number of nodes returned to the tree picker. This limit is configurable with the glide.ui.group\_heirarchy.max\_nodes property.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Tree picker, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Add the tree picker attribute

A limit of 1000 has been placed on the number of nodes returned to the tree picker. This limit is configurable with the **glide.ui.group\_heirarchy.max\_nodes** property.

## Before you begin

Role required: personalize\_dictionary

## About this task

**Note:** The tree display hierarchy does not appear in reference fields when using mobile applications.

## Procedure

1.  Open the [Dictionary attributes](https://www.servicenow.com/docs/access?context=c_DictionaryAttributes&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for the field.

2.  Add `tree_picker=true` to the **Attributes** field.

    If there are multiple attributes, use a comma to separate them without any spaces between.

    ![Tree picker attribute](../image/TreePickerAttribute.png)


**Parent Topic:**[Tree picker](../concept/c_TreePicker.md)

