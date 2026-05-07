---
title: Configure Service Graph Connector for Observability - New Relic using SGC Central
description: Use the playbook available with the SGC Central application to set up the Service Graph Connector for Observability - New Relic for pulling in New Relic project data into the CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Observability - New Relic, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Observability - New Relic using SGC Central

Use the playbook available with the SGC Central application to set up the Service Graph Connector for Observability - New Relic for pulling in New Relic project data into the CMDB.

## Before you begin

Dependencies and requirements:

-   Install Service Graph Connector for Observability - New Relic version 1.3.0 or later from the ServiceNow Store. For ServiceNow Store installation steps, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=installing-applications-in-application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US).
-   Install Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

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

3.  On the Create connection window, select the New Relic connector type, and then select **Create connection**.

4.  Complete the initial prerequisites when setting up a connection for the first time using a connector.

    **Note:** This step is required only during the first-time setup. See [Perform initial setup tasks when creating a connection in SGC Central](sgcc-first-time-setup.md).

5.  Enter connection details and test the API connection for importing New Relic data.

    1.  In the **Setup** stage of the playbook, select the **Create and test connection** activity.

    2.  On the form, fill in the fields.

        |Field|Description|
        |:----|:----------|
        |Connection Name|Name to identify the New Relic connection record.|
        |Connection URL|New Relic base URL in the following format: `*&lt;base-URL&gt;*`.|
        |API Key|New Relic API key or tenant code.|
        |Account ID|New Relic account ID.|

    3.  Select **Update and test connection**.

    4.  After the connection test is complete, select **Continue**.

6.  For the Configure Observability activity, select **Continue**.

    New Relic creates the destination, channel, and workflow required to enable alerts for all configuration items \(CIs\).

7.  Configure the import schedule to import data at regular intervals.

    1.  In the **Setup** stage of the playbook, select the **Configure import schedule** activity.

    2.  Select **Configure import schedule**.

    3.  Expand the Parent scheduled data import within the Import schedules list to select the **SG-New Relic Hosts** import schedule.

    4.  In the Configure import schedule dialog box, select the **Active** check box, and then fill in the run schedule and time details.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Save**.

        Alternatively, select **Execute Now** to execute the import schedule immediately.

    6.  Select **Continue**.

8.  In the **Setup** stage of the playbook, select the **Confirm connection creation** activity to verify whether the connection was configured.

9.  Enable alerts for configuration items \(CIs\) that aren’t available in the CMDB.

    1.  Navigate to **Workspaces** &gt; **CMDB Workspace** &gt; **SGC Central**.

    2.  Select **Settings**.

    3.  Select **New Relic system properties**.

    4.  On the System Properties form, select the **sn\_newrelic\_integ.alerts\_for\_unmatched\_ci.enabled** system property.

    5.  Set the **Value** of the system property to `true`.

    6.  Select **Submit**.


## What to do next

Select **View all connections** to review the connection details. The configured connection appears in the Installed connections list.

**Related topics**  


[Service Graph Connector for Observability - New Relic](../../configuration-management/concept/sgc-cmdb-integration-new-relic.md)

