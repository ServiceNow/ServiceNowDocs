---
title: Configure Service Graph Connector for Observability - Dynatrace SaaS using SGC Central
description: Use the playbook in SGC Central to set up the Service Graph Connector for Observability - Dynatrace SaaS and pull Dynatrace data into your CMDB.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/sgcc-configure-dynatrace-saas.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-06-03"
reading_time_minutes: 3
breadcrumb: [Observability - Dynatrace SaaS, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Observability - Dynatrace SaaS using SGC Central

Use the playbook in SGC Central to set up the Service Graph Connector for Observability - Dynatrace SaaS and pull Dynatrace data into your CMDB.

## Before you begin

**Important:** The Service Graph Connector for Observability - Dynatrace SaaS is designed for the Dynatrace SaaS \(3rd‑generation\) platform and leverages DQL-based APIs and the Grail architecture to import data from Dynatrace into the CMDB. If you're in a Dynatrace managed \(self‑hosted\) or legacy SaaS environment, you should use the Service Graph Connector for Observability - Dynatrace.

Install Service Graph Connector for Observability - Dynatrace SaaS from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/installing-applications-in-application-manager.md).

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

3.  On the Create connection window, select the Dynatrace SaaS connector type, and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-first-time-setup.md).

5.  Enter connection details and test the connection for importing Dynatrace data.

    1.  In the **Setup** stage, select **Create and test connection**.

    2.  On the form, fill in the fields.

<table id="table_kr2_ngj_njc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Dynatrace SaaS connection record.

</td></tr><tr><td>

Hostname

</td><td>

Host name of your Dynatrace environment \(`*Dynatrace-tenant*.apps.dynatrace.com`\).

</td></tr><tr><td>

Platform Token

</td><td>

Dynatrace platform token \(see [Platform tokens](https://docs.dynatrace.com/docs/manage/identity-access-management/access-tokens-and-oauth-clients/platform-tokens)\).**Note:** The platform token must not be prefixed with `Bearer`.

</td></tr></tbody>
</table>        **Note:** The following permissions are required for the platform token:

        ```
        storage:entities:read
        storage:smartscape:read
        ```

        For more information, see [Permissions in Grail](https://docs.dynatrace.com/docs/platform/grail/organize-data/assign-permissions-in-grail).

    3.  Select **Create and test connection**.

    4.  After the test completes, select **Continue**.

6.  Set the configuration properties for the connection.

    1.  In the **Setup** stage, select **Set configuration properties**.

    2.  Select the **Create upstream/downstream service-to-service relationship** option to enable the creation of upstream and downstream relationships between Dynatrace Service CIs \(service‑to‑service\).

        See the [service\_to\_service\_relationships\_enabled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-properties.md) connection property for more information.

    3.  Select the **Append Dynatrace tenant id to calculated service name** option to enable the creation of unique names across multiple Dynatrace connections by appending the Dynatrace tenant ID to the Calculated Service names.

        See the [append\_tenant\_id\_to\_service\_name](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-properties.md) connection property for more information.

    4.  Specify the maximum number of records to be returned per Dynatrace API request in the **Dynatrace API batch size** field.

        See the [dynatrace\_api\_batch\_size](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-dynatrace-saas-properties.md) connection property for more information.

    5.  Select **Continue**.

7.  Configure the import schedule.

    1.  In the **Setup** stage, select **Configure import schedule**.

    2.  Select the import schedule for your connection, set it to **Active**, and fill in the run schedule details.

    3.  Select **Save**, then **Continue**.

8.  Select **Confirm connection creation** to verify the connection.


## What to do next

Select **View all connections** to review the connection details.

You can manage connections from the SGC Central view of the CMDB Workspace or the Ingestion view of the Service Graph Workspace. For more information, see [Managing connections added for Service Graph Connectors in SGC Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/sgcc-managing-connection.md).

