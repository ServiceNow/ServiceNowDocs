---
title: Service Mapping — Linux servers in services
description: Use this example to build a Service Mapping query to find all Linux servers in services.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example queries, Reference, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Service Mapping — Linux servers in services

Use this example to build a Service Mapping query to find all Linux servers in services.

## Before you begin

Role required: none

## About this task

This example Service Mapping query finds all services that include Linux servers. Then, with a simple modification, the query can find all services that do not include a Linux server.

## Procedure

1.  Navigate to **All** &gt; **Configuration** and select **CMDB Query Builder**.

2.  Select **Create new** and then enter `Linux server in services` in the **Name** field.

3.  Choose **Service Mapping Query** and then select **Create**.

4.  In the **CMDB Classes** hierarchy list, locate **Linux Server** and drag it to the canvas.

    **Tip:** Use the search box to find items quickly.

5.  Select **Run**.

    Review the query results. Each row displays the name of a Service Mapping service and the name of a Linux server that is a member of that service.

6.  On the right-side pane, disable **Services Including This Pattern** and then select **Run** again.

    Review the query results. Now, each row displays the name of a Service Mapping service that doesn't include the specified Linux server.


