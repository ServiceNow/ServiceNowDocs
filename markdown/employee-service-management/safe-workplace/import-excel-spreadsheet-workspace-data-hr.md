---
title: Import your workspaces data from an Excel spreadsheet
description: Import your workspaces data from an Excel spreadsheet into the Workplace Core application.
locale: en-US
release: australia
product: Safe Workplace
classification: safe-workplace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Providing your workplace data, Workplace Core, Safe Workplace, Health and Safety, Employee Service Management]
---

# Import your workspaces data from an Excel spreadsheet

Import your workspaces data from an Excel spreadsheet into the Workplace Core application.

## Before you begin

Complete [Configuring spreadsheets to import workplace data](../concept/importing-workspace-data.md#).

Role required: sn\_wsd\_core.admin

## Procedure

1.  Navigate to **All** &gt; **System Import Sets** &gt; **Load Data**.

2.  Select **Existing table**.

3.  In the **Import set table** field, select **Space Staging \[sn\_wsd\_core\_space\_staging\]**.

4.  In the **Source of the import** field, select **File**.

5.  Select **Choose File** and select the source Excel spreadsheet.

6.  Specify the worksheet number in the **Sheet number** field and header row number in the **Header row** field.

7.  Select **Submit**.

    The imported data is now available in the new Import Set table.

8.  Select **Run Transform**.

    **Important:** Ensure that the Import set field shows sn\_wsd\_core\_space\_staging and the selected map is Space Transform map - sn\_wsd\_core\_space.

9.  Select **Transform**.

10. Verify that the data records were imported into the Spaces table by navigating to **Workplace Safety Management** &gt; **Space Administration** &gt; **Spaces**


**Parent Topic:**[Providing your workplace data](../concept/providing-your-workplace-data.md)

**Related topics**  


[Run an import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_RunImport.md)

[Create a transform map](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_CreateATransformMap.md)

