---
title: CMDB — Hardware with Windows installed
description: Use this example to build a CMDB query to find all hardware in my service offering that has Microsoft Windows installed.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Example queries, Reference, CMDB Query Builder, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# CMDB — Hardware with Windows installed

Use this example to build a CMDB query to find all hardware in my service offering that has Microsoft Windows installed.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CMDB Query Builder** and then select **Create new**.

2.  Enter `All hardware in my service offering that has Windows installed` as the query name.

3.  Choose **CMDB Query** and then select **Create**.

4.  In the **CMDB Classes** list, locate the following classes, and then drag them to the canvas:

    **Tip:** Use the search box to find items quickly.

    -   **Service**
    -   **Service Offering**
    -   **Application Service**
    -   Searching for infrastructure, **Hardware**
5.  Connect the Service node to the Service Offering node.

    In the Properties sidebar, select **Add Relationship Type** and select the **Connect to::Connected by** relationship.

6.  Connect the Serviced Offering node to the Application Service node.

    In the Properties right-side bar, select **Add Relationship Type** and select the **Connect to::Connected by** relationship.

7.  Select the Application Service node.

    In the Properties right-side bar, select **Convert attached nodes to pattern** to include all CIs within the application service, in the query.

8.  Connect the Application Service node to the Hardware node.

9.  All infrastructure under Service,

10. Select **Save**.

11. Select **Run** and then review the results.

    You can select **Column options** of the Service column header, and select to **Group by Service**. Then expand a service to see all the hardware infrastructure under that service.

12. Return to the CMDB Query Builder window, to expand the query to include only infrastructure CIs on which Windows is installed.

13. Select **Non-CMDB Tables**, locate the **Software Instance** class, and drag it to the canvas.

14. Connect the Hardware node to the Software Instance node.

    In the Properties right-side bar, set **Use CI reference column** to **Installed on**.

15. Point to the Software Instance node, and select on the **Apply filters** icon that appears.

    1.  In the Filters section, add the condition **\[Product Name.Name\] \[is\] \[windows\]**.

    2.  Close the Filters section.

16. Select **Save**.

17. Select **Run** and review the new results.


