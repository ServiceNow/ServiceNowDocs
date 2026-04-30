---
title: Document Intelligence monitoring dashboard
description: Monitor the overall performance of Document Intelligence over time in the Document Intelligence monitoring dashboard.Access the Document Intelligence monitoring dashboard on the Monitoring screen of the Admin experience.The Document Intelligence monitoring dashboard uses data visualizations to display your Document Intelligence \(DocIntel\) usage and performance data.
locale: en-US
release: yokohama
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Monitoring Document Intelligence performance, Document Intelligence, Enable AI experiences]
---

# Document Intelligence monitoring dashboard

Monitor the overall performance of Document Intelligence over time in the Document Intelligence monitoring dashboard.

## Overview of the Document Intelligence monitoring dashboard

The Document Intelligence monitoring dashboard provides a high-level overview of your Document Intelligence usage and value.

![Document Intelligence monitoring dashboard showing metrics on DocIntel activity.](../image/docintel-monitoring-page.png)

The data visualizations show document extraction activity in your instance. For example:

-   Active use cases
-   Active document tasks
-   Processed pages
-   Processed document tasks
-   Accuracy of the DocIntel recommendations

This dashboard provides useful answers to the following questions:

-   How many documents are processed using DocIntel?
-   How much of the document extraction is automated?
-   How has DocIntel accuracy progressed over time?

**Parent Topic:**[Monitoring Document Intelligence performance](monitoring-document-intelligence-performance.md)

**Related topics**  


[View reports on the Document Intelligence Admin home page](doc-intel-monitor-performance.md)

[Use case performance dashboard](use-case-performance-dashboard.md#)

## View the Document Intelligence monitoring dashboard

Access the Document Intelligence monitoring dashboard on the Monitoring screen of the Admin experience.

### Before you begin

-   Ensure that the Document Intelligence application \(sn\_docintel\) and Document Intelligence Admin \(com.snc.docintel\_admin\) ServiceNow® Store application is installed and active. For more information, see [Install Document Intelligence](../task/install-document-intelligence.md).
-   Have an active use case with multiple completed document tasks. For more information, see [Set up document extraction use cases](set-up-document-extraction-use-cases.md).
-   Role required: sn\_docintel.admin, sn\_docintel.manager, or admin.

### Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Monitoring**.

2.  Select a date range in the **Date range** filter to show only the data within the selected dates.

3.  Select one or more use cases in the **Use cases** filter to show only the data that applies to the selected use cases.

4.  Select an object within a chart to see additional details.


## Data visualizations in the Document Intelligence monitoring dashboard

The Document Intelligence monitoring dashboard uses data visualizations to display your Document Intelligence \(DocIntel\) usage and performance data.

The following table describes the data visualizations shown on the Monitoring screen.

|Name|Description|
|----|-----------|
|Use cases by mode|The number of document extraction use cases in this instance, grouped by extraction mode.|
|Pages processed|The number of pages processed for data extraction using DocIntel in this instance over the selected date range.|
|Document tasks processed|The number of DocIntel document tasks processed in this instance over the selected date range.|
|Document tasks by status|The number of DocIntel document tasks in this instance, grouped by status.|
|Average accuracy per use case|The percentage of times that the top recommendation from DocIntel is the correct field value, based on the tasks completed for a use case.|
|Document tasks per use case|The number of DocIntel document tasks for each use case, grouped by status.|

