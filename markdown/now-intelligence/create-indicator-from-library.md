---
title: Create an indicator from the library
description: From the indicator library, you can launch a process to create different kinds of indicators from different sources
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Indicator library, Platform Analytics experience, Platform Analytics]
---

# Create an indicator from the library

From the indicator library, you can launch a process to create different kinds of indicators from different sources

## Before you begin

Role required: pa\_power\_user or higher

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Indicators**.

2.  Select **Create indicator**.

    ![Create indicator button on indicator library page.](../image/create-indicator-button.png)

3.  Select the type of indicator: Automated, Formula, Manual, External.

    ![Create new indicator page opened from indicator library.](../image/create-new-indicator-page.png)

    -   **Automated indicator**

        An automated indicator uses an indicator source as its data set. The indicator source specifies a table or database view, conditions for filtering records from that source, and the frequency at which you expect to display the data. The indicator applies an aggregator and optional conditions to this data. If you have Data snapshots enabled on your instance, you can base automated indicators on Data snapshots sources, instead.

    -   **Formula indicator**

        The score of a formula indicator is calculated from a mathematical statement that includes data from one or more other indicators. This data can be the score of an indicator or a PAFormulaUtils\(\) calculated value for the indicator. If you have Data snapshots enabled on your instance, you can use Data snapshots indicators in the formula. However, you cannot mix classic and Data snapshots indicators in the formula, and PAFormulaUtils\(\) does not support Data snapshots.

    -   **Manual indicator**

        In some cases, you must manually enter indicator scores into a scoresheet.

    -   **External indicator**

        You can collect data via SQL queries from JDBC data sources external to the ServiceNow AI Platform.

4.  Under **Source type**, if you have Data snapshots enabled on the instance and you are creating an automated or formula indicator, select whether to use a Data snapshots source or a classic indicator source.

5.  Provide a meaningful name and description for the indicator.

6.  Select **Create**.


## Result

You are taken to the appropriate form, depending on your selection.

## What to do next

Follow the instructions for the form that opens:

-   [Create an automated indicator](t_CreateAnAutomatedIndicator.md#)
-   [Create a formula indicator](t_CreateAFormulaIndicator.md)
-   [Manual indicators](t_CreateAManualIndicator.md)
-   [Using Performance Analytics with external data](../concept/pa-external-data.md#)

