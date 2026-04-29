---
title: Assigning data classifications to dictionary entries
description: Assign data classifications to specific table columns in the Dictionary \[sys\_dictionary\] table. When you assign data classifications, it creates entries in the Dictionary-Data Class \[m2m\_dictionary\_dataclass\] table, which you can then review in the Overview dashboard.
locale: en-US
release: australia
product: Data Classification
classification: data-classification
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Data Classification, Platform Privacy]
---

# Assigning data classifications to dictionary entries

Assign data classifications to specific table columns in the Dictionary \[sys\_dictionary\] table. When you assign data classifications, it creates entries in the Dictionary-Data Class \[m2m\_dictionary\_dataclass\] table, which you can then review in the Overview dashboard.

## Before you begin

Role required: data\_classification\_admin and admin

## Procedure

1.  In the Navigator pane, type `sys_dictionary.list`.

2.  In Dictionary Entries, select each of the elements you want to assign specific data classifications to.

3.  After selecting the elements, click **Actions on selected rows**, and then select **Classify**.

    **Note:** To clear previously assigned data classifications for selected dictionary elements, you can select **Clear classification**.

4.  When the Assign to data class dialog appears, select the data classifications you want to assign to your selected dictionary elements, then click **Classify**.

    **Warning:** This will overwrite any existing classifications for the selected dictionary items.

    You can select multiple data classifications as needed.

    See [Data dictionary tables](https://www.servicenow.com/docs/access?context=c_DataDictionaryTables&version=australia&pubname=australia-platform-administration&ft:locale=en-US) for additional information.


