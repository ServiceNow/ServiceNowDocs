---
title: Configure Service Graph Connector for Observability - Dynatrace using SGC Central
description: Set up scheduled import jobs to pull in Dynatrace data into your Configuration Management Database \(CMDB\).
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 7
breadcrumb: [Observability-Dynatrace, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Observability - Dynatrace using SGC Central

Set up scheduled import jobs to pull in Dynatrace data into your Configuration Management Database \(CMDB\).

## Before you begin

Install Service Graph Connector for Observability - Dynatrace version 1.11.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../../configuration-management/image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Dynatrace connector type, and then select **Configure connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    1.  Install the Observability Commons for CMDB application \(sn\_observability\) for event ingestion.

        **Note:** The **Install Observability Commons for CMDB** activity appears only when the Observability Commons for CMDB application \(sn\_observability\) isn't already installed. If event ingestion isn't needed, you can skip this step by selecting **Continue** for the **Install Observability Commons for CMDB** activity.

        1.  In the **Prerequisites** stage of the playbook, select the **Install Observability Commons for CMDB** activity.
        2.  Install the [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) application \(sn\_observability\) from the ServiceNow Store.
        3.  After you have installed the application, select **Continue**.
    2.  Create data sources for the connection.

        **Note:** This step is required when configuring the connector for the first time only.

        1.  Verify that you have edit permissions for the Datasource \[sys\_data\_source\] table.
        2.  In the **Prerequisites** stage of the playbook, select the **Update data source access** activity.
        3.  Select **Update access**.
        4.  To edit the record, select the **Global** application scope from the application picker.
        5.  In the Application Access related list of the Data Source form, select the **Can create**, **Can update**, and **Can delete** check boxes.
        6.  Select **Update**.
        7.  From the application picker, select the application scope of the connector.
        8.  After completing the **Update data source access** activity, select **Continue**.
    3.  Enable creating scheduled jobs for the connection by updating the scheduled data import access.

        **Note:** This step is required when configuring the connector for the first time only.

        1.  Verify that you have edit permissions for the Scheduled Data Import \[scheduled\_import\_set\] table.
        2.  In the **Prerequisites** stage of the playbook, select the **Update scheduled data import access** activity.
        3.  Select **Update access**.
        4.  To edit the record, select the **Global** application scope from the application picker.
        5.  In the Application Access related list of the Data Source form, select the **Can create**, **Can update**, and **Can delete** check boxes.
        6.  Select **Update**.
        7.  From the application picker, select the application scope of the connector.
        8.  After completing the **Update scheduled data import access** activity, select **Continue**.
    4.  Enable creating values for the connection by updating the variable value access.

        **Note:** This step is required when configuring the connector for the first time only.

        1.  Verify that you have edit permissions for the Value \[sys\_variable\_value\] table.
        2.  In the **Prerequisites** stage of the playbook, select the **Update variable value access** activity.
        3.  Select **Update access**.
        4.  To edit the record, select the **Global** application scope from the application picker.
        5.  In the Application Access related list of the Data Source form, select the **Can create**, **Can update**, and **Can delete** check boxes.
        6.  Select **Update**.
        7.  From the application picker, select the application scope of the connector.
        8.  After completing the **Update variable value access** activity, select **Continue**.
    5.  Clear the cache on the Data Source \[sys\_data\_source\] table.

        **Note:** This step is required when configuring the connector for the first time only.

        1.  In the **Prerequisites** stage of the playbook, select the **Clear cache** activity.
        2.  Select **Run clear cache**.
        3.  In the **Run script** text box of the background script page, enter the following script:

            ```
            GlideTableManager.invalidateTable("sys_data_source");
                  GlideCacheManager.flushTable("sys_data_source");
            
                  GlideTableManager.invalidateTable("scheduled_import_set");
                  GlideCacheManager.flushTable("scheduled_import_set");
            
                  GlideTableManager.invalidateTable("sys_variable_value");
                  GlideCacheManager.flushTable("sys_variable_value");
            
                  GlideTableManager.invalidateTable("sys_db_object");
                  GlideCacheManager.flushTable("sys_db_object");
            ```

        4.  Select **Run Script** to run the background script in the **global** scope.

            The script may take several minutes to execute.

        5.  After the script is executed, select **Close**.
        6.  From the application picker, select the application scope of the connector.
        7.  After completing the **Clear cache** activity, select **Continue**.
    6.  Verify that the Event Management application works properly with the Dynatrace environment by copying the `EvtMgmtImpactManagerMediator` script to the Global application scope.

        **Note:** This step is displayed only when the Observability Commons for CMDB plugin \(sn\_observability\) is already installed and is required when configuring the connector for the first time only.

        1.  In the **Prerequisites** stage of the playbook, select the **Enable script access for event management** activity.
        2.  Select **Enable script access**.
        3.  Select the **Global** application scope from the application picker.
        4.  From the context menu, select **Insert and Stay**.
        5.  Verify that the `EvtMgmtlmpactManagerMediator` script was copied to the Global application scope and the **Accessible from** field was set to `All application scopes`.
        6.  Select **Update**.
        7.  From the application picker, select the application scope of the connector.
        8.  After completing the **Enable script access for event management** activity, select **Continue**.
5.  Enter connection details and test the API connection for importing Dynatrace data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_ahn_xtg_rmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Dynatrace connection record.

</td></tr><tr><td>

Hostname

</td><td>

Hostname of your Dynatrace environment.

</td></tr><tr><td>

API Key

</td><td>

Dynatrace API Key.**Note:** The API Key must be prefixed with `api-token`.

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

6.  Configure the connection and connector properties to map attributes and manage data imports.

    **Note:** To skip this step, select **Continue** for the **Set configuration properties** activity.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  Fill in the form.

<table id="table_orp_332_4yb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Management zone Ids

</td><td>

List of the management zone IDs to fetch from your Dynatrace environment. For multiple entries, separate the zone IDs with commas.

</td></tr><tr><td>

Management zone names

</td><td>

List of the management zones to fetch from your Dynatrace environment. For multiple entries, separate the zone names with commas.

</td></tr><tr><td>

Service types

</td><td>

List of the Dynatrace service types from where to ingest the data into the CMDB. For multiple entries, separate the service types with commas.**Note:** All service types except for DATABASE\_SERVICE are mapped to the Calculated Application Service \[cmdb\_ci\_service\_calculated\] CMDB table. The DATABASE\_SERVICE service type is mapped to the Database Instance \[cmdb\_ci\_db\_instance\] CMDB table.

Valid values are:

-   BACKGROUND\_ACTIVITY
-   CICS\_SERVICE
-   CUSTOM\_SERVICE
-   DATABASE\_SERVICE
-   ENTERPRISE\_SERVICE\_BUS\_SERVICE
-   EXTERNAL
-   IBM\_INTEGRATION\_BUS\_SERVICE
-   IMS\_SERVICE
-   MESSAGING\_SERVICE
-   QUEUE\_LISTENER\_SERVICE
-   RMI\_SERVICE
-   RPC\_SERVICE
-   WEB\_REQUEST\_SERVICE
-   WEB\_SERVICE


</td></tr><tr><td>

Tags

</td><td>

List of the tag names to fetch from your Dynatrace environment. For multiple entries, separate the tags with commas.

</td></tr></tbody>
</table>    3.  To manage data source failures during import, select the **Save REST response as attachment** check box to save each response as an attachment temporarily.

    4.  Select **Continue**.

7.  To enable Dynatrace notifications as events in your ServiceNow instance, trigger the workflow to create a problem notification and alerting profile in your Dynatrace environment.

    **Note:** This step is displayed only when the Observability Commons for CMDB plugin \(sn\_observability\) is already installed. To skip this step, select **Skip** for the **Configure observability** activity.

    1.  In the **Setup** stage of the playbook, select the **Configure observability** activity.

    2.  Select **Create problem notification**.

        **Note:** The created records appear in the Dynatrace application under the display name `ServiceNow default Problem notification` and can be customized.

    3.  Dismiss any success alerts and select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **SGO-Dynatrace Hosts - _Connection Name_** import schedule.

    3.  Select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Observability - Dynatrace](../../configuration-management/concept/cmdb-integration-dynatrace.md)

[CMDB classes targeted in Service Graph Connector for Observability - Dynatrace](../../configuration-management/reference/cmdb-dynatrace-classes.md)

[Service Graph Connector for Observability - Dynatrace properties](../../configuration-management/reference/sgc-cmdb-dynatrace-props.md)

