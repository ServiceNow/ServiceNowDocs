---
title: Configure Service Graph Connector for Microsoft Defender Endpoint using the guided setup
description: Pull in data from machines using the Microsoft Defender for Endpoint security solution into your Configuration Management Database \(CMDB\).
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 5
breadcrumb: [Microsoft Defender for Endpoint, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Microsoft Defender Endpoint using the guided setup

Pull in data from machines using the Microsoft Defender for Endpoint security solution into your Configuration Management Database \(CMDB\).

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. For Event Management to work, the Observability Commons for CMDB \(sn\_observability\) app must be installed prior to installing the connector. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

Complete the following tasks:

-   Install the Service Graph Connector for Microsoft Defender Endpoint application \(sn\_defender\_integ\). For more information, see [Install a ServiceNow Store application](https://www.servicenow.com/docs/access?context=t_InstallApplications&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US).
-   Ensure that you have an active subscription to Microsoft Defender for Endpoint.
-   Ensure that you have created an Azure application to get programmatic access to Microsoft Defender for Endpoint. See [Create an app to access Microsoft Defender for Endpoint without a user](https://learn.microsoft.com/en-us/defender-endpoint/api/exposed-apis-create-app-webapp?view=o365-worldwide) in the Microsoft 365 documentation.
-   Obtain the tenant ID, client ID, and client secret details for the Microsoft Defender for Endpoint administrator account.
-   Enable the Machine.Read.All and Machine.ReadWrite.All permissions in Microsoft Defender for Endpoint. See [Permissions](https://learn.microsoft.com/en-us/microsoft-365/security/defender-endpoint/api/get-machines?view=o365-worldwide#permissions) for the List machines API in the Microsoft 365 documentation.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for Microsoft Defender Endpoint application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Microsoft Defender** &gt; **Setup**.

3.  On the Getting started page, select **Get Started**.

4.  Configure the authentication credentials details for sending requests to the List machines API in Microsoft Defender for Endpoint.

    1.  Configure your Microsoft Defender for Endpoint authentication credentials.

        1.  In the Configure the connection section of the Service Graph Connector for Microsoft Defender page, select **Get Started**.
        2.  For the Configure the credentials task, select **Configure**.
        3.  On the form, review and modify the fields.

<table id="table_npd_v2z_swb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the connection record.**Note:** This field is automatically set to the `SG Defender OAuth` connection record. Leave the field value as is.

</td></tr><tr><td>

Client ID

</td><td>

Application \(client\) ID of your Microsoft Defender for Endpoint as described in the [Before you begin](sgc-configure-msdefender-integration.md#prereq_onn_3sx_tzb) section.

</td></tr><tr><td>

Client Secret

</td><td>

Client Secret of your Microsoft Defender for Endpoint as described in the [Before you begin](sgc-configure-msdefender-integration.md#prereq_onn_3sx_tzb) section.

</td></tr><tr><td>

OAuth Token URL

</td><td>

Token URL of your Microsoft Defender for Endpoint.Enter the token URL in the following format:

```
https://login.microsoftonline.com/*&lt;tenantid&gt;*/oauth2/v2.0/token
```

Where *&lt;tenantid&gt;* is the tenant ID of your Microsoft Defender for Endpoint as described in the [Before you begin](sgc-configure-msdefender-integration.md#prereq_onn_3sx_tzb) section.

</td></tr></tbody>
</table>        4.  Select **Update**to return to the guided setup page.
        5.  Set the Configure the credentials task to complete by selecting **Mark as Complete**.
    2.  Test the List machines API connection to import machine-related data from Microsoft Defender for Endpoint.

        1.  For the Test the connection task, select **Configure**.
        2.  On the Service Graph Connections page, select **Test Connection**.
        3.  When the **Status** field is set to **Success**, select **Update** to close the Test the connection dialog box and return to the guided setup page.

            If any of the tests have errors, follow the suggestions for remediation.

        4.  Set the Test the connection task to complete by selecting **Mark as Complete**.
5.  Configure the scheduled jobs to import machine-related data from Microsoft Defender for Endpoint.

    1.  In the Set up scheduled import jobs section of the Service Graph Connector for Microsoft Defender page, select **Get Started**.

    2.  For the Configure scheduled jobs task, select **Configure**.

    3.  From the **Name** column, select the scheduled job that you want to activate.

        By default, the SG-Defender Machines scheduled job is available to run the SG-Defender Machines data source.

    4.  On the Scheduled Data Import form, verify the field values for the scheduled job.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    5.  Select **Update**.

    6.  Select the back button of your browser to return to the guided setup page.

    7.  Set the Configure the scheduled jobs task to complete by selecting **Mark as Complete** in the guided setup.


**Related topics**  


[Accessing the connection details of Service Graph Connector for Microsoft Defender Endpoint](../concept/sgc-cmdb-msdefender-conn.md#)

