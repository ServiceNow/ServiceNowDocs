---
title: Configure Service Graph Connector for Trellix using guided setup
description: Set up scheduled import jobs to pull in data from a Trellix project into your CMDB.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Trellix, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure Service Graph Connector for Trellix using guided setup

Set up scheduled import jobs to pull in data from a Trellix project into your CMDB.

## Before you begin

**Important:** Unless there are configuration issues, use SGC Central to configure the connection. The guided setup method for configuration is being deprecated.

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=australia&pubname=australia-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The Integration Commons for CMDB store app, which is automatically installed. See [Integration Commons for CMDB](../concept/integration-commons-for-cmdb.md).
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../concept/cmdb-ci-class-models.md).
-   The ITOM Licensing plugin \(com.snc.itom.license\). See [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

Role required: admin

## Procedure

1.  Verify that the application scope is set to the Service Graph Connector for Trellix application by using the application picker.

    For more information, see [Application picker](https://www.servicenow.com/docs/access?context=c_ApplicationPicker&version=australia&pubname=australia-application-development&ft:locale=en-US).

2.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Trellix** &gt; **Setup**.

3.  On the Service Graph Connector for Trellix page, verify that the **Quick Start** option is selected, and then select **Continue**.

4.  Configure the connection to send requests to the Trellix application.

    1.  On the Service Graph Connector for Trellix page, in the Configure the Connection and Credentials section, select **Start**.

    2.  Configure the authentication credentials.

        1.  For the Configure Trellix authentication credentials task, fill in the fields on the Basic Auth Credentials form.

            |Field|Description|
            |-----|-----------|
            |Name|Credentials to use for the connection. For example, `SGTrellix.Credentials`.|
            |Order|The sequence in which the records are processed. The default value is `100`.|
            |User name|User name of your Trellix account.|
            |Password|Password of your Trellix account.|
            |Active|Verify that the check box is selected.|

        2.  Select **Update** to save the authentication credentials.
        3.  Set the Configure Trellix authentication credentials task to complete by selecting **Mark as complete**, and then select **Continue**.
    3.  Configure the HTTP connection.

        1.  For the Configure Trellix HTTP Connection task, fill in the fields on the HTTP\(s\) Connection form.

<table id="table_x2m_wp5_lfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the Trellix connection record. For example, `SGTrellix`.Don’t modify the name for the default connection `SGTrellix`.

</td></tr><tr><td>

Active

</td><td>

Verify that the check box is selected.

</td></tr><tr><td>

Credential

</td><td>

Credentials to use for the connection.

</td></tr><tr><td>

Domain

</td><td>

Domain that contains the connection.

</td></tr><tr><td>

Connection alias

</td><td>

Connection alias that resolves your connection and credentials at runtime.**Note:** Only one connection is active per connection alias at a time.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL of the connection. The base URL is the hostname of your Trellix instance. For example, `https://*subdomain*.*domain*.com:*port*`.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server. Select this check box if you're using an on-premises instance of Trellix. Complete the **Advanced MID Server Configuration**.**Note:** A MID Server must be configured on your ServiceNow instance before you select this option.

</td></tr><tr><td>

MID selection

</td><td>

Select a MID Server from the list.This field appears only when the **Use MID Server** check box is selected.

</td></tr><tr><td>

MID application

</td><td>

Select a MID Server application from the list.This field appears only when the **Use MID Server** check box is selected.

</td></tr><tr><td>

Connection timeout

</td><td>

The maximum time \(in seconds\) the system waits while attempting to establish a connection.

</td></tr></tbody>
</table>        2.  Select **Update** to save the HTTP connection details.
        3.  Set the Configure Trellix HTTP Connection task to complete by selecting **Mark as complete**, and then select **Continue**.
    4.  Test the Trellix API connection to import data from the Trellix application.

        1.  Test the connection by selecting the **Test Connection** related link in the Test Connection task.

            Testing the connection might take a few moments. The page is refreshed to show the test results.

        2.  When the **Status** field is set to **Success**, set the Test Connection task to complete by selecting **Mark as complete**, and then select **Continue**.

            If any of the tests have errors, follow the suggestions for remediation.

5.  Add multiple instances.

    **Note:** If you don't need to add multiple instances, you can skip this step.

    1.  On the Service Graph Connector for Trellix page, in the Add Multiple Instances section, select **Start**.

    2.  In the Update Data Source Access section, select the Data Source \[sys\_data\_source\] table.

    3.  Select the **Global** application scope by using the application picker.

    4.  In the Application Access related list, select the **Can create**, **Can update**, and **Can delete** check boxes, if not already selected.

    5.  Modify the application scope again to **Service Graph Connector for Trellix** by using the application picker.

    6.  Select **Update** to save the data source access details.

    7.  Set the Update Data Source Access task to complete by selecting **Mark as Complete**, and then select **Continue**.

    8.  Repeat steps [5.c](sgc-config-trellix-integration.md#substep_zwt_dv4_nfc) to [5.e](sgc-config-trellix-integration.md#substep_gzr_2hp_nfc) for the Update Scheduled Data Import Access task with the Scheduled data import \[scheduled\_data\_set\] table.

    9.  Select **Update** to save the scheduled data import access details.

    10. Set the Update Scheduled Data Import Access task to complete by selecting **Mark as Complete**, and then select **Continue**.

    11. In the Add Another Connection section, modify the application scope to **Service Graph Connector for Trellix** by using the application picker.

    12. Select **Click Here**.

    13. On the Workflow Studio page, select **Add Connection** in the SGTrellix section.

    14. Fill in the fields on the Create Connection form, and then select **Create Connection**.

<table id="table_pgl_qw4_nfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection name

</td><td>

Name to identify the Trellix connection record.

</td></tr><tr><td>

Connection url

</td><td>

URL of the connection.

</td></tr><tr><td>

Use MID server

</td><td>

Option to use a MID Server. Select this check box if you're using an on-premises instance of Trellix. Complete the **Advanced MID Server Configuration**.**Note:** A MID Server must be configured on your ServiceNow instance before you select this option.

</td></tr><tr><td>

MID selection

</td><td>

Select a MID Server from the list.This field appears only when the **Use MID Server** check box is selected.

</td></tr><tr><td>

MID application

</td><td>

Select a MID Server application from the list.This field appears only when the **Use MID Server** check box is selected.

</td></tr><tr><td>

User name

</td><td>

User name of your Trellix account.

</td></tr><tr><td>

Password

</td><td>

Password of your Trellix account.

</td></tr></tbody>
</table>    15. Close the Workflow Studio page, and navigate back to the guided setup.

    16. Set the Add Another Connection task to complete by selecting **Mark as Complete**, and then select **Continue**.

    17. In the Test New Connections section, select the newly created connection record, and then select the **Test Connection** related link.

        Testing the connection might take a few moments. The page is refreshed to show the test results.

    18. When the **Status** field is set to **Success**, set the Test New Connections task to complete by selecting **Mark as complete**, and then select **Continue**.

        If any of the tests have errors, follow the suggestions for remediation.

6.  Configure the scheduled jobs to import data from the Trellix application.

    1.  On the Service Graph Connector for Trellix page, in the Set up scheduled import jobs section, select **Start**.

    2.  For the Configure the scheduled jobs task, select the connection.

        **Note:** The SG-Trellix-Devices scheduled import job is set to inactive by default.

    3.  On the Scheduled Data Import form, verify the field values for the scheduled job.

        For more information, see [Schedule a data import](https://www.servicenow.com/docs/access?context=t_ScheduleADataImport&version=australia&pubname=australia-integrate-applications&ft:locale=en-US#table_r53_5hm_xp).

    4.  Select the **Active** check box to activate the SG-Trellix-Devices scheduled import job.

    5.  In the **Run** field, select **Periodically** to specify how often the job runs.

    6.  Select **Execute Now** to execute the import schedule.

    7.  Set the Configure the scheduled jobs task to complete by selecting **Mark as complete**, and then select **Continue**.

7.  On the Service Graph Connector for Trellix page, select **Exit** to exit the guided setup.


**Related topics**  


[Service Graph Connector for Trellix](../concept/sgc-integration-trellix.md)

[CMDB classes targeted in Service Graph Connector for Trellix](../reference/cmdb-trellix-classes.md)

[Accessing the connection details of Service Graph Connector for Trellix](../concept/sgc-trellix-conn.md#)

