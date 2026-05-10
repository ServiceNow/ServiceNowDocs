---
title: Create a cross-scope access privilege for the AI Search dashboards
description: Enable the AI Search dashboards to read records from tables that cannot be accessed from the Advanced AI Search Management Tools application scope.
locale: en-US
release: australia
product: AI Search
classification: ai-search
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Advanced AI Search Management Tools, ServiceNow Store applications and integrations, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Create a cross-scope access privilege for the AI Search dashboards

Enable the AI Search dashboards to read records from tables that cannot be accessed from the Advanced AI Search Management Tools application scope.

## Before you begin

The Platform Analytics Solution for Advanced AI Search Management Tools must be activated on your instance. For details on activating this solution, see [Activate the Platform Analytics Solution for Advanced AI Search Management Tools](install-adv-ais-mgmt-tools.md).

Role required: admin

## About this task

The AI Search Profile and AI Search dashboards belong to the Advanced AI Search Management Tools application scope.

If an indexed source or search source table can't be accessed from this scope, the dashboards display the following informational message:

`Read operation on table '<name>' from scope 'Advanced AI Search Management Tools' was denied. The application 'Advanced AI Search Management Tools' must declare a cross scope access privilege. Please contact the application author to update their privilege requests.`

To resolve this issue, define a cross-scope table access privilege for the Advanced AI Search Management Tools application.

For more information on cross-scope privileges, see [Cross-scope privilege record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/c_CrossScopePrivilegeRecord.md).

## Procedure

1.  Set your current application scope context to Advanced AI Search Management Tools using [the application picker](../../../build/applications/task/t_SelectAnAppFromTheAppPicker.md).

2.  Navigate to **All** &gt; **System Applications** &gt; **Application Cross-Scope Access**.

3.  Select **New**.

4.  On the Cross scope privilege form, enter the following field values.

    |Field|Value|
    |-----|-----|
    |Target Scope|&lt;table scope&gt;|
    |Target Name|&lt;table name&gt;|
    |Target Type|Table|
    |Operation|Read|
    |Status|Allowed|

5.  Select **Submit**.


## Result

The new cross-scope privilege appears in the Cross scope privilege table.

