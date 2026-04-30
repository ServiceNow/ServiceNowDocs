---
title: Set up Federal plugin
description: Set up the Federal plugin.You can activate the Additional tables for Federal Agencies plugin \[com.snc.fedtables\] if you have the admin role. Some data elements included in the Federal plugin allow for an import of the reference data.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Federal plugin, HR Service Delivery, Employee Service Management]
---

# Set up Federal plugin

Set up the Federal plugin.

## Activate Federal plugin

You can activate the Additional tables for Federal Agencies plugin \[com.snc.fedtables\] if you have the admin role.

### Before you begin

Role required: admin

### About this task

Tables are installed with the plugin. For more information, see [Federal plugin](../concept/fed-view.md).

### Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Find the Additional tables for Federal Agencies plugin \[com.snc.fedtables\] using the filter criteria and search bar.

    You can search for the plugin by its name or ID. If you cannot find a plugin, you might have to request it from ServiceNow personnel.

3.  Select **Install** to start the installation process.

    **Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the **global** domain. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

    You will see a message after installation is completed. For information about the components installed with a plugin, see [Find components installed with an application](https://www.servicenow.com/docs/bundle/yokohama-platform-administration/page/administer/plugins/task/find-components.html).


## Import an excel template for Federal plugin

Some data elements included in the Federal plugin allow for an import of the reference data.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  In the **Name** column, filter the tables by **sn\_fedtables**.

3.  Select the Federal table in which you want to import the data.

4.  Open **Show List** in **Related links**.

5.  Right-click on the column heading for the data element you want to add reference data to.

6.  Select **Import** from the menu.

    ![Import an excel template for Federal](../image/import-excel-fed.png)

7.  Select **Insert** or **Update** as the import type.

8.  Select **Choose file** to select the Microsoft Excel spreadsheet.

9.  Select **Upload** to upload the Microsoft Excel spreadsheet.

10. In the Upload Progress page, select **Preview Imported Data** to verify the imported data.

11. If the template passes validation and the imported preview matches your expectations, select **Complete Import** to import data into the staging table.

    **Note:** If the template fails validation, verify records in the template and repeat the process again.


