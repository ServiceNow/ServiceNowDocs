---
title: Delete a table in Table Builder
description: Delete a table from your application so that it no longer appears in the app dashboard.
locale: en-US
release: yokohama
product: Form Builder
classification: form-builder
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Data in Table Builder, Using Table Builder, Table Builder, Builder library, Developing your application, Building applications]
---

# Delete a table in Table Builder

Delete a table from your application so that it no longer appears in the app dashboard.

## Before you begin

**Note:** Parent tables can't be deleted until all existing child tables are deleted.

Role required: Users must have canDelete access to **sys\_db\_object** or AES user role and delegated developer permissions. For more information, see [Delegate developers using AES](../../../build/app-engine-studio/concept/aes-app-dev-workflow.md).

## Procedure

1.  Navigate to the **Data** tab.

2.  Select the menu icon \(![Menu icon.](../../../build/app-engine-studio/image/menu-icon.png)\), and then select **Delete Table**.

3.  In the dialog box, enter `delete` and then select **Delete**.

4.  Select **Save**.


## Result

The table is no longer available in the app dashboard.

**Parent Topic:**[Data in Table Builder](../concept/table-builder.md)

