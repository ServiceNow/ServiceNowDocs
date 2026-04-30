---
title: Add a custom field mapping in the staging table for Service Graph Connector for Microsoft Excel
description: With the Service Graph Connector for Microsoft Excel, add a custom field to the staging table and map the custom field to the configuration item \(CI\) field.
locale: en-US
release: yokohama
product: Operational Technology Manager
classification: operational-technology-manager
topic_type: task
last_updated: "2025-07-17"
reading_time_minutes: 4
breadcrumb: [Configuring the Service Graph Connector for Microsoft Excel, Service Graph Connector for Microsoft Excel, Use, Operational Technology Manager, Operational Technology]
---

# Add a custom field mapping in the staging table for Service Graph Connector for Microsoft Excel

With the Service Graph Connector for Microsoft Excel, add a custom field to the staging table and map the custom field to the configuration item \(CI\) field.

## Before you begin

To configure the form layout, see [Configure the form layout](https://www.servicenow.com/docs/access?context=configure-form-layout&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

To create a custom field on the staging table, see [Add and customize a field in a table](https://www.servicenow.com/docs/access?context=t_CreatingNewFields&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Roles required:

-   admin - Can change the script include. Can add class or field mappings and change the ETL.
-   cmdb\_inst\_admin - Can only add new class or field mappings and change the ETL.

## Procedure

1.  Add custom columns to the Staging \[sg\_ot\_excel\_staging\] table.

2.  Navigate to **All** and in the **Filter** field, add `sg_ot_excel_staging.list`.

3.  On your keyboard, press enter.

4.  If needed, manually create records by selecting **New**.

5.  Navigate to **All** &gt; **Industrial Workspace Admin** &gt; **OT Manager** &gt; **Import OT Devices - Script Includes** and select the `SGOTAssetImportExcelConstants` script include.

6.  In the script, update the new column name from the staging table, and the new ETL column name inside the `SGOTAssetImportExcelConstants.importSetColumnsVsStagingColumnsMap` object in the format “&lt;ETL Column Name&gt;”: “&lt;Column Name from staging table&gt;”.

    In this example, the “u\_my\_custom\_field” before the colon \( : \) indicates the ETL column name \(shown as a column in the ETL preview step\), and the “u\_my\_custom\_field” after the colon indicates the column name in the staging table.

    Make sure that there’s a comma \(,\) added at the end of the line above the new line. In this example, a comma is added after the "custom\_fields": "custom\_fields" line.

    ![Updated ETL column name with SGOTAssetImportExcelConstants.](../image/custom-field-new.png)

7.  Select **Update** to save your changes.

8.  Navigate to **All** &gt; **Configuration** &gt; **IntegrationHub ETL**.

9.  Select the **CMDB Application: SG-OT Excel Import** ETL.

10. If the Invalid Mapping Data-Detected page is displayed, select **Close**.

11. From the ETL Transform Map Assistant, in the Specify Basic Details section of the guided setup, select **Import Source Data and Provide Basic Details**.

    ![Select step 1: Provide basic information for the ETL Transform Map.](../image/step-1-provide-basic-info-etl-transform.png)

12. In the **Sample Import Set** field, select **Auto-pull a new import set**.

    ![Sample Import Set field, select Auto-pull a new import set.](../image/sample-import-set-auto-pull-new-set.png)

13. Select **Save**.

    The basic information saved successfully banner is displayed.

14. Select **Mark as Complete**.

15. From the ETL Transform Map Assistant page, in the Prepare Source Data for Mapping section, select **Preview and prepare data**.

    ![Preview and prepare data.](../image/prepare-source-data.png)

    If the column isn’t visible, repeat the steps 11 through 14.

16. Select **Mark as Complete**.

17. From the ETL Transform Map Assistant page, in the Map Data to CMDB and Add Relationships section, select **CMDB Classes to Map Source Data**.

18. Map the column to the target class and attribute.

    For example, the **Comments** field is present on the Hardware \[cmdb\_ci\_hardware\] class. After the field is mapped, the **Comments** field on Hardware child classes is updated if the value for the Comments column in the staging table for that row isn’t empty.

    If you're adding a mapping for a new field that isn't present, or for a field that isn't specific to the Hardware cmdb\_ci\_hardware class and instead is a field in the Operational Technology \(cmdb\_ci\_ot\) class, you can add the field mapping in the Operational Technology \(OT\) 1 stub.

    1.  Add a field mapping to the Hardware 1 class.

    2.  For the Hardware 1 class, select **Edit Mapping**.

        ![Select CMDB Classes to Map Source Data](../image/select-cmdb-clasess-map-source-data.png)

19. In the Add Attribute dialog box that appears, from the **Attribute** list, select **Comments**.

    ![Map Hardware 1 class - Add Attribute dialog box.](../image/map-hardware-add-attribute-dialog.png)

20. Select **Save**.

    A new field named “Comments” is displayed.

    ![New comments field added.](../image/map-hardware-1-new-comments-field.png)

21. From the Data pane, drag the data pill to the Comments **Source Column** field.

    ![Map to hardware.](../image/map-cmdb.png)

    You can also select the source column icon \( ![Source column icon.](../image/source-column-icon.png) \) to select the data-mapping field for it.

    The Source Column includes the data pill.

    ![Source Column field filled with a data pill.](../image/map-cmdb-1.png)

22. Navigate back to the **CMDB Classes to Map Source Data** of the Map Data to CMDB and Add Relationships section in the ETL Transform Map Assistant page.

    ![Navigate back to the CMDB Classes to Map Source Data page.](../image/map-hardware-navigate-back-cmdb-classes.png)

23. Select **Mark as Complete**.

24. Follow these steps to verify the new field mappings.

    1.  Navigate to the home page of the ETL Transform Map Assistant.

    2.  In the Preview Sample Integration Results and Schedule Import section of the guided setup, select **Test and Rollback Integration Results**.

        ![ETL Transform Map Assistant - Test and Rollback Integration Results.](../image/etl-test-rollback.png)

    3.  Select **Run Integration**.

    4.  After the run finishes successfully, confirm that the Comments field of the CI that you provided a comments value for is updated in the staging table.

    5.  Select **Mark as Complete**.

        ![After the Test and Rollback Integration Results successfully runs, confirm that the Excel sheet is updated.](../image/test-rollback-integration.png)

    6.  Select **Perform Rollback**.

        ![Select Perform Rollback.](../image/rollback-options-plc.png)

    7.  If the ETL isn’t activated, select **Activate**.

    The new column field mapping is successfully added and verified.


**Parent Topic:**[Configuring the Service Graph Connector for Microsoft Excel](../concept/configuring-service-graph-connector-for-excel.md)

