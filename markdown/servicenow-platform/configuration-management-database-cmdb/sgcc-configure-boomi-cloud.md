---
title: Configure API Service Graph Connector for Boomi Cloud API Management using SGC Central
description: Set up scheduled import jobs to pull in Boomi Cloud API Management data into your CMDB.
locale: en-US
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Boomi Cloud API Management, API Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure API Service Graph Connector for Boomi Cloud API Management using SGC Central

Set up scheduled import jobs to pull in Boomi Cloud API Management data into your CMDB.

## Before you begin

Install API Service Graph Connector for Boomi Cloud API Management version 1.0.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US).

Obtain the API credentials from your Boomi Cloud API Management administrator. Make a note of the following details:

-   Client ID: The unique identifier for your Boomi Cloud API Management application.
-   Client Secret: The secret key for authenticating your Boomi Cloud API Management application.
-   Area ID: The Boomi area identifier from which data is imported.
-   Area Name: The Boomi area name for your instance.

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

**Note:** Alternatively, you can configure a default connection already available from the installed or draft connections in SGC Central. Go to **All** &gt; **Service Graph Connectors**, then select **Setup** for the connector from the menu. To learn about installed and draft connections, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the Boomi connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

6.  Enter connection details and test the API connection for importing Boomi Cloud API Management data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_l2g_zn4_nyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Boomi connection record.For example, `Boomi connection`.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the Boomi Cloud API Management service.**Note:** This field is automatically set to the URL to connect to the application. Leave the field value as is.

</td></tr><tr><td>

OAuth client ID

</td><td>

Client ID of your Boomi Cloud API Management application as noted in the [Before you begin](sgcc-configure-boomi-cloud.md#prereq) section.

</td></tr><tr><td>

OAuth Client secret

</td><td>

Client secret of the Boomi Cloud API Management application as noted in the [Before you begin](sgcc-configure-boomi-cloud.md#prereq) section.

</td></tr><tr><td>

Area ID

</td><td>

Boomi area identifier from which data is imported as noted in the [Before you begin](sgcc-configure-boomi-cloud.md#prereq) section.

</td></tr></tbody>
</table>    3.  Select **Create and test connection**.

    4.  Once the connection test is complete, select **Continue**.

7.  Set the configuration properties for the connection.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  In the **Area Name** field, enter the area name for your **Boomi** instance as noted in the [Before you begin](sgcc-configure-boomi-cloud.md#prereq) section.

    3.  Select **Continue**.

8.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **APIs** import schedule associated with your connection.

        **Note:** The connection name is prefixed to the schedule name.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=yokohama&pubname=yokohama-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

You can then manage connections from the SGC Central view of the CMDB Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](../concept/sgcc-managing-connection.md).

