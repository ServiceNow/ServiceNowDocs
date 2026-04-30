---
title: Importing date/time values
description: Considerations when importing data containing date/time values.
locale: en-US
release: xanadu
product: System Import Sets
classification: system-import-sets
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Importing data using import sets, Import sets, Imports, Creating integrations with applications]
---

# Importing date/time values

Considerations when importing data containing date/time values.

-   The field containing the date/time value should be a Date/Time type field in the target table.
-   The user performing the import should have their timezone \(in the **Time zone** \[time\_zone\] field in the User \[sys\_user\] record for that user\) set to match the timezone of the date/time values in the import file.

    To set the user timezone, do the following.

    1.  Click the user drop-down in the banner and select **Profile**.
    2.  Change the **Time zone** field value to the timezone of the date/time values in the import file and click **Update**.

**Parent Topic:**[Importing data using import sets](c_ImportDataUsingImportSets.md)

