---
title: Grant access to the update set picker
description: Enable a non-administrative user to use the update set picker.
locale: en-US
release: zurich
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Administer system update sets, System update sets, Deploying applications, Building applications]
---

# Grant access to the update set picker

Enable a non-administrative user to use the update set picker.

## Before you begin

Role required: admin

## About this task

The update set picker appears on the Settings panel. The picker allows users to choose an update set for making and tracking customizations. By default, only administrators can use the update set picker. You can grant access to additional users.

![update set picker](../image/u16-update-set-picker.jpeg)

## Procedure

1.  [Grant the user role read access](https://www.servicenow.com/docs/access?context=t_CreateAnACLRule&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) to the Update Set table \[sys\_update\_set\].

2.  Enable users to see the update set picker on the Settings panel.

    1.  [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=zurich&pubname=zurich-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US) **glide.ui.update\_set\_picker.role** to the System Properties table.

    2.  Set the value of **glide.ui.update\_set\_picker.role** to the role for which you want to give access.


**Parent Topic:**[Administer system update sets](../concept/administer-system-update-sets.md)

