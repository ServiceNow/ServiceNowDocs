---
title: Configure instance API import settings in API Insights
description: Set options to import custom and ServiceNow APIs from your instance into the CMDB.
locale: en-US
release: zurich
product: API Insights
classification: api-insights
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [CMDB administrator tasks, Configure, API Insights, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure instance API import settings in API Insights

Set options to import custom and ServiceNow APIs from your instance into the CMDB.

## Before you begin

Configure the **Import ServiceNow API to API Insights** scheduled job to automatically import configured APIs from your ServiceNow instance into the API Insights workspace at regular intervals. For more information, see [Scheduled jobs](https://www.servicenow.com/docs/access?context=c_ScheduledJobs&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Role required: sn\_cmdb\_admin

## About this task

Configure API import options to bring custom and ServiceNow APIs from your ServiceNow instance into the CMDB. This feature enables you to analyze and manage ServiceNow instance APIs together with other enterprise APIs within the API Insights workspace.

## Procedure

1.  Navigate to **Workspaces** &gt; **API Insights**.

2.  Select the **Settings** tab.

3.  In the Import instance APIs section, select **Configure API import**.

4.  In the Set up import section, select the options for importing scripted and outbound REST APIs, and scripted and outbound SOAP APIs into the CMDB.

    |Option|Description|
    |------|-----------|
    |All custom APIs|Imports all custom-developed APIs within the instance.|
    |ServiceNow APIs|Imports predefined ServiceNow APIs within the instance.|
    |Active in last|Imports only APIs based on recent activity, available for scripted APIs only.|

    1.  If you select the **ServiceNow APIs** check box, select **Select APIs** and then manage the APIs to import.

        |Action|Description|
        |------|-----------|
        |Add ServiceNow APIs|On the Select ServiceNow APIs page, select **Add to import list**. Then, on the Add to import list page, select the check box for APIs from the All ServiceNow APIs list and select **Add selected**.|
        |Remove any selected ServiceNow APIs|On the Select ServiceNow APIs page, select the check box for APIs from the Selected APIs list, and select **Remove from import list**.|

    2.  If you select the **Active in last** option, enter the number of days in the **Days** field to import only APIs that have been active in the specified timeframe.

5.  On the Select ServiceNow APIs page, select **Done**.

6.  On the Configure API import page, select **Save configuration**.


