---
title: CMDB — Critical application services
description: Use this example to build a CMDB query to find all critical application services, and their owner.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Example queries, Reference, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB — Critical application services

Use this example to build a CMDB query to find all critical application services, and their owner.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder** and then select **Create new**.

2.  Enter `All critical application services` as the query **Name**.

3.  Choose **CMDB Query** and then select **Create**.

4.  In the **CMDB Classes** list, locate the **Application Service** class and then drag it to the canvas.

    **Tip:** Use the search box to find items quickly.

5.  Add a filter to the application service node.

    1.  Point to the application service node and then select the **Apply filters** icon.

    2.  In the Filters section, add the condition **\[business criticality\] \[is\] \[1 - most critical\]**.

    3.  Close the Filters section.

6.  Add columns to the query results.

    1.  In the Properties sidebar, select **Add Columns**.

    2.  Select **business criticality** and **owned by**, and then select outside the columns list to close it.

7.  Select **Save**.

8.  Select **Run** and then review the results.

    You can, for example, locate any of the critical application services without an owner.


