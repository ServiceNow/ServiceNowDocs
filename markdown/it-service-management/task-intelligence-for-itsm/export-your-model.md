---
title: Export an incident prediction model
description: Export either the Similar Incidents or Incident Categorization model model in Task Intelligence for ITSM to another instance so you can use the model in the other instance without recreating the model from scratch.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-service-management/task-intelligence-for-itsm/export-your-model.html
release: zurich
product: Task Intelligence for ITSM
classification: task-intelligence-for-itsm
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Manage, Task Intelligence for ITSM, IT Service Management]
---

# Export an incident prediction model

Export either the Similar Incidents or Incident Categorization model model in Task Intelligence for ITSM to another instance so you can use the model in the other instance without recreating the model from scratch.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Task Intelligence for ITSM** &gt; **Setup**.

2.  In the Models list, select the menu \(\[Omitted image "menu-icon.png"\] Alt text: Menu icon\) icon of the model you want to export, and then select **Export model**.

    A new tab opens with authentication steps.

3.  Select **Allow**.


## Result

The XML file of your model downloads to your browser.

## What to do next

You can use the XML file to transfer the model to another instance using update sets. For more information update sets, see [System update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/system-update-sets/system-update-sets.md).

**Parent Topic:**[Managing Task Intelligence for ITSM models](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-service-management/task-intelligence-for-itsm/using-task-intelligence-itsm.md)

