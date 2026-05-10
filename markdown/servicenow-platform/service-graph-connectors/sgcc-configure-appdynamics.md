---
title: Configure Service Graph Connector for Observability - AppDynamics using SGC Central
description: Set up scheduled import jobs to pull in AppDynamics data into your Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Observability-AppDynamics, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Observability - AppDynamics using SGC Central

Set up scheduled import jobs to pull in AppDynamics data into your Configuration Management Database \(CMDB\).

## Before you begin

-   Install Service Graph Connector for Observability - AppDynamics version 1.4.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/installing-applications-in-application-manager.md).
-   Install Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This application must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/playbook-ui.md).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the AppDynamics connector type, and then select **Configure connection**.

    A default connection for AppDynamics is available within the application. As the Service Graph Connector for Observability - AppDynamics supports only a single instance, you can configure the default connection for the first time or resume editing it thereafter.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Enter connection details and test the API connection for importing AppDynamics data.

    1.  In the **Setup** stage of the playbook, select the **Configure and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_z4n_2tt_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the AppDynamics connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL of your AppDynamics controller.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your AppDynamics client application.**Note:** Verify that Server Visibility is active for the AppDynamics account and the AppDynamics user has the Applications and Dashboards Viewer \(Default\) and Server Monitoring User \(Default\) roles.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret of your AppDynamics client application.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server.**Note:** Use of a MID Server is optional.

</td></tr><tr><td>

MID selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID server** check box is selected.

</td></tr></tbody>
</table>    3.  Select **Update and test connection**.

    4.  Once the connection test is complete, select **Continue**.

6.  Enable real-time event integration by creating an HTTP request template to receive real-time health-check alerts and events from AppDynamics to your ServiceNow instance.

    **Note:** To skip this step, select **Skip** for the **Enable real-time event integration** activity.

    1.  In the **Setup** stage of the playbook, select the **Enable real-time event integration** activity.

    2.  Select **Continue** to create an HTTP request template automatically.

        After you enable real-time event integration, multiple API calls are executed to start the event ingestion service in AppDynamics. For more information, see the [Service Graph Connector for Observability AppDynamics](https://www.servicenow.com/community/cmdb-blog/service-graph-connector-for-observability-appdynamics/ba-p/2275530) article on the ServiceNow Community site.

7.  Configure duplicate detection rules.

    AppDynamics uses duplicate detection rules to insert only new or updated rows into the CMDB. To insert all rows, deactivate the rule and run the **Clean AppDynamics Duplicate Row Hashes** scheduled job for a full data import.

    1.  In the **Setup** stage of the playbook, select the **Configure duplicate detection rules** activity.

    2.  In the Duplicate detection rules list, select the rule from the **Name** column.

    3.  On the Edit duplicate detection rule window, select the **Active** check box to activate the rule.

        **Note:** To remove fields from being evaluated, add the field names in the **Ignore Fields** field for a rule. To ignore multiple fields, separate the fields with commas.

    4.  Select **Save**.

    5.  Repeat steps from [7.b](sgcc-configure-appdynamics.md#rule-select) to [7.d](sgcc-configure-appdynamics.md#rule-save) for each rule you want to activate.

    6.  Select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **SG-AppDynamics Servers and Applications** import schedule.

    3.  Select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/system-import-sets/t_ScheduleADataImport.md#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was configured.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Observability - AppDynamics](../../configuration-management/concept/cmdb-integration-appdynamics.md)

[CMDB classes targeted in Service Graph Connector for Observability - AppDynamics](../../configuration-management/reference/cmdb-appdynamics-classes.md)

[Accessing the connection details for Service Graph Connector for Observability - AppDynamics](../../configuration-management/concept/sgc-appdynamics-conn.md#)

