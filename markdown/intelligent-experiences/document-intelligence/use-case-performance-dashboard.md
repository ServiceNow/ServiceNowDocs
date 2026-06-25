---
title: Use case performance dashboard
description: Monitor Document Intelligence \(DocIntel\) performance at the use case and field levels in the use case performance dashboard.Access the use case performance dashboard in the Performance tab on the use case screen.The use case performance dashboard provides data visualizations to display your usage and performance data for the use case.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/document-intelligence/use-case-performance-dashboard.html
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Monitor, Document Intelligence, Enable AI experiences]
---

# Use case performance dashboard

Monitor Document Intelligence \(DocIntel\) performance at the use case and field levels in the use case performance dashboard.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-in-document-intelligence/docintel-nowassist-landing.md).

## Overview of the use case performance dashboard

The use case performance dashboard provides quality metrics for the use case.

\[Omitted image "docintel-use-case-dashboard.png"\] Alt text: Performance dashboard showing metrics on Document Intelligence use case activity.

The data visualizations show document extraction activity for the use case. For example:

-   Agent effort to process document tasks
-   Accuracy of the DocIntel recommendations

This dashboard provides useful answers to the following questions:

-   How much effort is needed to complete document tasks for this use case?
-   How has DocIntel accuracy progressed for this use case?

**Parent Topic:**[Monitoring Document Intelligence performance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/monitoring-document-intelligence-performance.md)

**Related topics**  


[View reports on the Document Intelligence Admin home page]()

[Document Intelligence monitoring dashboard]()

## View the use case performance dashboard

Access the use case performance dashboard in the Performance tab on the use case screen.

### Before you begin

-   Ensure that the Document Intelligence application \(sn\_docintel\) and Document Intelligence Admin \(com.snc.docintel\_admin\) ServiceNow® Store application is installed and active. For more information, see [Install Document Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/install-document-intelligence.md).
-   Have an active use case with multiple completed document tasks. For more information, see [Set up document extraction use cases](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/document-intelligence/set-up-document-extraction-use-cases.md).
-   Role required: sn\_docintel.admin, sn\_docintel.manager, or admin.

### Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Use Cases**.

2.  Select the **Performance** tab.

3.  Select a date range in the **Date range** filter to show only the data within the selected dates.

4.  Select one or more fields in the **Fields** filter to show only the data that applies to the selected fields.

5.  Select one or more field types in the **Field type** filter to show only the data that applies to the selected field types.

6.  Select an object within a data visualization to see additional details.


## Data visualizations in the use case performance dashboard

The use case performance dashboard provides data visualizations to display your usage and performance data for the use case.

The following table describes the data visualizations shown on the **Performance** tab.

|Name|Description|
|----|-----------|
|Accuracy of extraction|The average extraction accuracy per time period for the use case. Accuracy is defined as the number of times that the AI's top recommendation is the correct answer.|
|Agent effort|The number of keystrokes your agents need to press in order to extract all field values for a document task. This measurement is an average per document task.|
|Rank of recommendations selected|The number of times that DocIntel recommendations from were selected by an agent when completing a document task, grouped by the order presented.|
|Field level accuracy|The percentage of times that the top recommendation from DocIntel is the correct value for a field.|
|Average key strokes per field|The average number of keystrokes an agent performs to extract a value for a field.|
|Field level accuracy over time|The percentage of times over the selected date range that the top recommendation from DocIntel is the correct value for a field.|

