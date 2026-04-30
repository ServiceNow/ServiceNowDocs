---
title: Load data from Watershed into ESG Management
description: Load data from the Watershed spreadsheets into the staging table. After you load the data and complete the setup, you can start using the Watershed Integration for ESG.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Integrating ESG Management with Watershed, Integrating ESG Management with other applications, Environmental, Social, and Governance Management]
---

# Load data from Watershed into ESG Management

Load data from the Watershed spreadsheets into the staging table. After you load the data and complete the setup, you can start using the Watershed Integration for ESG.

## Before you begin

You must add the import\_admin role to the sn\_grc\_metric.admin role.

Role required: sn\_esg.program\_manager

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **Load Data**.

2.  On the Load Data form, select **Existing table**.

3.  In the Import set field, select **Watershed Data \[sn\_esg\_watershed\_data\]**.

4.  Select **Choose File**, and select the file that you want to load.

5.  Select **Open**.

6.  In the **Sheet number** field, verify that the sheet number is appropriate.

7.  In the **Header row** field, verify that the header row is appropriate.

8.  Select **Submit**.


## Result

The spreadsheet is loaded in the staging table. All the columns from the spreadsheet are created.

## What to do next

[View the import set](view-and-verify-the-import-sets.md).

**Parent Topic:**[Integrating ESG Management with Watershed](../concept/integrate-esg-with-watershed.md)

