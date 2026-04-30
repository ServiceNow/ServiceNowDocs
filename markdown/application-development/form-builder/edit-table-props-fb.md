---
title: Edit table properties in Table Builder
description: Change table properties such as the table label or other settings so that you can make a table extensible or add record numbers by using Table Builder.
locale: en-US
release: xanadu
product: Form Builder
classification: form-builder
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Data in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Edit table properties in Table Builder

Change table properties such as the table label or other settings so that you can make a table extensible or add record numbers by using Table Builder.

## Before you begin

Role required: none

**Note:** User must have canWrite access to **sys\_db\_object** or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

## About this task

By editing table properties, you can relabel your table, make your table extensible, or add record numbers. You can also set application access settings.

Making a table extensible means that you are enabling new tables to share columns from your table. For example, if you created an "Office location" column in your table, you can allow new tables to use the "Office location" column also. For more information on table extensions, see [Table extension and classes](https://www.servicenow.com/docs/access?context=table-extension-and-classes&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Adding record numbers means that a tracking number is created automatically for each new table entry. For example, a new entry to the Travel Requests table would get a record number like TRV1234567. You can use this number to find table records more easily.

Application access settings determine whether script objects from other applications can access the table in your application. You can give these script objects access to read, create, update, or delete records on your table. Alternatively, you can disable access to your table from other applications. For more information on the application access controls, see [Table design and runtime settings](../../../build/applications/reference/r_TableApplicationAccessFields.md).

## Procedure

1.  Navigate to the **Data** tab.

2.  Select **Properties**.

3.  In the dialog box that appears, update the table properties as shown in the following example.

    For more information on these properties, see [Table properties](../reference/table-parameters.md#section_ezz_pft_ssb).

    ![Editing table properties.](../image/tb-edit-table-props.png "Editing table properties")

4.  To close the dialog box, select **Save**.

5.  Select **Save**.


**Parent Topic:**[Data in Table Builder](../concept/table-builder.md)

