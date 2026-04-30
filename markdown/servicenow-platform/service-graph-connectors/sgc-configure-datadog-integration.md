---
title: Configure Service Graph Connector for Observability - Datadog
description: Pull in data from Datadog into your Configuration Management Database \(CMDB\).
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 5
breadcrumb: [Observability-Datadog, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Observability - Datadog

Pull in data from Datadog into your Configuration Management Database \(CMDB\).

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

**Note:** If you have an earlier version of the Service Graph Connector for Observability - Datadog, then don’t migrate data from the old connector. You must uninstall the previous version and run the new integration.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Observability Datadog** &gt; **Setup**.

2.  On the Getting started page, select **Get Started**.

3.  Configure the authentication credentials and the host name to send requests to the Datadog API.

    1.  Configure your Datadog credentials.

        1.  In the Configure the Connection section of the Datadog Integration with CMDB page, select **Get Started**.
        2.  For the Configure the Credentials task, select **Configure**.
        3.  In the **Connection name** field, enter a name for the connection.

            **Note:** Do not modify the name of the default connection.

        4.  In the **Connection URL** field, enter the base URL or IP address for Datadog.
        5.  In the **API key** field, enter the Datadog API token.
        6.  In the **Application key** field, enter the application key used for connecting to the Datadog API.
        7.  Select **Update**.
        8.  Set the Configure the Credentials task to complete by selecting **Mark as Complete**.
    2.  Test the connection.

        1.  For the Test Connection task, select **Configure**.
        2.  Test the connection by selecting the **Test Connection** related link.

            Testing the connection might take a few moments. The page is refreshed to show the test results.

        3.  When the **Status** field is set to **Success**, select **Update**.

            If any of the tests have errors, follow the suggestions for remediation.

        4.  Set the Test Connection task to complete by selecting **Mark as complete**.
    3.  Add a filter for the SGO-Datadog Hosts \[sn\_datadog\_integra\_datadog\_hosts\] data source.

        1.  For the Create Hosts Filter task, select **Configure**.
        2.  Enter a comma-separated list of host tags in `key:value` format in the **Value** field to define a filter for pulling host data from Datadog.

            For example, `datadog:monitored,env:production`.

        3.  Select **Update**.
        4.  Set the Create Hosts Filter task to complete by selecting **Mark as complete**.
4.  Configure the webhook and monitors for Observability Datadog.

    1.  In the Configure Observability section of the Datadog Integration with CMDB page, select **Get started**.

    2.  For the Configure the Webhooks and Monitors task, select **Configure**.

    3.  In the Datadog Webhooks list, select **New** to add a Datadog webhook.

    4.  Fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Name|Name of the Datadog webhook.|
        |Connection Alias|Search for and select the connection and credential alias that you created in step [3](sgc-configure-datadog-integration.md#datadog-alias).|

    5.  Select **Submit**.

    6.  Populate the Datadog Webhooks list by selecting the **Synchronize Monitors** related link on the Datadog Webhook page.

        **Note:** In the Datadog Webhooks list, don't select **New** to add a monitor as this option is not used in this scenario.

    7.  In the **Name** column of the Datadog Webhooks list, select a monitor.

    8.  On the Datadog Monitors page, select the **Webhook Active** check box, and then select **Update**.

    9.  Repeat steps [4.g](sgc-configure-datadog-integration.md#substep-datadog-monitor1) and [4.h](sgc-configure-datadog-integration.md#substep-datadog-monitor2) for all the monitors in the Datadog Webhooks list.

    10. On the Datadog Webhook page, select **Update** to save your changes.

    11. Set the Configure the Webhooks and Monitors task to complete by selecting **Mark as Complete**.

5.  Set up scheduled import jobs.

    1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Observability Datadog** &gt; **Import Schedules**.

    2.  Select the name of the scheduled import that you want to activate.

    3.  On the Scheduled Data Import form, verify the field values for the scheduled job and select the **Active** check box.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select **Update**.


**Related topics**  


[Service Graph Connector for Observability - Datadog](../concept/sgc-cmdb-integration-datadog.md)

[CMDB classes targeted in Service Graph Connector for Observability - Datadog](../reference/sgc-cmdb-datadog-classes.md)

[Accessing the connection details of Service Graph Connector for Observability - Datadog](../concept/sgc-datadog-conn.md#)

