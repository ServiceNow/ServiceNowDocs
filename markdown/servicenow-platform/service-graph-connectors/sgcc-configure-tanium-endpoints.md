---
title: Configure Service Graph Connector for Tanium Endpoints using SGC Central
description: Use the playbook in SGC Central to set up the Service Graph Connector for Tanium Endpoints and pull Tanium data into your CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgcc-configure-tanium-endpoints.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-05-12"
reading_time_minutes: 4
breadcrumb: [Tanium Endpoints, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Tanium Endpoints using SGC Central

Use the playbook in SGC Central to set up the Service Graph Connector for Tanium Endpoints and pull Tanium data into your CMDB.

## Before you begin

**Important:** The Service Graph Connector for Tanium Endpoints populates the Computer class with user-facing endpoints, and doesn't import data from the Server child class. Use this connector if you don't require Server data. If you require Server data, use the Service Graph Connector for Tanium.

Install Service Graph Connector for Tanium Endpoints from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/installing-applications-in-application-manager.md).

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/configuration-management-database-cmdb/cmdb-sgc-intro.md).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-ui.md).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon \[Omitted image "icon-sgc-central.png"\] to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

3.  On the Create connection window, select the Tanium Endpoints connector type, and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-first-time-setup.md).

5.  Enter connection details and test the connection for importing Tanium data.

    1.  In the **Setup** stage, select **Create and test connection**.

    2.  On the form, fill in the fields.

<table id="table_br3_4cc_mjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Service Graph connection record for Tanium Endpoints.

</td></tr><tr><td>

Host name

</td><td>

Base URL or IP address of the Tanium server.

</td></tr><tr><td>

Token

</td><td>

Authentication token for the Tanium API that grants access to the Tanium data \(see [Create an API token](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-tanium-endpoints-create-api-token.md)\).

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use a MID Server.**Note:** Use of a MID Server is optional.

</td></tr><tr><td>

MID selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID Server** check box is selected.

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  After the test completes, select **Continue**.

6.  Configure additional sensors.

    You can configure additional sensors from the list of available sensors in the SG-Tanium-Endpoints Sensors table. To skip this step, select **Skip**.

    For information about Tanium sensors, see [What is a sensor?](https://help.tanium.com/bundle/ug_console_cloud/page/platform_user/interact_questions.html#What_is_a_Sensor), [Managing sensors for collecting endpoint data](https://help.tanium.com/bundle/ug_console_cloud/page/platform_user/authoring_sensors.html), and [Example: Multi-column sensors](https://help.tanium.com/bundle/ug_console_cloud/page/platform_user/authoring_example_multicolumn_sensor.html).

    1.  In the **Setup** stage, select **Configure additional sensors**.

    2.  Select **Fetch sensors** to populate the SG-Tanium-Endpoints Sensors table with the list of available additional sensors.

    3.  Set the **Ingest** field to `true` for the sensors from which data is to be imported.

    4.  Specify the data format in the **Type** field.

        -   **Single line**: For sensors that return one record per device—a simple set of attribute-value pairs, with no nested objects or lists.

            Example:

            ```
            JSON
            {"ip_address": "192.168.1.100"}
            ```

        -   **Multiline**: For sensors that return multiple records per device—each record contains attribute-value pairs, which are returned as an array of objects.

            Example:

            ```
            JSON
            {
              "AssetNetworkAdaptor":[
                  {"name": "eth0", "IPv4Address": "192.168.1.100"},
                  {"name": "eth1", "IPv4Address": "10.0.0.50"}
                ]
             }
            ```

        **Note:** The normalized sensor name \(in the **SG-Tanium-Endpoints Sensors** table\) is used to look up the sensor's data in the endpoint JSON payload. This name is derived from the sensor name by removing whitespaces and replacing special characters with underscores. Use this value when configuring Robust Transform Engine \(RTE\) mappings or for any downstream lookup that references the sensor by its JSON key.

    5.  Select **Mark as complete**.

7.  Configure the import schedule.

    1.  In the **Setup** stage, select **Configure import schedule**.

    2.  Select the import schedule for your connection, set it to **Active**, and then fill in the run schedule details.

    3.  If you configured additional sensors in step [6](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown), run the scheduled data import to view the sensor details in the import set table and complete the RTE mapping.

    4.  Select **Save**, and then select **Continue**.

8.  Select **Confirm connection creation** to verify the connection.


## What to do next

Select **View all connections** to review the connection details.

You can manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-managing-connection.md).

