---
title: Enable Software Editions in Service Graph Connector for Microsoft SCCM
description: Enable software editions so that you can gather edition information for products such as Adobe Acrobat, Microsoft SQL Server, and Windows Exchange Server into the Service Graph Connector for Microsoft SCCM.
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Microsoft SCCM, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Enable Software Editions in Service Graph Connector for Microsoft SCCM

Enable software editions so that you can gather edition information for products such as Adobe Acrobat, Microsoft SQL Server, and Windows Exchange Server into the Service Graph Connector for Microsoft SCCM.

## Before you begin

**Note:** There are two types of setup that are required, one on the SCCM Manager and the other on the ServiceNow Instance. For more information on how to set up the SCCM Manager, see the SCCM Manager Setup section of the [Custom solution to gather editions in SCCM \[KB0721360\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0721360) article on the HI Knowledge Base. When you're finished setting up the SCCM Manager, refer back to this task and complete the steps.

Role required: admin

## About this task

You can set up the ServiceNow Instance on the Service Graph Connector for Microsoft SCCM.

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connector Microsoft SCCM** &gt; **Import Schedules**.

2.  Select the Software Edition scheduled import you created to edit this import record.

3.  Select the **Active** check box.

4.  Click **Update**.

5.  Navigate to **Service Graph Connector Microsoft SCCM** &gt; **Data Sources**.

6.  Select the Software Edition data source you created.

7.  Under the Transforms list, select **Update software install with edition**.

8.  Edit the data source and select the **Active** check box.

9.  Click **Update**.


## What to do next

You can verify that the edition information has been gathered by doing the following:

1.  Navigate to **Service Graph Connector Microsoft SCCM** &gt; **Data Sources** and the Software Edition data source you want to verify.
2.  Select **Load All Records**.

**Note:** If the displayed completion code is `Success`, then the software edition data source was executed successfully. If the displayed completion code is `Error`, then there is an error that must be fixed.

