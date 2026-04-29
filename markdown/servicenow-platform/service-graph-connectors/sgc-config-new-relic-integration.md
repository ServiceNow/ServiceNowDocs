---
title: Configure Service Graph Connector for Observability - New Relic using the guided setup
description: Set up scheduled import jobs to pull in data from New Relic into your CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Observability - New Relic, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Observability - New Relic using the guided setup

Set up scheduled import jobs to pull in data from New Relic into your CMDB.

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=australia&pubname=australia-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

**Note:** If you have an earlier version of the Service Graph Connector for Observability - New Relic, then don’t migrate data from the old connector. You must uninstall the previous version and run the new integration.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for Observability - New Relic application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **New Relic** &gt; **Setup**.

3.  On the Getting started page, select **Get Started**.

4.  Configure the authentication credentials to send requests to the New Relic application.

    1.  Configure your New Relic connection and credentials.

        1.  In the Configure the Connection section of the New Relic Integration with CMDB page, select **Get Started**.
        2.  For the Configure connection and credentials task, select **Configure**.
        3.  On the Connections page of the Workflow Studio, select **Configure** for the **NewRelicConnectionAlias** connection that is available by default.
        4.  On the form, review and modify the fields.

<table id="table_vyj_kgv_y4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name to uniquely identify the connection record. For example, `NewRelicConnectionAlias`.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL to connect to the New Relic application in the following format: ```
https://api.newrelic.com/graphql
```

**Note:** This field is automatically set to the URL to connect to the NerdGraph API in the New Relic application. Leave the field value as is.

</td></tr><tr><td class="sub-head" colspan="2">

Credential Information

</td></tr><tr><td>

API Key

</td><td>

NerdGraph API token used for authentication on the New Relic application.

</td></tr><tr><td>

Account ID

</td><td>

Account ID associated with the New Relic credential.

</td></tr></tbody>
</table>        5.  Select **Configure Connection**.

            **Note:** The Service Graph Connector for Observability - New Relic supports connection to a single New Relic instance only. So, you can use the single default connection only.

        6.  Return to the Configure the connection task page using the back button for your browser.
        7.  Set the Configure connection and credentials task to complete by selecting **Mark as Complete**.
    2.  Test the NerdGraph API connection to import data from the New Relic application.

        1.  In the Configure the Connection section of the New Relic Integration with CMDB page, select **Continue**.
        2.  For the Test Connection task, select **Configure**.
        3.  Test the connection by selecting the **Test Connection** related link.

            Testing the connection might take a few moments. The page is refreshed to show the test results.

        4.  When the **Status** field is set to **Success**, select **Update**.

            If any of the tests have errors, follow the suggestions for remediation.

        5.  Set the Test Connection task to complete by selecting **Mark as Complete**.
5.  Configure the destination, channel, and workflow for Observability New Relic and turn on alerts for unmatched configuration items \(CIs\).

    1.  Configure the destination, channel, and workflow for Observability New Relic.

        1.  In the Configure Observability section of the New Relic Integration with CMDB page, select **Get started**.
        2.  For the Configure destination, channel and workflow task, select **Configure**.
        3.  In the SG-New Relic Webhooks list, select **New**.
        4.  On the form, fill in the fields.

<table id="table_ctf_lpz_nwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the New Relic configuration.The `destination`, `channel`, and `workflow` strings are appended to the configuration name when the configuration is created.

</td></tr><tr><td>

Connection and Credential Alias

</td><td>

Select the connection alias that you created in step [4](sgc-config-new-relic-integration.md#new-relic-alias).

</td></tr></tbody>
</table>        5.  Select **Submit**.
        6.  Set the Configure destination, channel and workflow task to complete by selecting **Mark as Complete**.
    2.  Enable alerts for configuration items \(CIs\) that aren’t available in the CMDB.

        1.  In the Configure Observability section of the New Relic Integration with CMDB page, select **Continue**.
        2.  For the Turn on alerts for unmatched CI task, select **Configure**.
        3.  On the System Properties form, select the **sn\_newrelic\_integ.alerts\_for\_unmatched\_ci.enabled** system property.
        4.  Set the **Value** of the system property to `true`.
        5.  Select **Submit**.
        6.  Set the Turn on alerts for unmatched CI task to complete by selecting **Mark as Complete**.
6.  Configure the scheduled jobs to import data from the New Relic application.

    1.  In the Set up scheduled data imports section of the New Relic Integration with CMDB page, select **Get started**.

    2.  For the Configure Scheduled Data Imports task, select **Configure**.

    3.  Select the scheduled job that you want to activate.

    4.  On the Scheduled Data Import form, verify the field values for the scheduled job.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select the **Active** check box to activate the scheduled job.

    6.  Select **Update**.

    7.  Repeat steps [6.c](sgc-config-new-relic-integration.md#select-job) to [6.f](sgc-config-new-relic-integration.md#exe-job) for each scheduled job for data import.

    8.  Navigate back to the guided setup page.

    9.  Set the Configure Scheduled Data Imports task to complete by selecting **Mark as Complete**.


