---
title: Configure API Service Graph Connector for Kong Konnect using SGC Central
description: Set up scheduled import jobs to pull in Kong Konnect data into your CMDB.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Kong Konnect, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure API Service Graph Connector for Kong Konnect using SGC Central

Set up scheduled import jobs to pull in Kong Konnect data into your CMDB.

## Before you begin

Install API Service Graph Connector for Kong Konnect version 1.0.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/installing-applications-in-application-manager.md).

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-ui.md).

**Note:** Alternatively, you can configure a default connection already available from the installed or draft connections in SGC Central. Go to **All** &gt; **Service Graph Connectors**, then select **Setup** for the connector from the menu. To learn about installed and draft connections, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the Kong Konnect connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

6.  Enter connection details and test the API connection for importing Kong Konnect data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_l2g_zn4_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Kong Konnect connection record.For example, `Kong Konnect connection`.

</td></tr><tr><td>

Personal access token

</td><td>

Token used to securely authenticate your identity and authorize access to your Kong Konnect account via the API

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

7.  Set the configuration properties for the connection.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  Fill in the property details.

<table id="table_nn3_31v_3cc"><thead><tr><th>

Property

</th><th>

Description

</th></tr><tr><th class="sub-head" colspan="2">

Data retrieval configuration

</th></tr></thead><tbody><tr><td>

Gateway group IDs

</td><td>

Group IDs associated with a Kong Konnect gateway representing control plane groups consisting of self-managed control planes.For multiple IDs, separate them with commas.

**Note:** The **Gateway group IDs** property is used if specified, and it overrides the Gateway IDs.

</td></tr><tr><td>

Gateway IDs

</td><td>

IDs of individual Kong Konnect gateways, each representing a control plane.For multiple IDs, separate them with commas.

**Note:** The **Gateway IDs** property value is ignored if Gateway group IDs are specified.

</td></tr><tr><td>

Regions

</td><td>

List of comma-separated regions where the Kong Konnect gateway resides.

</td></tr><tr><td>

Expand HTTP method types

</td><td>

HTTP methods including `GET`, `POST`, `PUT`, `PATCH`, `DELETE`, `OPTIONS`, `HEAD`, `CONNECT`, and `TRACE`, to consider for routes.For multiple methods, separate them with commas. If left blank, results in a single API Frontend being created with the `ALL` method, indicating support for all standard HTTP methods.

</td></tr><tr><td>

Collect usage data

</td><td>

Enable usage data collection to retrieve API usage data over a specified duration.

</td></tr><tr><td>

Collection period duration

</td><td>

Duration for collecting API usage data. Valid values include:

-   `15m` \(Last 15 minutes\)
-   `1h` \(Last 1 hour\)
-   `6h` \(Last 6 hours\)
-   `12h` \(Last 12 hours\)
-   `24h` \(Last 24 hours\)
-   `7d` \(Last 7 days\)
-   `30d` \(Last 30 days\)
-   `current_week` \(Current week\)
-   `previous_week` \(Previous week\)
-   `current_month` \(Current month\)
-   `previous_month` \(Previous month\)


</td></tr><tr><td class="sub-head" colspan="2">

Performance configuration

</td></tr><tr><td>

Page size

</td><td>

Number of records per page. Default is `100`.

</td></tr><tr><td>

Partition size

</td><td>

Partition size for Kong Konnect managed APIs if parallel loading is enabled.Accepts a numeric value greater than zero. If left empty, the value is automatically calculated.

**Note:** Parallel loading is available for the following data sources only:

-   Routes
-   Target


</td></tr><tr><td class="sub-head" colspan="2">

Tags settings

</td></tr><tr><td>

Import tags

</td><td>

Option to ingest tags from the Kong Konnect gateway.

</td></tr><tr><td>

Tags value separator

</td><td>

Separator for key and value in tags.

</td></tr></tbody>
</table>    3.  Select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **Gateway** import schedule associated with your connection.

        **Note:** The connection name is prefixed to the schedule name.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

You can then manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

**Related topics**  


[API Service Graph Connector for Kong Konnect](../../configuration-management/concept/api-sgc-kong-konnect.md)

[Target tables for storing API Service Graph Connector for Kong Konnect data](../../configuration-management/reference/api-sgc-kong-konnect-tables.md)

