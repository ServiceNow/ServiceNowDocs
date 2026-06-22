---
title: Edit table properties in Table Builder
description: Change table properties such as the table label or other settings so that you can make a table extensible or add record numbers by using Table Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/form-builder-glide-family-release/edit-table-props-fb.html
release: zurich
product: Form Builder \(Glide Family Release\)
classification: form-builder-glide-family-release
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Data in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Edit table properties in Table Builder

Change table properties such as the table label or other settings so that you can make a table extensible or add record numbers by using Table Builder.

## Before you begin

Role required: none

**Note:** User must have canWrite access to **sys\_db\_object** or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/app-engine-studio/aes-app-dev-workflow.md).

## About this task

By editing table properties, you can relabel your table, make your table extensible, or add record numbers. You can also set application access settings.

Making a table extensible means that you are enabling new tables to share columns from your table. For example, if you created an "Office location" column in your table, you can allow new tables to use the "Office location" column also. For more information on table extensions, see [Table extension and classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-administration/table-administration-and-data-management/table-extension-and-classes.md).

Adding record numbers means that a tracking number is created automatically for each new table entry. For example, a new entry to the Travel Requests table would get a record number like TRV1234567. You can use this number to find table records more easily.

Application access settings determine whether script objects from other applications can access the table in your application. You can give these script objects access to read, create, update, or delete records on your table. Alternatively, you can disable access to your table from other applications. For more information on the application access controls, see [Table design and runtime settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/building-applications/r_TableApplicationAccessFields.md).

## Procedure

1.  In the header, navigate to the more options button \[Omitted image "cs-more-actions-icon.png"\].

2.  Select **Properties**.

3.  In the dialog box that appears, update the table properties as shown in the following example.

    For more information on these properties, see [Table properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/table-parameters.md).

    \[Omitted image "tb-edit-table-props.png"\] Alt text: Editing table properties.

4.  To close the dialog box, select **Save**.

5.  Select **Save**.


**Parent Topic:**[Data in Table Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/form-builder-glide-family-release/table-builder.md)

