---
title: Configure the Service Graph Connector for Qualys
description: Set up the Qualys environment and scheduled jobs to import in Qualys data into your Configuration Management Database \(CMDB\).
locale: en-US
release: yokohama
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Qualys, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the Service Graph Connector for Qualys

Set up the Qualys environment and scheduled jobs to import in Qualys data into your Configuration Management Database \(CMDB\).

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by [ITOM Visibility or ITOM Discovery](https://www.servicenow.com/docs/access?context=itom-license-module&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US), these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

Dependencies and requirements:

-   The [Integration Commons for CMDB](../../../configuration-management/concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models](../../../configuration-management/concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see [Request Discovery](https://www.servicenow.com/docs/access?context=t_ActivateTheDiscoveryPlugin&version=yokohama&pubname=yokohama-it-operations-management&ft:locale=en-US).
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This app must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

There are two supported Qualys APIs:

-   Qualys Global Asset API v2. You might prefer to use this API if you are importing data for the Security Posture Control application.
-   Qualys Asset Management API v2. This API is deactivated by default. You should only activate this API if you don't have access to the Qualys Cybersecurity Asset Management \(CSAM\) product. ServiceNow® uses a different API \(Asset management and tagging\) for this API but the data returned is not comprehensive.

For more information, see [Service Graph Connector for Qualys APIs](../reference/sgc-qualys-apis.md).

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Qualys** &gt; **Setup**.

2.  Select **Continue** on the Home page.

3.  Select **Best Experience** and **Continue** on the Experience page.

    On the Service Graph Connector for Qualys page in the Configure the connection page, three tasks are displayed:

    -   Configure the connection
    -   Add multiple instances
    -   Set up scheduled import jobs
4.  Select **Start** for the **Configure the Connection** task to expand it.

    The following steps are displayed:

    -   Configure Qualys authentication credentials
    -   Configure Qualys HTTP Connection
    -   Test Connection
5.  Select **Configure Qualys authentication credentials**.

    1.  In the Username and Password field, enter your Qualys username and password.

    2.  Select the **Active** check box to activate the record.

    3.  Right-click in the gray header titled Basic Auth Credentials and select **Save**.

    4.  Select **Mark as complete** followed by **Continue**.

        The Configure Qualys HTTP Connection page is displayed.

6.  Fill in the fields.

    1.  Add the Qualys base URL or Host details.

        Domain part of the URL without the 'https'. An example might be `qualysapi.qualys.com`.

    2.  If the API is accessible through a MID Server, activate the **Use MID Server** check box.

    3.  In the advanced MID Server configuration section select the appropriate MID Server from the MID Selection list.

    4.  Right-click in the gray header titled HTTP\(s\) Connection and select **Save**.

    5.  Select **Mark as complete** followed by **Continue**.

        The Test Connection page is displayed.

7.  Test the connection.

    1.  Update the **use\_asset\_management\_and\_tagging\_api** property in the 'Service Graph Connection Properties' section.

        |Option|Description|
        |------|-----------|
        |true|Set the property **use\_asset\_management\_and\_tagging\_api** flag to `true` if you are using the asset management and tagging API in the configuration.|
        |false|Set the property **use\_asset\_management\_and\_tagging\_api** to `false` if you are not using the asset management and tagging API in the configuration.|

    2.  In the Related links section select the **Test Connection** link.

        If the connection is successful, the status code field displays `200` or `201` and a message is displayed. If your connection test fails, review the Message and Suggestion fields for how to proceed.

    3.  Right-click in the gray header titled Service Graph Connections and select **Save**.

    4.  Select **Mark as complete** followed by **Continue**.

        The Update Data Source Access page is displayed.

8.  Update the data source.

    1.  Follow the steps listed at the top of the page to switch the application scope with the application picker to open, edit, and save the record.

    2.  Select a record from the list to open it.

    3.  Select the **Application Access** tab.

    4.  Select the check boxes to set the permissions you want.

    5.  Right-click in the gray header titled Tables and select **Save**.

    6.  Select **Mark as complete** followed by **Continue**.

        The Update Scheduled Data Import page is displayed.

9.  Update the Scheduled Data Import record.

    1.  Follow the steps listed at the top of the page to switch the application scope with the application picker as required to open, edit, and save the record.

    2.  Select the **Application Access** tab.

    3.  Select the check boxes to set the permissions you want.

    4.  Right-click in the gray header titled Table and select **Save**.

    5.  Select **Mark as complete** followed by **Continue**.

        The Add Another Connection task is displayed.

10. Follow the instructions at the top of the page to add a connection.

    1.  Follow the steps listed at the top of the page to switch the application scope with the application picker to open, edit, and save the record.

    2.  Select the link.

        The SG-Qualys Connections page is displayed.

    3.  Select **Add Connection** and fill out the fields.

        |Field|Description|
        |-----|-----------|
        |Connection name|Unique name for your connection|
        |Connection URL|Connection URL|
        |User name|Qualys account user name|
        |Password|Qualys account password|

    4.  Select **Create Connection**.

    5.  Navigate back to the Add Another Connection page in the Setup Assistant.

    6.  Select **Mark as complete** followed by **Continue**.

        The Configure MID Server for new HTTP connection page is displayed.

11. Configure the MID Server

    1.  Select a record to open it.

    2.  Select the Use MID server check box.

    3.  Select the search icon in the MID Server field and choose one from the list.

    4.  Right-click in the gray header titled HTTP\(s\) Connection and select **Save**.

    5.  Select **Mark as complete** followed by **Continue**.

        The Test New Connections page is displayed.

12. Test the connection.

    1.  Select the record for the connection you want to test.

    2.  Scroll to the Related links section and select the **Test Connection** link.

        If the connection is successful, the status code field displays `200` or `201` and a message is displayed. If your connection test fails, review the Message and Suggestion fields for how to proceed.

    3.  Right-click in the gray header titled, Service Graph Connections and select **Save**.

    4.  Select **Mark as complete** followed by **Continue**.

        The Configure the scheduled jobs page is displayed.

13. Configure the scheduled jobs.

    1.  Select a record to open it.

    2.  Fill out the scheduled data import from.

<table id="table_tmw_f2z_tzb"><tbody><tr><td>

Field

</td><td>

Description

</td></tr><tr><td>

Name

</td><td>

Name of the scheduled job.

</td></tr><tr><td>

Application

</td><td>

Read-only application name.

</td></tr><tr><td>

Data source

</td><td>

Data source record that defines the data to import.

</td></tr><tr><td>

Run

</td><td>

How often you want the job to run. If you want to run a test import prior to scheduling it, you might prefer to select **Once**.

</td></tr><tr><td>

Run as

</td><td>

Option to run the scheduled job with the credentials of the specified user.

</td></tr><tr><td>

Conditional

</td><td>

Specific conditions under which this job is run.

</td></tr><tr><td>

Active

</td><td>

Option to activate the scheduled job. Select this option.

</td></tr><tr><td>

Use connection

</td><td>

Leave this deactivated for the first run. Specifies another connection and credentials for this job.

</td></tr><tr><td>

Concurrent Import

</td><td>

Leave check box activated. Splits data into multiple imports sets. See the field message for more information.

</td></tr><tr><td>

Partition Method

</td><td>

Leave set as `Custom size`.

</td></tr><tr><td>

Partition Size

</td><td>

Leave set as `1,000`. Import set size for early scheduling.

</td></tr><tr><td>

Execute pre-import script

</td><td>

Leave check box selected. Specifies a script to run before the import is performed.

</td></tr><tr><td>

Execute post-import script

</td><td>

Leave check box selected. Specifies a script to run after the import is performed.

</td></tr></tbody>
</table>    3.  Right-click in the gray header titled Scheduled Data Import and select **Save**.

    4.  Select **Execute Now**.

        If you do not choose to run the job on-demand, the next job runs according to the schedule you set.

    5.  Select **Mark as complete** followed by **Continue**.

        The Home page of the Setup Assistant is displayed.

14. Add Multiple Instances

    1.  Select Add Multiple Instances to expand it.

        The following steps are displayed:

        -   Update Data Source Access
        -   Update Scheduled Data Import
        -   Add Another Connection
        -   Configure MID Server for New HTTP connection
        -   Test New Connections
    2.  To update the Data Source, follow the steps listed in step 8.

    3.  To update the Scheduled Data Import, follow the steps in step 9.

    4.  To add another connection, follow the steps listed in step 10.

    5.  To configure a MID Server, follow the steps listed in step 11.

    6.  To test connections, follow the steps listed in step 12.

15. On the Service Graph Connector for Qualys page for Guided Setup, select **Complete** to finish the configuration.


