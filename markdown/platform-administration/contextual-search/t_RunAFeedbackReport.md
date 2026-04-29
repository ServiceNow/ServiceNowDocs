---
title: Run a report on contextual search usage
description: Run a report on usage such as how many times a knowledge article is attached to a record to know the effectiveness of the contextual search results.
locale: en-US
release: australia
product: Contextual Search
classification: contextual-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Feedback information on contextual search, Managing contextual search, Contextual search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Run a report on contextual search usage

Run a report on usage such as how many times a knowledge article is attached to a record to know the effectiveness of the contextual search results.

## Before you begin

Role required: admin

## About this task

A service desk manager can generate a report on user issues that were resolved without an incident being raised. The information can help to create targeted knowledge based on trends. You can analyze commonly raised incidents and then create knowledge articles around those incidents which can help resolve or deflect similar incidents in future.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View/Run**.

2.  Select **Create a report**.

3.  Under **Data**, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Report name|Unique name for the report.|
    |Source type|Source from which the data is populated. The default value is **Data source**. Select **Table**.|
    |Table|Select the Relevant Document Detail table \[cxs\_rel\_doc\_detail\].|

4.  Select **Next**.

5.  Under **Type**, select **Next**.

6.  Under **Configure**, select **Choose columns** and move the required fields from the **Available** box to the **Selected** box.

    ![Select fields for report](../image/cxs-report-column.png)

7.  Select **OK** and then select **Run**.

    ![Contextual search report](../image/run-search-report.png)

    **Note:** When users select the **Search on tab** check box in the Search Context \[csc\_context\_config\] table and then modify and leave the search field, an action gets logged in the Relevant Document Detail table \[cxs\_rel\_doc\_detail\]. The information in the table can help you find the instances where users ran a search but did not take any action. In those cases, the value of the **Position** column is **-1**.


**Parent Topic:**[Feedback information on contextual search](../reference/r_QueryFeedbackInformation.md)

