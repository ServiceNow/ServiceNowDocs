---
title: Configure Service Graph Connector for Observability - AppDynamics using the guided setup
description: Set up scheduled import jobs to pull in data from AppDynamics into your Configuration Management Database \(CMDB\).
locale: en-US
release: xanadu
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-12-09"
reading_time_minutes: 7
breadcrumb: [Observability-AppDynamics, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Observability - AppDynamics using the guided setup

Set up scheduled import jobs to pull in data from AppDynamics into your Configuration Management Database \(CMDB\).

## Before you begin

**Important:** Unless there are configuration issues, use the SGC Central view in the Service Graph Workspace or CMDB Workspace to configure the connection for the connector, as the guided setup method is planned for deprecated.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=xanadu&pubname=xanadu-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

When using client credentials for authentication, obtain the OAuth credentials from your AppDynamics administrator. Make a note of the following details:

-   Application \(client\) ID
-   Client Secret

**Note:** If you have an earlier version of the Service Graph Connector for Observability - AppDynamics, then do not migrate data from the old connector. You must uninstall the previous version and run the new integration.

Role required: SGC-Admin \(sn\_cmdb\_int\_util.sgc\_admin\) or admin

**Note:** The admin user role is required to run background scripts and to provide access to global tables to the SGC-Admin user. For information about the user roles for Service Graph Connectors, see [Service Graph Connector user roles](../concept/cmdb-sgc-intro.md#section_ett_spp_4hc).

## Procedure

1.  Ensure that the application scope is set to the Service Graph Connector for Observability - AppDynamics application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **AppDynamics** &gt; **Setup**.

3.  On the Getting started page, select **Get Started**.

4.  Configure the authentication credentials and establish an HTTP connection to send requests to the AppDynamics API.

    1.  In the Configure API authentication section of the Service Graph Connector for Observability - AppDynamics page, select **Get Started**.

    2.  Configure the connection for AppDynamics by editing the default connection.

        You can configure either a Basic Auth connection or an OAuth connection.

        **Note:** As the connector supports only single instance, edit the **AppDynamicsConnectionAlias** connection, available by default.

        -   Configure a Basic Auth connection.
            1.  For the Configure Basic Auth Connection task, select **Configure**.
            2.  Select **Edit** for AppDynamicsConnectionAlias.

                **Note:** If not redirected to the connection setup, search for **AppDynamicsConnectionAlias** on the Integrations page, and then select **View Details** to edit the default connection.

            3.  In the Connection Information section of the Edit Connection window, fill in the fields.

<table id="table_umb_r4t_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the AppDynamics connection record.`AppDynamicsConnectionAlias` is the default credential alias name and is read-only.

</td></tr><tr><td>

Host name

</td><td>

Host name of your AppDynamics controller.

</td></tr></tbody>
</table>            4.  \(Optional\) If a MID Server is required for the AppDynamics server connection, select the **Use MID server** check box. Then, select the MID Server-related fields accordingly.
            5.  In the Credential Information section of the Edit Connection window, fill in the fields.

<table id="table_vmb_r4t_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Username

</td><td>

AppDynamics account user name that is used to authenticate the connection request.**Note:** Verify that Server Visibility is active for the AppDynamics account and the AppDynamics user has the Applications and Dashboards Viewer \(Default\) and Server Monitoring User \(Default\) roles.

</td></tr><tr><td>

Password

</td><td>

Password that is used to authenticate the connection request.

</td></tr></tbody>
</table>            6.  Select **Edit Connection**.
            7.  Return to the guided setup page.
            8.  Set the Configure Basic Auth Connection task to complete by selecting **Mark as Complete**.
        -   Configure an OAuth connection.
            1.  For the Configure OAuth Authentication: Client Credentials task, select **Configure**.
            2.  Select **Edit** for AppDynamicsConnectionAlias.

                **Note:** If not redirected to the connection setup, search for **AppDynamicsConnectionAlias** on the Integrations page, and then select **View Details** to edit the default connection.

            3.  In the Connection Information section of the Edit Connection window, fill in the fields.

<table id="table_rsj_ppt_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the AppDynamics connection record.`AppDynamicsConnectionAlias` is the default credential alias name and is read-only.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL of your AppDynamics controller.

</td></tr></tbody>
</table>            4.  \(Optional\) If a MID Server is required for the AppDynamics server connection, select the **Use MID server** check box. Then, select the MID Server-related fields accordingly.
            5.  In the Credential Information section of the Edit Connection window, fill in the fields.

<table id="table_ssj_ppt_zfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID of your AppDynamics client application as noted in the [Before you begin](configure-appdynamics-integration.md#prereq_xvj_dg1_bgc) section.**Note:** Verify that the API client has a role with the required privileges and sufficient Token Expiration Time.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret of your AppDynamics client application as noted in the [Before you begin](configure-appdynamics-integration.md#prereq_xvj_dg1_bgc) section.

</td></tr></tbody>
</table>            6.  Select **Edit Connection**.
            7.  Return to the guided setup page.
            8.  Set the Configure OAuth Authentication: Client Credentials task to complete by selecting **Mark as Complete**.
    3.  Test the connection.

        1.  For the Test connection task, select **Configure**.
        2.  Select the **Test Connection** related link to start the testing process.
        3.  When the **Status** field is set to **Success**, return to the guided setup page.

            **Note:** If any of the tests have errors, follow the suggestions for remediation.

        4.  Set the Test the connection task to complete by selecting **Mark as Complete**.
    4.  Enable AppDynamics event integration with your ServiceNow instance by pushing a default HTTP Request Template to AppDynamics.

        **Note:** To push HTTP requests, verify that the Observability Commons for CMDB application \(sn\_observability\) is installed for events ingestion on your ServiceNow instance. Also, on your AppDynamics instance, as the ServiceNow user, you must have the account-level Configure HTTP Request Templates permission to create or modify HTTP Request Templates.

        1.  For the Push HTTP Request Template task, select **Configure**.
        2.  Select the **Push HTTP Request Template** related link.
        3.  Return to the guided setup page.
        4.  Set the Push HTTP Request Template task to complete by selecting **Mark as Complete**.
        After you push the HTTP request template, multiple API calls are executed to start the event ingestion service in AppDynamics. For more information, see the [Service Graph Connector for Observability AppDynamics](https://www.servicenow.com/community/cmdb-blog/service-graph-connector-for-observability-appdynamics/ba-p/2275530) article on the ServiceNow Community site.

5.  Configure duplicate detection rules.

    1.  For the Configure duplicate detection rules task in the Duplicate detection rules section, select **Configure**.

    2.  In the CMDB Duplicate Row Rules list, set the **Active** column value for a rule to **true** to activate the rule.

        **Note:** To remove fields from being evaluated, add the field names in the **Ignore Fields** column for a rule. To ignore multiple fields, separate the fields with commas.

    3.  Return to the guided setup page.

    4.  Set the Configure duplicate detection rules task to complete by selecting **Mark as Complete**.

6.  Configure advanced settings.

    1.  For the Advanced Settings task in the Advanced section, select **Configure**.

    2.  Review and modify the advanced properties.

        |Property|Description|
        |--------|-----------|
        |Toggle to populate relationships between tiers|Option to enable the import of relationships between AppDynamics tiers in the CI Relationship \[cmdb\_rel\_ci\] table.|
        |The number of minutes of metrics to fetch in order to generate tier to tier relationships|Number of minutes of metrics to fetch for generating tier-to-tier relationships. For example, `60` retrieves the last hour's relationships.|
        |Toggle to import business transactions from AppDynamics|Option to enable the import of business transactions into the Calculated Application Service \[cmdb\_ci\_service\_calculated\] table.|
        |Toggle to populate tags for imported servers|Option to enable the import of server tags into the Key Value \[cmdb\_key\_value\] table.|
        |Toggle to import node data from AppDynamics and map to the cmdb\_ci\_appl hierarchy|Option to enable the import of nodes into the Application \[cmdb\_ci\_appl\] table hierarchy.|

    3.  Select **Save**.

    4.  Set the Advanced Settings task to complete by selecting **Mark as Complete**.

7.  Set up the SG-AppDynamics Servers and Applications scheduled job available by default.

    1.  For the Configure scheduled job task in the Set up scheduled import jobs section, select **Configure**.

    2.  On the Scheduled Data Import form, verify the field values for the SG-AppDynamics Servers and Applications scheduled job and select the **Active** check box.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    3.  Select **Update**.

    4.  Set the Configure scheduled job task to complete by selecting **Mark as Complete**.


