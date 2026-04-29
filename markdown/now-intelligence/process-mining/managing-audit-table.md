---
title: Managing an audit table
description: After the audit and record tables are created with the imported data, you can use them to create a project. You can also share, edit, empty, or delete the tables.Share the audit and record tables with the analyst to analyze the data. The audit and record tables are available only to the administrator. However, the administrator might want an analyst to look at the tables and create projects.Edit a dataset if you want to change the dataset, such as add or delete data from the current dataset.Empty a dataset when you want to remove the old data and import new data from the same external system to the same table.Delete a dataset when the dataset is no longer needed. Your analysis is complete, and you want to delete the entire tables.
locale: en-US
release: australia
product: Process Mining
classification: process-mining
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Working with external datasets, Use, Process Mining, Platform Analytics]
---

# Managing an audit table

After the audit and record tables are created with the imported data, you can use them to create a project. You can also share, edit, empty, or delete the tables.

**Parent Topic:**[Working with external datasets](external-dataset.md)

## Share the audit and record tables

Share the audit and record tables with the analyst to analyze the data. The audit and record tables are available only to the administrator. However, the administrator might want an analyst to look at the tables and create projects.

### Before you begin

Role required: sn\_process\_mining\_admin

### Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the External data integration icon \(![External data integration icon](../image/ext-dataset-modules.png)\).

3.  Select a dataset that you want to share.

    The dataset opens in a new tab.

4.  Select **Share**.

    ![Share dataset](../image/ext-data-edit.png)

    The **External dataset permissions** tab is displayed.

5.  Select **New**.

    The **Create New Permission** page is displayed.

6.  Select a user, role, or group, and select **Save**.

    ![Permissions for sharing tables](../image/ext-dataset-share.png)

    Every user with the specified permission can access the audit and record tables.


## Edit a dataset

Edit a dataset if you want to change the dataset, such as add or delete data from the current dataset.

### Before you begin

Role required: sn\_process\_mining\_admin

### Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the External data integration icon \(![External data integration icon](../image/ext-dataset-modules.png)\).

3.  Select a dataset that you want to edit.

    The dataset opens in a new tab.

4.  Select **Edit dataset** from the dataset tab.

    ![Edit dataset](../image/ext-data-edit.png)

    You are taken back to the **Import data** tab. You can import the new data that you want to populate in the table. For steps to import data, see [Import data into the audit table](../task/import-data.md).


## Empty a dataset

Empty a dataset when you want to remove the old data and import new data from the same external system to the same table.

### Before you begin

Role required: sn\_process\_mining\_admin

### Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the External data integration icon \(![External data integration icon](../image/ext-dataset-modules.png)\).

3.  Select a dataset that you want to empty.

    The dataset opens in a new tab.

4.  Select **Empty dataset** from the dataset tab.

    ![Empty dataset](../image/ext-data-man.png)

    A dialog box appears requesting you to confirm that you want to empty the selected dataset.

5.  Type “Empty” in the confirmation area, and select **Empty dataset**.

    The content from the audit and record tables are removed. After you’ve emptied the dataset, you can import any dataset again. For steps to import data, see [Import data into the audit table](../task/import-data.md).


## Delete a dataset

Delete a dataset when the dataset is no longer needed. Your analysis is complete, and you want to delete the entire tables.

### Before you begin

Role required: sn\_process\_mining\_admin

### Procedure

1.  Navigate to **Workspaces** &gt; **Process Mining Workspace**.

2.  On the left of the page, select the External data integration icon \(![External data integration icon](../image/ext-dataset-modules.png)\).

3.  Select a dataset that you want to delete.

    The dataset opens in a new tab.

4.  Select **Delete dataset** from the dataset tab.

    ![Delete dataset](../image/ext-data-man.png)

    A dialog box appears requesting you to confirm that you want to delete the selected dataset.

5.  Type “Delete” in the confirmation area, and select **Delete dataset**.

    The data from the audit and record tables, and the associated Process Mining projects are removed.

    **Note:** The tables aren’t deleted. Only data is deleted. If you want to delete the tables, the administrator must delete them manually. The administrator must delete the tables periodically.


