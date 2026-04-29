---
title: Known error article form
description: Description of the field values for the legacy problem form.
locale: en-US
release: australia
product: Problem Management
classification: problem-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference section for Problem Management, Problem Management, IT Service Management]
---

# Known error article form

Description of the field values for the legacy problem form.

|Field|Description|
|-----|-----------|
|Number|Read-only field. Unique number to identify the known error article.|
|Knowledge base|Knowledge base \(defaults to Known Error\) in which the article is stored for future reference. The article is saved in the Known Error article \[kb\_template\_known\_error\_article\] table.|
|Category|Read-only field. The value of this field is reference from the Category field of the Problem.|
|Valid to|Date after which the known error article is deleted from the database. After this date, the article does not appear in the search result.|
|Version|Read-only field. Managed by the Knowledge Management process when changes are made to a published article.|
|Workflow|Read-only field.|
|Source Task|Read-only field. The Problem record on which you are creating the article.|
|Attachment link|Select the check box so that the article appears as an attachment in the Problem record. If you do not select the check box, the content of the article appears in the work note of the Problem.|
|Display attachments|Select the check box so that all attachments to the article appear when you view the article. The field is relevant only when the Attachment link field is not selected.|
|Short description|Brief description of the Known Error.|
|Description|Detailed explanation of the Known Error.|
|Workaround|Method that you have used to overcome the Problem. It can be a way of dealing with a problem or making something work despite the problem not being resolved.|
|Cause|Information on what had caused the problem.|

**Parent Topic:**[Reference section for Problem Management](../concept/reference-section-for-problem-management.md)

