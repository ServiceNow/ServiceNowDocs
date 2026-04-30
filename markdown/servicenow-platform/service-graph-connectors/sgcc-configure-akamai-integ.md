---
title: Configure Service Graph Connector for Akamai API Security using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for Akamai API Security for pulling in Akamai API Security data into the CMDB.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-06"
reading_time_minutes: 4
breadcrumb: [Akamai API Security, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Akamai API Security using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for Akamai API Security for pulling in Akamai API Security data into the CMDB.

## Before you begin

-   Install Service Graph Connector for Akamai API Security version 1.0.0 from the ServiceNow Store.

    For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).

-   Create a service account on the Akamai platform and generate client credentials to enable data retrieval using the Service Graph Connector for Akamai API Security.

    The Akamai API Security platform supports client credentials-based authentication. Client credentials are required to authenticate and securely access API data​.


Role required: The following table shows the roles required for each stage of the playbook.

|Stage|Role|
|-----|----|
|Prerequisites|admin|
|Setup|SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin|

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../../configuration-management/concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## About this task

The playbook experience for onboarding connectors is activated with SGC Central in the Service Graph Workspace or CMDB Workspace. To configure the SGC Central application, see [Configuring SGC Central](../concept/sgcc-configuring.md) and for more information on how to interact with a playbook, see [Interact with Playbook](https://www.servicenow.com/docs/access?context=playbook-ui&version=zurich&pubname=zurich-build-workflows&ft:locale=en-US).

## Procedure

1.  Use one of the following methods to open SGC Central:

    -   Navigate to **Workspaces** &gt; **Service Graph Workspace**, and from the left navigation panel, select the Ingestion icon to open the SGC Central view.
    -   Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.
2.  On the Overview page, select **Create connection**.

    **Tip:** Alternatively, you can select **Create connection** on the All connections page.

3.  On the Create connection window, select the Akamai connector type, and then select **Create connection**.

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

Akamai Connection Name

</td><td>

Name to identify the Akamai connection record.For example, `Akamai`.

</td></tr><tr><td>

Connection URL

</td><td>

URL of the connection.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your Akamai client application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret of your Akamai client application.

</td></tr><tr><td>

OAuth Token URL

</td><td>

Token URL of your Akamai client application.

</td></tr></tbody>
</table>        3.  Select **Create and test connection**.
        4.  After the connection test is complete, select **Continue**.
    2.  Set the configuration properties to import tags and to configure source-based filtering.

        1.  In the **Setup** stage of the playbook, select the **Set configuration properties** activity.
        2.  \(Optional\) In the **Data retrieval configuration** section, specify the **Source name** or **Source alias** as a comma-separated list to fetch API Component data from specific sources or gateways, respectively.

            **Note:** When a value is specified or updated in the **Source name** or **Source alias** field, the last\_run\_datetime field for SG-Akamai data sources is reset. This triggers full data ingestion during the next scheduled import. Subsequent runs perform delta loads based on the configured filters.

        3.  In the **Tags settings** section, select the **Import tags** check box to import tags for the records.
        4.  In the **Tags value separator** field, specify `=` as the key-value pair separator.
        5.  Select **Continue**.
    3.  Configure the import schedule to import data at regular intervals.

        1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.
        2.  Expand the Parent scheduled data import within the Import schedules list, and select the Sources import schedule.
        3.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select **Save**.

            Alternatively, select **Execute Now** to execute the import schedule immediately.

        5.  Select **Continue**.
    4.  In the **Setup** stage of the playbook, select the **Confirm connection setup** activity to verify whether the connection was created.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Akamai API Security](../../configuration-management/concept/sgc-integration-akamai.md)

[CMDB classes targeted in Service Graph Connector for Akamai API Security](../../configuration-management/reference/cmdb-akamai-classes.md)

