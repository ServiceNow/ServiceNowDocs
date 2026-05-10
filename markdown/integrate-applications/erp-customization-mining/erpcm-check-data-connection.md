---
title: Check and troubleshoot the data refresh status for ERP Semantic Mining
description: Check the data refresh status to find out when ERP Semantic Mining most recently loaded ERP \(Enterprise Resource Planning\) data from the system of record.
locale: en-US
release: australia
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Configure, ERP Semantic Mining overview, Workflow Data Fabric]
---

# Check and troubleshoot the data refresh status for ERP Semantic Mining

Check the data refresh status to find out when ERP Semantic Mining most recently loaded ERP \(Enterprise Resource Planning\) data from the system of record.

## Before you begin

Role required: sn\_erp\_mining.erp\_admin and sn\_erp\_mining.erp\_user

**Important:** Starting with the Zurich release, ERP Semantic Mining is being prepared for future deprecation. It will be hidden and no longer activated on new instances but will continue to be supported.

## About this task

To verify that ServiceNow AI Platform® is synchronized with the ERP system of record, ServiceNow AI Platform reloads data every 24 hours from the system of record.

You can receive email notifications for connection task success and failures. For more information, see [Getting notifications for ERP Semantic Mining connection updates](../concept/erpcm-notifications.md).

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Semantic Mining**.

2.  In the side panel, select the connection status icon.

    The **Overview** tab displays a summary of connection issues to review, as well as a list of the most recent active connection tasks.

3.  Check the most important connection details in the **Connection status** page header.

    |Field|Definition|
    |-----|----------|
    |Credential alias|Alias of the connection credentials configured in Zero Copy Connector for ERP.|
    |Updated by|Name of the last account to update the connection credentials.|
    |ERP heartbeat|Indicates whether a ping to the connection is successful.|
    |Task execution|Indicates whether ServiceNow AI Platform® is attempting to connect to the instance.|

4.  View a refined subset of connection tasks by selecting one of the following tabs.

<table id="choicetable_s1g_n5l_zwb"><thead><tr><th align="left" id="d226854e209">

Tab

</th><th align="left" id="d226854e212">

Description

</th></tr></thead><tbody><tr><td id="d226854e218">

**All tasks**

</td><td>

Log list of all connection tasks.

</td></tr><tr><td id="d226854e227">

**Task issues**

</td><td>

Log list of all connection tasks that have an **Error** or **Warning** status.

</td></tr><tr><td id="d226854e242">

**Snapshots**

</td><td>

List of scan results that have been saved, exported, and imported.

</td></tr></tbody>
</table>5.  Troubleshoot any system connection issues using the **Change system** button.

    -   Pause the task execution by selecting **Stop task execution**.
    -   Restart the ETL \(extract, transform, and load\) process by selecting **Retry ETL process**.
    -   Delete all data in ERP Semantic Mining and start over by selecting **Delete data**. On the confirmation dialog, you must select the **Yes, I am sure I want to delete data** option and select the **Delete data** button.

        **Warning:** This action deletes all existing data in the ERP Semantic Mining workspace and restarts the data integration process.

    -   Share and back up data at any time by selecting **Export data**. A downloadable zip file is created.
    -   After exporting data, use the created zip file **Import data** for sharing and back up.
    -   Use **Run AI/ML analysis** when changing existing models or importing new models, to verify that the ML training in the mining process is based on the relevant data.
    -   Use **Reset AI/ML analysis** to reset the analysis so the flow can run again. This reset enables you to control the ML training in the mining process.
6.  View the information for each task and note actions that you must take by scrolling to the task list.

    For a description of the field values, see [ERP Semantic Mining task list field descriptions](../reference/erpcm-task-list-details.md).

    For any column, you can select the more options icon ![](../../../administer/integrationhub/images/more-options-icon.png) to perform additional actions, such as **Show matching** and **Filter out**.

7.  Update the status of any open task in error to indicate changes to its status.

    You can't resolve errors directly in ERP Semantic Mining, but you can mark them as resolved or irrelevant.

    1.  Select the **Task** tab.

    2.  On the **Task** tab, select the task that you want to update.

    3.  Update the **Status** on the task record to **Resolved** or **Irrelevant**.

8.  Refresh the Issues to review list and the Executed tasks list by selecting their respective refresh icons ![](../image/refresh-icon.png).


**Parent Topic:**[Configuring ERP Semantic Mining](../concept/configuring-ecm.md)

