---
title: Grant access to the update set picker
description: Enable a non-administrative user to use the update set picker.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/system-update-sets/t\_GrantAccessToTheUpdateSetPicker.html
release: xanadu
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Update set administration, System update sets, Deploying applications, Building applications]
---

# Grant access to the update set picker

Enable a non-administrative user to use the update set picker.

## Before you begin

Role required: admin

## About this task

The update set picker appears on the Settings panel. The picker allows users to choose an update set for making and tracking customizations. By default, only administrators can use the update set picker. You can grant access to additional users.

\[Omitted image "u16-update-set-picker.jpeg"\] Alt text: update set picker

## Procedure

1.  Grant the user role read access to the Update Set table \[sys\_update\_set\].

2.  Enable users to see the update set picker on the Settings panel.

    1.  Add a system property **glide.ui.update\_set\_picker.role** to the System Properties table.

    2.  Set the value of **glide.ui.update\_set\_picker.role** to the role for which you want to give access.


