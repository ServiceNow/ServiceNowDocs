---
title: View Log fields and description
description: The knowledge View log stores the history of knowledge articles views and their usage.
locale: en-US
release: australia
product: Knowledge Management
classification: knowledge-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [View knowledge logs, Configuring Knowledge Management, Knowledge Management, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# View Log fields and description

The knowledge View log stores the history of knowledge articles views and their usage.

The View log shows who has viewed which knowledge articles and who has attached a knowledge article to a task and when. It identifies final search terms when the type-ahead search suggestions feature is enabled. The View log displays data from the Knowledge Use \[kb\_use\] table.

As an administrator and knowledge manager, you can access the view log by navigating to **All** &gt; **Knowledge** &gt; **Administration** &gt; **View Log**.

The following table describes some of the fields in the View log.

|View log field|Description|
|--------------|-----------|
|Created|Date and time when the article was viewed or used by the user.|
|Article|Article that was viewed or used by the user.|
|User|User who viewed or used the article|
|Used|If set to true, the article was attached to a task \(case, incident, and the like\).|
|Viewed|If set to true, indicates that the article was viewed.|
|Search Id|Reference ID of the Search log \(ts\_query\_kb\). This links the search performed by a user to the article viewed from the search results.|
|Session Id|Unique identifier for user session.|
|Times Viewed|How many times the article was viewed.|

**Parent Topic:**[View knowledge logs](../task/view-knowledge-logs.md)

