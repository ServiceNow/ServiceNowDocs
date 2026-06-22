---
title: Grant access to the update set picker
description: Enable a non-administrative user to use the update set picker.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/system-update-sets/t\_GrantAccessToTheUpdateSetPicker.html
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

\[Omitted image "u16-update-set-picker.jpeg"\] Alt text: update set picker

## Procedure

1.  [Grant the user role read access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-security/access-control/t_CreateAnACLRule.md) to the Update Set table \[sys\_update\_set\].

2.  Enable users to see the update set picker on the Settings panel.

    1.  [Add a system property](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/ai-platform-administration/t_AddAPropertyUsingSysPropsList.md) **glide.ui.update\_set\_picker.role** to the System Properties table.

    2.  Set the value of **glide.ui.update\_set\_picker.role** to the role for which you want to give access.


**Parent Topic:**[Administer system update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/system-update-sets/administer-system-update-sets.md)

