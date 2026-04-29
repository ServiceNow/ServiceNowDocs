---
title: CMDB — Application services with incident or change
description: Use this example to build a CMDB query to find all application services for which there is an incident or a change request. Results are returned for either the application service itself or any CI within the service.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example queries, Reference, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB — Application services with incident or change

Use this example to build a CMDB query to find all application services for which there is an incident or a change request. Results are returned for either the application service itself or any CI within the service.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder**.

2.  Select **Create new** and then enter `Application services with incidents or change requests` as the query name.

3.  Choose **CMDB Query** and then select **Create**.

4.  In the **CMDB Classes** list, locate the **Application Service** class and then drag it to the canvas.

    **Tip:** Use the search box to find items quickly.

5.  Select **Non-CMDB Tables**.

6.  Locate the **Incidents** class in the class hierarchy, and then drag it to the canvas.

7.  Locate the **Change Requests** class in the class hierarchy, and then drag it to the canvas.

8.  Connect the Application Service and the Incidents nodes, and then, in the Properties right-side bar.

    1.  Select **Apply Incidents reference filter to all nodes in the pattern**.

    2.  Set **Use CI reference column** to **Configuration item**.

9.  Connect the Application Service and the Change Request node, and then, in the Properties right-side bar.

    1.  Select **Apply Change Request reference filter to all nodes in the pattern**.

    2.  Set **Use CI reference column** to **Configuration item**.

10. Select the **And** operator between the Incidents and the Change Request nodes, and switch it to **Or**.

11. Select **Save**.

12. Select **Run** and then review the results.


