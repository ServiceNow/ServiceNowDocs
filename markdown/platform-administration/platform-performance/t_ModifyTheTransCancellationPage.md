---
title: Add or modify a transaction cancellation message
description: The Quota Manager uses a UI page to control the contents of the transaction cancellation message.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-administration/platform-performance/t\_ModifyTheTransCancellationPage.html
release: zurich
product: Platform Performance
classification: platform-performance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Transaction quotas, Configure, Platform performance, Maintain and monitor, Administer]
---

# Add or modify a transaction cancellation message

The Quota Manager uses a UI page to control the contents of the transaction cancellation message.

## Before you begin

Role required: admin

## About this task

Knowledge of [Apache Jelly](http://commons.apache.org/jelly/) is highly recommended when modifying the UI page. See Extensions to Jelly syntax for more information.

## Procedure

1.  Navigate to **All** &gt; **System UI** &gt; **UI Pages**.

2.  Open the UI page with the name **transaction\_canceled\_quota**.

3.  In the **HTML** field, add or modify the new cancellation message.

    To add variable information to the cancellation message, see [Methods to add variable information to the cancellation message](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/platform-performance/r_AddVarInfoToTheCancellationMsg.md).

4.  Click **Update**.


**Parent Topic:**[Maintaining and monitoring the ServiceNow AI Platform](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-administration/ai-platform-administration/maintain-monitor-now-platform.md)

