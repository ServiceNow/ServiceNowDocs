---
title: Configure Service Graph Connector for Infoblox using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for Infoblox for pulling in Infoblox data into the CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Infoblox, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Infoblox using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for Infoblox for pulling in Infoblox data into the CMDB.

## Before you begin

Install Service Graph Connector for Infoblox version 1.2.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=installing-applications-in-application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Infoblox connector type and then select **Configure connection**.

    A default connection, SG\_Infoblox\_Connection, for Infoblox is available within the application. As the Service Graph Connector for Infoblox supports only a single instance, you can configure the default connection for the first time or resume editing it thereafter.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Enter connection details and test the API connection for importing Infoblox data.

    1.  In the **Setup** stage of the playbook, select the **Configure and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_ahn_xtg_rmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Infoblox connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Infoblox base URL in the following format: `*&lt;base-URL&gt;*`.

</td></tr><tr><td>

User name

</td><td>

User name for authenticating the HTTP request.

</td></tr><tr><td>

Password

</td><td>

Password for the user name used for authenticating the HTTP request.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use the MID Server for connecting to the Infoblox instance.**Note:** A MID Server is required only if a direct connection between the ServiceNow and Infoblox instances isn’t possible.

</td></tr><tr><td>

Mid Selection

</td><td>

MID Server for the connection.This field appears only when you select the **Use MID Server** check box.

</td></tr></tbody>
</table>    3.  Select **Update and test connection**.

    4.  Once the connection test is complete, select **Continue**.

6.  Specify network views and the API version for connecting to the Infoblox instance by setting the configuration properties.

    **Note:** To skip this step, select **Continue** for the **Set configuration properties** activity. If you skip this step, the default values of the **Network view** and **API version** properties are considered.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  In the **Network view** field, enter the network views for which data is to be imported.

        For multiple views, separate them with commas. For example: `view1,view2`.

        If you leave this field empty or set it to `Default`, the data sources within the connector import data from all the network views.

    3.  In the **API version** field, enter the [version of WAPI](https://ipam.illinois.edu/wapidoc/) you’re using.

        For more information about the Infoblox API, see the [Infoblox Developer documentation](https://www.infoblox.com/wp-content/uploads/infoblox-deployment-infoblox-rest-api.pdf).

    4.  Select **Save properties**.

    5.  Select **Continue**.

7.  Opt for task creation on network insertion or deletion.

    **Note:** To skip this step, select **Continue** for the **Configure task preferences** activity.

    1.  In the **Setup** stage of the playbook, select the **Configure task preferences** activity.

    2.  Select the **Create task on network insertion** check box to enable creating a task when a network is inserted.

    3.  Select the **Create task on network deletion** to enable creating a task when a network is deleted.

    4.  In the Task user group list, select the user group assigned to tasks created on network insertion or deletion.

    5.  Select **Save preferences**.

    6.  Select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Select **Configure import schedule**.

    3.  Expand the Parent scheduled data import within the Import schedules list to select the **SG-Infoblox IP Pool** import schedule.

    4.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    6.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Infoblox](../../configuration-management/concept/sgc-cmdb-integration-infoblox.md)

[CMDB classes targeted in Service Graph Connector for Infoblox](../../configuration-management/reference/sgc-cmdb-infoblox-classes.md)

[Accessing the connection details of Service Graph Connector for Infoblox](../../configuration-management/concept/sgc-cmdb-infoblox-conn.md#)

