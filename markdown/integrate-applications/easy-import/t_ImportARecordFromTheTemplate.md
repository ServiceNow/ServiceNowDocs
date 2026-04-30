---
title: Import a record from the template
description: After updating the import template with new data, import the template to your instance.
locale: en-US
release: xanadu
product: Easy Import
classification: easy-import
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Easy import, Imports, Creating integrations with applications]
---

# Import a record from the template

After updating the import template with new data, import the template to your instance.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to the same list you used to download the import template.

2.  Perform the appropriate action for the list version.

    |Action|Version|
    |------|-------|
    |**List v2**|Right-click the column heading and select **Import**|
    |**List v3**|Open the list title menu and select **Import**.|

    ![Import template insert or update records](../image/ImportTemplateInsertOrUpdateRecords.png)

3.  From Insert or update, select the import type.

4.  From File, select the import template to import.

5.  Click **Upload and Preview Import Data**.

    ServiceNow validates the template.

    If the template passes validation and the imported preview matches your expectations, click **Complete Import** to import records into the current table. If the template fails validation, review the errors. Click **Ignore Errors and Complete Import** to continue the import by skipping any bad data cells.


**Parent Topic:**[Easy import](../concept/c_EasyImport.md)

