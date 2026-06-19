---
title: Grant access to the update set picker
description: Enable specific roles to access the update set picker.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/system-update-sets/t\_GrantAccessToTheUpdateSetPicker.html
release: australia
product: System Update Sets
classification: system-update-sets
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, System update sets, Deploying applications, Building applications]
---

# Grant access to the update set picker

Enable specific roles to access the update set picker.

## Before you begin

Role required: admin

## About this task

The update set picker appears when selecting the globe icon. The picker enables you to choose an update set for making and tracking customizations. By default, only administrators can use the update set picker. You can grant access to additional users.

\[Omitted image "UpdateSetList.png"\] Alt text: update set picker list.

## Procedure

1.  Grant the user role read access to the sys\_update\_set table.

    For more information, see Grant the user role read access.

2.  Enable access to the update set picker when selecting the globe icon.

    1.  Add glide.ui.update\_set\_picker.role to the System Properties table.

    2.  Set the value of glide.ui.update\_set\_picker.role to the role that you want to grant access to.

    See Add a system property and [Update sets properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/update-sets-properties.md) for more information.


**Parent Topic:**[Configuring System Update Sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/system-update-sets/configure-system-update-sets.md)

