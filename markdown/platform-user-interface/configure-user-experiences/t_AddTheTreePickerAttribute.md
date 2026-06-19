---
title: Add the tree picker attribute
description: A limit of 1000 has been placed on the number of nodes returned to the tree picker. This limit is configurable with the glide.ui.group\_heirarchy.max\_nodes property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/t\_AddTheTreePickerAttribute.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
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

1.  Open the Dictionary attributes for the field.

2.  Add `tree_picker=true` to the **Attributes** field.

    If there are multiple attributes, use a comma to separate them without any spaces between.


**Parent Topic:**[Tree picker](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/c_TreePicker.md)

