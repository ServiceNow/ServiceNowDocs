---
title: Configure Service Graph Connector for Wiz using SGC Central
description: Set up scheduled import jobs to pull in data from a Wiz project into your Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Wiz, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Wiz using SGC Central

Set up scheduled import jobs to pull in data from a Wiz project into your Configuration Management Database \(CMDB\).

## Before you begin

-   Install Service Graph Connector for Wiz version 1.3.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   You must obtain the OAuth credentials associated with the Wiz service account and make a note of the following details:

    -   Client ID
    -   Client secret
    -   OAuth token URL
    -   Connection URL
    For more information, see [Set up the Wiz environment](../../configuration-management/task/sgc-cmdb-wiz-setup.md).

-   You must have the following permissions for the Wiz service account:
    -   read:resources
    -   read:projects

Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|cmdb\_inst\_admin or admin|

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon ![](../image/icon-sgc-central.png) to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Wiz connector type, and then select **Configure connection**.

    A default connection, SG-Wiz, for Wiz is available within the application. As the Service Graph Connector for Wiz supports only a single instance, you can configure the default connection for the first time or resume editing it thereafter.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required when configuring the connector for the first time only. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Enter connection details and test the API connection for importing Wiz data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_ahn_xtg_rmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Wiz connection record.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to your Wiz application. **Note:** Based on the region of your Wiz application, enter the connection URL in the following format:

```
https://api.*&lt;region&gt;*.app.wiz.io
```

Where *&lt;region&gt;* is the region where the Wiz tenant is located. For example, us1, us2, eu1, or eu2.

</td></tr><tr><td>

Client ID

</td><td>

Client ID of your Wiz application as described in [Before you begin](sgcc-configure-wiz.md#task-prereq).

</td></tr><tr><td>

Client secret

</td><td>

Client secret of your Wiz application as described in [Before you begin](sgcc-configure-wiz.md#task-prereq).

</td></tr><tr><td>

OAuth token URL

</td><td>

Token generation URL. This field is automatically set to the following URL:```
https://auth.app.wiz.io/oauth/token
```

</td></tr></tbody>
</table>    3.  Select **Update and test connection**.

    4.  Once the connection test is complete, select **Continue**.

6.  Configure properties of the connector to access resources.

    **Note:** To skip this step, select **Continue** for the **Set configuration properties** activity.

    1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.

    2.  On the form, fill in the fields.

<table><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Projects

</td><td>

List of project IDs for which the resources are to be imported.Separate multiple entries with a comma.

</td></tr><tr><td>

Exclude projects

</td><td>

List of project IDs for which the resources are excluded only when the **Projects** property isn’t set. In this case, all the resources except for the specified projects are imported.Separate multiple entries with a comma.

</td></tr></tbody>
</table>    3.  Select **Continue**.

7.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **SG-Wiz-Organization** import schedule.

    3.  Select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

8.  Enable the `Reset Last Run Datetime for SG-Wiz` script to retrieve full data periodically.

    **Note:** To skip this step, select **Skip** for the **Enable full data retrieval** activity.

    1.  In the **Setup** stage of the playbook, select the **Enable full data retrieval** activity.

    2.  Select the **Active** check box, and then fill in the run schedule and time details.

        **Note:** When active, the script clears the **Last Run Date Time** field value in a data source, ensuring that the SG-Wiz Organization scheduled job retrieves all Wiz-related data sources periodically.

    3.  Select **Continue**.

9.  In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The created connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Wiz](../../configuration-management/concept/sgc-cmdb-integration-wiz.md)

[Target tables for storing Service Graph Connector for Wiz data](../../configuration-management/reference/sgc-cmdb-wiz-classes.md)

[Service Graph Connector for Wiz properties](../../configuration-management/reference/sgc-cmdb-wiz-props.md)

[Supported Wiz types](../../configuration-management/reference/sgc-cmdb-wiz-types.md)

[Accessing the connection details of Service Graph Connector for Wiz](../../configuration-management/concept/sgc-cmdb-wiz-conn.md#)

