---
title: Configure Service Graph Connector for Wiz using guided setup
description: Set up scheduled import jobs to pull in data from a Wiz project into your CMDB.
locale: en-US
release: zurich
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-11-04"
reading_time_minutes: 6
breadcrumb: [Wiz, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Wiz using guided setup

Set up scheduled import jobs to pull in data from a Wiz project into your CMDB.

## Before you begin

**Important:** Starting with the Service Graph Connector for Wiz version 1.4.0, the guided setup method is deprecated. Use the SGC Central view in the CMDB Workspace to configure the connection for the connector.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   Wiz advanced or standard license
-   The Integration Commons for CMDB store app, which is automatically installed. See [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md).
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../concept/cmdb-ci-class-models.md).
-   ITOM Licensing plugin \(com.snc.itom.license\). See [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).
-   Discovery and Service Mapping Patterns \(sn\_itom\_pattern\). See [Install Discovery and Service Mapping Patterns](https://www.servicenow.com/docs/access?context=install-discovery-service-mapping-patterns&version=zurich&pubname=zurich-it-operations-management&ft:locale=en-US).
-   Discovery Core \(com.snc.discovery.core\)

You must obtain the OAuth credentials associated with the Wiz service account and make a note of the following details:

-   Client ID
-   Client Secret
-   OAuth Token URL
-   Connection URL

See [Set up the Wiz environment](sgc-cmdb-wiz-setup.md).

You must have the following permissions for the Wiz service account:

-   read:resources
-   read:projects

Role required: admin

## Procedure

1.  Verify that the application scope is set to the Service Graph Connector for Wiz application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Wiz** &gt; **Setup**.

3.  On the Service Graph Connector for Wiz page, verify that the **Quick Start** option is selected and then select **Continue**.

4.  Configure the connection to send requests to the Wiz application.

    1.  In the Configure the Connection and Credentials section of the Service Graph Connector for Wiz page, select **Start**.

    2.  Configure the connection.

        1.  Select the Configure the Connection task and then select **Click Here**.
        2.  On the Connections page that opens in another browser tab, select **Edit** for the **SG-Wiz** connection that is available by default.
        3.  On the form, fill in the fields.

<table id="table_zhs_djn_21c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to identify the connection record. For example, `SG-Wiz`.Don’t modify the name for the default connection alias `SG-Wiz`.

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

Client ID of your Wiz application as described in [Before you begin](sgc-config-wiz-integration.md#prereq).

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of your Wiz application as described in [Before you begin](sgc-config-wiz-integration.md#prereq).

</td></tr><tr><td>

OAuth Token URL

</td><td>

Token generation URL. This field is automatically set to the following URL:```
https://auth.app.wiz.io/oauth/token
```

</td></tr></tbody>
</table>        4.  Select **Edit and Get OAuth Token**.
        5.  Return to the guided setup.
        6.  Set the Configure the Connection task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    3.  Configure the connection properties.

        1.  Select the Add configuration properties task.
        2.  In the Service Graph Connections section, review and modify the property details by selecting a property from the **Property** column in the Service Graph Connection Properties related list.

            You can configure the following properties:

            -   **Projects**

                A list of comma-separated project IDs for which the resources are to be pulled.

            -   **Exclude Projects**

                A list of comma-separated project IDs for which the resources are excluded only when the **Projects** property isn’t set. In this case, all the resources except for the specified projects are imported.

            **Note:** If no property is configured, data from all the Wiz projects are fetched.

        3.  Select **Update** in the Service Graph Connection Properties section.
        4.  Set the Add connection properties task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    4.  Test the Wiz API connection to import data from the Wiz application.

        1.  Select the Test Connection task.
        2.  Test the connection by selecting the **Test Connection** related link.

            Testing the connection might take a few moments. The page is refreshed to show the test results.

        3.  When the **Status** field is set to **Success**, select **Update**.

            If any of the tests have errors, follow the suggestions for remediation.

        4.  Set the Test Connection task to complete by selecting the **Mark as complete** check box and then select **Continue**.
5.  Configure the scheduled jobs to import data from the Wiz application.

    1.  Configure the scheduled job for the complete \(full\) import of data during the initial execution, and then incremental \(delta\) import of data on subsequent executions.

        1.  Select the Configure the scheduled jobs task.
        2.  Select the **SG-Wiz-Organization** scheduled job.
        3.  On the Scheduled Data Import form, verify the field values for the scheduled job.

            For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

        4.  Select the **Active** check box to activate the SG-Wiz-Organization scheduled job.
        5.  In the **Run** field, select **Periodically** to specify how often the job will run.
        6.  Select **Update**.
        7.  Set the Configure the scheduled jobs task to complete by selecting the **Mark as complete** check box and then select **Continue**.
    2.  Configure the Reset Last Run Datetime for SG-Wiz scheduled script to enable full pull for subsequent execution of the scheduled job.

        **Note:** To fetch the complete data using a data source on subsequent executions, you must remove the **Last Run Date Time** field value from a data source. The Reset Last Run Datetime for SG-Wiz scheduled script provided with the connector resets the **Last Run Date Time** field value automatically. Therefore, confirming that the SG-Wiz Organization scheduled job executes all data sources for a full pull.

        1.  Select the Configure the scheduled script for full data retrieval task.
        2.  Select the **Active** check box to activate the SG-Wiz scheduled script.
        3.  In the **Run** field, select **Periodically** to specify how often the script will run.

            For more information, see [Automatically run a script of your choosing](https://www.servicenow.com/docs/access?context=t_ScheduleAScriptExecution&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US#t_ScheduleScriptExecution).

        4.  Select **Update**.
        5.  Set the Configure the scheduled script for full data retrieval task to complete by selecting the **Mark as complete** check box and then select **Continue**.
6.  On the Service Graph Connector for Wiz page, select **Complete** to save your changes.

7.  In Complete setup dialog box, select **Complete** to complete the setup.

8.  In the message box that appears, select **Done**.


