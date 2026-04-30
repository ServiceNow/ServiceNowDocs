---
title: Import goals and targets data from a spreadsheet
description: With the admin role, you can import your existing goals and targets data from a spreadsheet to the Goal Framework tables.
locale: en-US
release: xanadu
product: Goal Framework
classification: goal-framework
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Import goals and targets data from a spreadsheet

With the admin role, you can import your existing goals and targets data from a spreadsheet to the Goal Framework tables.

## Before you begin

-   On a successful job run, the goals data from your spreadsheet is imported to the Goal \[sn\_gf\_goal\] table.
-   On a successful job run, the targets data from your spreadsheet is imported to the Target \[sn\_gf\_goal\_target\] table.

**Note:** Because the targets are associated to a goal, you should import the goals first and then the targets.

**Important:** Goals and targets data in the spreadsheet must be in the supported format. For details on the supported data format to import goals and targets data from a spreadsheet, see [Import goals and targets data \[KB1191233\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1191233).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  From the Import set table drop-down list, select **Goal Import Set \[imp\_sn\_gf\_goal\]** or **Target Import Set \[imp\_sn\_gf\_goal\_target\]**.

3.  From the **Source of the import** option, select **File**.

4.  In the **File** option, click **Choose** and select your spreadsheet to import the data.

    **Important:**

    -   Goals and targets data in the spreadsheet must be in a specific format. For details on the supported data format, see [Import goals and targets data \[KB1191233\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1191233).
    -   Don't modify the names in the header row of the spreadsheet because the data is imported to the respective fields in the goal and target tables based on the header title of each column.
5.  Click **Submit**.

6.  On the Progress page, click **Run Transform**.

7.  On the Specify Import set and Transform map page, click **Transform**.

8.  Click **Transform history** and verify that the State column is set to **Complete** in the Import Set Runs related list.

    Depending on the option that you selected from the Import set table drop-down list, your goals or targets data is imported to the Goal \[sn\_gf\_goal\] or Target \[sn\_gf\_goal\_target\] tables.

    If the job is failed, click **Transform history** and refer to the details.

    **Note:** The Import operation can be used for inserting new data or updating the existing data in the tables. By default, the Name and Owner values are the primary keys used for updating the existing records. You can also add additional fields as primary key for inserting new data or updating the existing data. For details on how to add additional fields as primary key, see [Import goals and targets data \[KB1191233\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1191233).


**Parent Topic:**[Configuring Goal Framework and Goal Framework for SPM](../concept/configuring-goal-framework.md)

