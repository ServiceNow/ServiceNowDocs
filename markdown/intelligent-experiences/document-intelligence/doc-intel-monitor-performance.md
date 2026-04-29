---
title: View reports on the Document Intelligence Admin home page
description: Monitor document extraction performance in the Admin experience.
locale: en-US
release: australia
product: Document Intelligence
classification: document-intelligence
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Monitor, Document Intelligence, Enable AI experiences]
---

# View reports on the Document Intelligence Admin home page

Monitor document extraction performance in the Admin experience.

**Important:** Starting with the Zurich release, Document Intelligence is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported. For details, see the Deprecation Process article \[[KB0867184](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0867184)\] in the Now Support Knowledge Base. Instead, you can extract information from documents using the Now Assist in Document Intelligence application. For more information, see [Now Assist in Document Intelligence](docintel-nowassist-landing.md).

## Before you begin

-   Ensure that the Document Intelligence application \(sn\_docintel\) and Document Intelligence Admin \(com.snc.docintel\_admin\) ServiceNow® Store application is installed and active. For more information, see [Install Document Intelligence](../task/install-document-intelligence.md).
-   Have an active use case with multiple completed document tasks. For more information, see [Set up document extraction use cases](set-up-document-extraction-use-cases.md).
-   Role required: sn\_docintel.admin, sn\_docintel.manager, or admin.

## About this task

You can review the value of your Document Intelligence \(DocIntel\) implementation when you open the Document Intelligence Admin experience home page.

The **Monitor DocIntel performance over time** section displays the following measurements:

-   The Accuracy of Extraction widget shows the average extraction accuracy per time period for the selected use case. Accuracy is defined as the number of times that the AI's top recommendation is the correct answer.
-   The Agent effort widget shows the number of keystrokes that your agents need to perform in order to extract all field values for a document task. This measurement is an average per document task.

![Monitor DocIntel performance over time on the DocIntel admin experience.](../image/doc-intel-monitor-performance1.png)

## Procedure

1.  Navigate to **All** &gt; **Document Intelligence** &gt; **Document Data Extraction Administration** &gt; **Home**.

2.  Expand the **Use Case** list and select your use case.

3.  Expand the **Time Period** list and select a date range.

4.  Review the results displayed in the **Accuracy of Extraction** and the **Agent effort** widgets.


**Parent Topic:**[Monitoring Document Intelligence performance](monitoring-document-intelligence-performance.md)

**Related topics**  


[Document Intelligence monitoring dashboard](document-intelligence-monitoring-dashboard.md#)

[Use case performance dashboard](use-case-performance-dashboard.md#)

