---
title: Disable live form features
description: User presence includes several new live form features for Core UI. You can show or hide these features using the glide.ui16.live\_forms.enabled property.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/configure-user-experiences/configure-live-form-feat.html
release: zurich
product: Configure User Experiences
classification: configure-user-experiences
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [User presence, Common UI elements, Working in Core UI, Configure UIs and portals, Configure user experiences]
---

# Disable live form features

User presence includes several new live form features for Core UI. You can show or hide these features using the **glide.ui16.live\_forms.enabled** property.

## Before you begin

Role required: admin

## About this task

The **glide.ui16.live\_forms.enabled** property is included automatically with Core UI \(UI16\) as part of the **com.glide.ui.form\_presence** plugin. It controls the following form features:

-   Live form updates
-   Form presence
-   Activity formatter appearance
-   Attachments displaying in the activity stream

## Procedure

1.  Enter `sys_properties.list` in the Navigation filter.

2.  In the system properties list, search for the **glide.ui16.live\_forms.enabled** property.

3.  In the Value field, type `false`.


**Parent Topic:**[User presence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/c_UserPresence.md)

