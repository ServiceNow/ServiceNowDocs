---
title: Configure Service Graph Connector for Trellix using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for Trellix for pulling in Trellix data into the CMDB.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 3
breadcrumb: [Trellix, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Trellix using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for Trellix for pulling in Trellix data into the CMDB.

## Before you begin

Install Service Graph Connector for Trellix version 1.0.0 from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

Role required: admin

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Dashboard page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Trellix connector type, and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Complete the setup for configuring the connector for importing data.

    1.  Create and test a connection.

        1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.
        2.  On the form, fill in the fields.

<table id="table_cnv_sn5_lfc"><thead><tr><th>

Field

</th><th>

 

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Trellix connection record.For example, `SGTrellix`.

</td></tr><tr><td>

Connection url

</td><td>

URL of the connection.

</td></tr><tr><td>

User name

</td><td>

User name of your Trellix account.

</td></tr><tr><td>

Password

</td><td>

Password of your Trellix account.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server. Select this check box if you’re using an on-premises instance of Trellix.**Note:** A MID Server must be configured on your ServiceNow instance before you select this option.

</td></tr><tr><td>

Mid Selection

</td><td>

Name of the MID Server used by the connector.This field appears only when the **Use MID Server** check box is selected.

</td></tr></tbody>
</table>        3.  Select **Create and test connection**.
        4.  Once the connection test is complete, select **Continue**.
    2.  Configure the import schedule to import data at regular intervals.

        1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.
        2.  Expand the Parent scheduled data import within the Import schedules list, and select the SG-Trellix-Devices import schedule.
        3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Save**.

            Alternatively, select **Execute Now** to execute the import schedule immediately.

        5.  Select **Continue**.
    3.  In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Trellix](../../configuration-management/concept/sgc-integration-trellix.md)

[CMDB classes targeted in Service Graph Connector for Trellix](../../configuration-management/reference/cmdb-trellix-classes.md)

[Accessing the connection details of Service Graph Connector for Trellix](../../configuration-management/concept/sgc-trellix-conn.md#)

