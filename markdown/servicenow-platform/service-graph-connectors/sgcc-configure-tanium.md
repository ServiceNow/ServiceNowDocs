---
title: Configure Service Graph Connector for Tanium using SGC Central
description: Set up scheduled import jobs to pull in Tanium data into your Configuration Management Database \(CMDB\).
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 4
breadcrumb: [Tanium, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Tanium using SGC Central

Set up scheduled import jobs to pull in Tanium data into your Configuration Management Database \(CMDB\).

## Before you begin

Install Service Graph Connector for Tanium version 1.7.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

Role required: admin

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **CMDB Workspace**.

2.  In the CMDB Workspace, select **SGC Central**.

3.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

4.  On the Create connection window, select the Tanium connector type, and then select **Create connection**.

5.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

6.  Complete the prerequisites for setting up the Tanium environment.

    1.  Create a custom view on your Tanium instance.

        1.  In the **Prerequisites** stage of the playbook, select the **Create custom view** activity.
        2.  Create a custom view on your Tanium instance to be used in the **Select view** activity later by referring to the [Tanium Asset User Guide for Cloud](https://help.tanium.com/bundle/ug_asset_cloud/page/asset/exportasset.html#servicenow_app).

            **Note:** Copy the unmodifiable **ServiceNow \(reserved\)** view from the Tanium instance to create the custom view.

        3.  After creating a view, select the **I have created a custom view for this connection according to the instructions** check box.
        4.  After completing the **Select view** activity, select **Continue**.
7.  Determine the type of authentication for the Tanium connection.

    1.  In the **Setup** stage of the playbook, select the **Select alias template** activity.

        If needed, expand the **Setup** stage to select an activity.

    2.  Select an alias template for the connection.

        -   **Basic authentication**: Select when using Basic authentication that grants access to the Tanium data.
        -   **Token-based authentication**: Select when using an authentication token for the Tanium API to grants access to the Tanium data.
    3.  Select **Continue**.

8.  Enter connection details and test the API connection for importing Tanium data.

    1.  In the **Setup** stage of the playbook, select the **Configure and test connection** activity.

    2.  On the form, fill in the fields.

<table id="table_ahn_xtg_rmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Tanium connection record.

</td></tr><tr><td>

Host name

</td><td>

Base URL or IP address of the Tanium server.

</td></tr><tr><td>

Username

</td><td>

Tanium account user name that is used to authenticate the connection request.This field appears only when the **Basic authentication** alias template was selected in the **Select alias template** activity.

</td></tr><tr><td>

Password

</td><td>

Password associated with the user name required for authenticating requests.This field appears only when the **Basic authentication** alias template was selected in the **Select alias template** activity.

</td></tr><tr><td>

Token

</td><td>

Authentication token for the Tanium API that grants access to the Tanium data.This field appears only when the **Token-based authentication** alias template was selected in the **Select alias template** activity.

</td></tr><tr><td>

Use MID Server

</td><td>

Option to use a MID Server.**Note:** Use of a MID Server is optional.

</td></tr><tr><td>

MID selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID Server** check box is selected.

</td></tr></tbody>
</table>    3.  Select **Update and test connection**.

    4.  Once the connection test is complete, select **Continue**.

9.  Select the view created on your Tanium instance.

    1.  In the **Setup** stage of the playbook, select the **Select view** activity.

    2.  In the **View** field, select the custom view you created on the Tanium instance in the [Prerequisites activity](sgcc-configure-tanium.md#prereq-activity).

    3.  Select **Continue**.

10. Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Expand the Parent scheduled data import within the Import schedules list to select the **_Connection name_ - SG-Tanium Usage** import schedule.

    3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    5.  Repeat steps [10.b](sgcc-configure-tanium.md#parent) to [10.d](sgcc-configure-tanium.md#save) for the **_Connection name_ - SG-Tanium Hardware and Software** parent import schedule.

    6.  Select **Continue**.

11. In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Tanium](../../configuration-management/concept/cmdb-integration-tanium.md)

[CMDB classes targeted in Service Graph Connector for Tanium](../../configuration-management/reference/cmdb-tanium-classes.md)

[Accessing the connection details of Service Graph Connector for Tanium](../../configuration-management/concept/sgc-tanium-conn.md#)

