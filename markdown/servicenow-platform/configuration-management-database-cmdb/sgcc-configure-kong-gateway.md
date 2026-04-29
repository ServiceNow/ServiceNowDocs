---
title: Configure API Service Graph Connector for Kong Gateway using SGC Central
description: Set up scheduled import jobs to pull in Kong Gateway data into your Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Kong Gateway, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure API Service Graph Connector for Kong Gateway using SGC Central

Set up scheduled import jobs to pull in Kong Gateway data into your Configuration Management Database \(CMDB\).

## Before you begin

Install API Service Graph Connector for Kong Gateway version 2.0.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

If setting up the Prometheus connection, enable the Prometheus plugin on Kong Gateway and verify that any required credentials are available. To learn more about the Prometheus plugin, see [Prometheus](https://developer.konghq.com/plugins/prometheus) on the Kong Developer documentation site.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

**Note:** Alternatively, you can configure a default connection already available from the installed or draft connections in SGC Central. Go to **All** &gt; **Service Graph Connectors**, then select **Setup** for the connector from the menu. To learn about installed and draft connections, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the Kong connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

6.  Select a template for the authentication type to create a connection.

    1.  In the **Setup** stage of the playbook, select the **Select alias template** activity.

    2.  Select a template type.

        -   **Kong RBAC Authentication**: Select when using token-based authentication.
        -   **Kong Basic Authentication**: Select when using basic authentication.
7.  Enter connection details and test the API connection for importing Kong Gateway data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

        |Field|Description|
        |:----|:----------|
        |Connection Name|Name to identify the Kong Gateway connection record.|
        |Host Name|Admin URL address of the Kong Admin API server.|
        |Protocol|Protocol used for the connection ensuring secured communication between the client and the Kong server.|
        |Override default port|Port used by the Kong Admin API.|
        |API Key|Authentication secret to connect to the Kong Gateway service. This field appears only when **Kong RBAC Authentication** is selected in the **Select alias template** activity.|
        |User Name|User name required for authenticating requests to the Kong Gateway Admin API. This field appears only when **Kong Basic Authentication** is selected in the **Select alias template** activity.|
        |Password|Password associated with the user name required for authenticating requests. This field appears only when **Kong Basic Authentication** is selected in the **Select alias template** activity.|

    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

8.  Set the configuration properties for the connection.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  In the **Expand HTTP Method Types** field available in the Data retrieval configuration section, enter the HTTP methods including `GET`, `POST`, `PUT`, `PATCH`, `DELETE`, `OPTIONS`, `HEAD`, `CONNECT`, and `TRACE`, to consider for routes.

        For multiple methods, separate them with commas. If left blank, results in a single API Frontend being created with the `ALL` method, indicating support for all standard HTTP methods.

    3.  In the **Exclude workspaces** field available in the Property settings section, enter the workspace that must be excluded from import.

        For multiple workspaces, separate them with commas. For example: `workspace1,workspace2`. If you leave this field empty, the data sources within the connector import data from all the workspaces.

    4.  Select the **Import tags** check box available in the tag settings section, to ingest tags from the Kong Gateway service.

        When selected, specify the key-value pair separator for tags in the **Tags value separator** field. If not selected, tags won't be fetched.

    5.  In the **Tags value separator** field available in the tag settings section, enter the separator for key and value in tags.

        For example, if the tag value separator is set to `=`, the tag `env=prod` is saved with `env` as the key and `prod` as the value.

        If left empty, no tags will be ingested.

    6.  Select the **Collect Usage Data** check box available in the Metric Settings section to enable usage data collection to retrieve API usage data over a specified duration.

    7.  In the **Collection period \(in days\)** field available in the Metric Settings section, enter the duration in days for collecting API usage data.

    8.  Select **Continue**.

9.  Enter Prometheus connection details and test the API connection for importing Kong Gateway metrics data using the Prometheus plugin.

    **Note:** You can skip this step if API usage monitoring with Prometheus isn't required or if you're using an existing Prometheus instance. To skip this step, select **Skip** for the **Create and Test Prometheus Connection** activity.

    1.  In the **Setup** stage of the playbook, select the **Create and Test Prometheus Connection** activity.

    2.  On the form, fill in the fields.

        |Field|Description|
        |:----|:----------|
        |Connection Name|Name to identify the Prometheus connection record.|
        |Connection URL|Base URL of the Prometheus HTTP API, used for fetching metrics.|
        |User Name|User name required for authenticating requests to the Prometheus server.|
        |Password|Password associated with the user name required for authenticating requests to the Prometheus server.|

    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

10. Associate the Prometheus connection with a Kong Gateway connection.

    **Note:** You can skip this step if API usage monitoring with Prometheus isn't required. To skip this step, select **Skip** for the **Kong Prometheus Mapping** activity.

    1.  In the **Setup** stage of the playbook, select the **Kong Prometheus Mapping** activity.

    2.  In the **Prometheus Connections** field, search for and select a Prometheus connection to associate.

        You can select the Prometheus connection created in step [9](sgcc-configure-kong-gateway.md#prometheus-connection) or select any existing Prometheus connection during this step. If you skip step [9](sgcc-configure-kong-gateway.md#prometheus-connection), select any existing Prometheus connection.

    3.  Select **Submit**.

    A Prometheus connection can be associated with multiple Kong Gateway connections. You can update the Prometheus mapping in the Kong Gateway connection from the SGC Central view at any time. See [Update a connection for a Service Graph Connector in SGC Central](sgcc-update-connection.md).

11. Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Select **Configure import schedule**.

    3.  Expand the Parent scheduled data import within the Import schedules list to select the **SG-Kong Gateway** import schedule associated with your connection.

        **Note:** The connection name is prefixed to the schedule name.

    4.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    6.  Select **Continue**.

12. In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to check whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The configured connections, including the Kong Gateway connection and the Prometheus connection, if created, appear in the Installed connections list.

You can then manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

**Related topics**  


[API Service Graph Connector for Kong Gateway](../../configuration-management/concept/api-sgc-kong-gateway.md)

[Target tables for storing API Service Graph Connector for Kong Gateway data](../../configuration-management/reference/api-sgc-kong-gateway-tables.md)

