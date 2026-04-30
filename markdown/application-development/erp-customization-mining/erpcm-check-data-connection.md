---
title: Check and troubleshoot the data refresh status for ERP Customization Mining
description: Check the data refresh status to find out when ERP Customization Mining \(ERP-CM\) most recently loaded ERP \(Enterprise Resource Planning\) data from the system of record.
locale: en-US
release: xanadu
product: ERP Customization Mining
classification: erp-customization-mining
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Configuring ERP Customization Mining, ERP Customization Mining \(ERP-CM\), Building low-code applications, Developing your application, Building applications]
---

# Check and troubleshoot the data refresh status for ERP Customization Mining

Check the data refresh status to find out when ERP Customization Mining \(ERP-CM\) most recently loaded ERP \(Enterprise Resource Planning\) data from the system of record.

## Before you begin

Role required: sn\_erp\_mining.erp\_admin and sn\_erp\_mining.erp\_user

## About this task

To verify that ServiceNow AI Platform® is synchronized with the ERP system of record, ServiceNow AI Platform reloads data every 24 hours from the system of record.

You can receive email notifications for connection task success and failures. For more information, see [Getting notifications for ERP Customization Mining connection updates](../concept/erpcm-notifications.md).

## Procedure

1.  Navigate to **All** &gt; **ERP Foundation** &gt; **ERP Customization Mining**.

2.  In the side panel, select the connection status icon \(![Credential alias page link](../image/credential-alias-icon.png)\).

    The **Overview** tab displays a summary of connection issues to review, as well as a list of the most recent active connection tasks.

3.  Check the most important connection details in the **Connection status** page header.

    |Field|Definition|
    |-----|----------|
    |Credential alias|Alias of the connection credentials configured in ERP Data Hub.|
    |Updated by|Name of the last account to update the connection credentials.|
    |ERP heartbeat|Indicates whether a ping to the connection is currently successful.|
    |Task execution|Indicates whether ServiceNow AI Platform® is currently attempting to connect to the instance.|

4.  View a refined subset of connection tasks by selecting one of the following tabs.

<table id="choicetable_s1g_n5l_zwb"><thead><tr><th align="left" id="d160216e209">

Tab

</th><th align="left" id="d160216e212">

Description

</th></tr></thead><tbody><tr><td id="d160216e218">

**All tasks**

</td><td>

Log list of all connection tasks.

</td></tr><tr><td id="d160216e227">

**Task issues**

</td><td>

Log list of all connection tasks that have an **Error** or **Warning** status.

</td></tr><tr><td id="d160216e242">

**Snapshots \(available in Xanadu Store Release 2\)**

</td><td>

List of scan results that have been saved, exported, and imported.

</td></tr></tbody>
</table>5.  Troubleshoot any system connection issues using the **Change system** button \(Xanadu Store Release 1\) or **Connect system** button \(Xanadu Store Release 2\).

    ![Troubleshoot the system connection using the Change system or Connect system button](../image/ecm-change-connection.png)

    -   Pause the task execution by selecting **Stop task execution**.
    -   Restart the ETL \(extract, transform, and load\) process by selecting **Retry ETL process**. \(Xanadu Store Release 1\)
    -   Delete all data in ERP-CM and start over by selecting **Delete data**. On the confirmation dialog, you must select the **Yes, I am sure I want to delete data** option and select the **Delete data** button.

        **Warning:** This action deletes all existing data in the ERP-CM workspace and restarts the data integration process.

    -   Share and back up data at any time by selecting **Export data**. A downloadable zip file is created.
    -   After exporting data, use the created zip file **Import data** for sharing and back up.
    -   Run AI/ML
6.  View the information for each task and note any actions that you must take by scrolling to the task list.

    For a description of the field values, see [ERP-CM task list field descriptions](../reference/erpcm-task-list-details.md).

    For any column, you can select the more options icon \(![More options icon](../../../administer/ui-builder/image/more-options-icon.png)\) to perform additional actions, such as **Show matching** and **Filter out**.

7.  Update the status of any open task in error to indicate changes to its status.

    You can't resolve errors directly in ERP-CM, but you can mark them as resolved or irrelevant.

    1.  Select the **Task** tab.

    2.  On the **Task** tab, select the task that you want to update.

    3.  Update the **Status** on the task record to **Resolved** or **Irrelevant**.

8.  Refresh the Issues to review list and the Executed tasks list by selecting their respective refresh icons \(![Refresh the Executed tasks list](../image/refresh-icon.png)\).

    ![Refresh the issues list or active connection tasks](../image/ecm-connection-status-page.png)


**Parent Topic:**[Configuring ERP Customization Mining](../concept/configuring-ecm.md)

