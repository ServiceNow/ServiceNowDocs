---
title: Perform initial setup tasks when creating a connection in SGC Central
description: Complete the prerequisites for setting up a connection for the first time using a Service Graph Connector within the SGC Central view of the Service Graph Workspace or CMDB Workspace.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2026-02-27"
reading_time_minutes: 1
breadcrumb: [Managing connections, SGC Central, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Perform initial setup tasks when creating a connection in SGC Central

Complete the prerequisites for setting up a connection for the first time using a Service Graph Connector within the SGC Central view of the Service Graph Workspace or CMDB Workspace.

## Before you begin

Role required: admin

## About this task

During the initial connection setup with a Service Graph Connector, a few tasks appear in the Prerequisites stage. Complete these tasks before proceeding to the next steps.

## Procedure

1.  Create data sources for the connection.

    1.  Ensure that you have edit permissions for the Datasource \[sys\_data\_source\] table.
    2.  In the **Prerequisites** stage of the playbook, select the **Update data source access** activity.
    3.  Select **Update access**.
    4.  To edit the record, select the **Global** application scope from the application picker.
    5.  In the Application Access related list of the Data Source form, select the **Can create**, **Can update**, and **Can delete** check boxes.
    6.  Select **Update**.
    7.  From the application picker, select the application scope of the connector.
    8.  After completing the **Update data source access** activity, select **Continue**.
2.  Clear the cache on the Data Source \[sys\_data\_source\] table.

    1.  In the **Prerequisites** stage of the playbook, select the **Clear cache** activity.
    2.  Select **Run clear cache**.
    3.  In the **Run script** text box of the background script page, enter the following script:

        ```
        GlideTableManager.invalidateTable("sys_data_source");
        GlideCacheManager.flushTable("sys_data_source");
        GlideTableManager.invalidateTable("sys_db_object");
        GlideCacheManager.flushTable("sys_db_object");
        ```

    4.  Select **Run Script** to run the background script in the **global** scope.

        The script may take several minutes to execute.

    5.  After the script is executed, select **Close**.
    6.  From the application picker, select the application scope of the connector.
    7.  After completing the **Clear cache** activity, select **Continue**.

