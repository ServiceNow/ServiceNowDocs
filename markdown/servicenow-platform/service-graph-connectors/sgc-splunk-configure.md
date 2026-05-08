---
title: Configure the Service Graph Connector for Splunk
description: Configure your connections, set up scheduled imports, verify successful connections and optionally add multiple instances in the Guided Setup.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Splunk, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the Service Graph Connector for Splunk

Configure your connections, set up scheduled imports, verify successful connections and optionally add multiple instances in the Guided Setup.

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by ITOM Visibility or ITOM Discovery, these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

-   The [Integration Commons for CMDB](../../../configuration-management/concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../../../configuration-management/concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see Request Discovery.
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Optional: Only required for event ingestion. Observability Commons for CMDB \(sn\_observability\). If used, this app must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Splunk** &gt; **Setup** in the navigation panel in your instance.

2.  On the Welcome to Guided Setup Home page, select **Continue**.

3.  On the Experience page that is displayed, select **Best Experience** followed by **Continue**.

    On the Service Graph Connector for Splunk page, there are three tasks displayed:

    -   Configure the connection
    -   Add multiple instances
    -   Set up scheduled import jobs
4.  Select **Configure the connection** to expand it.

    There are three tasks:

    -   Configure Splunk authentication credentials
    -   Configure Splunk HTTP Connection
    -   Test Connection
5.  Select **Configure Splunk authentication credentials** and fill in the fields.

    1.  Enter a name for the credentials, for example **SG-Splunk Credentials**.

    2.  Verify the **Active** check box is selected.

    3.  Enter your User name and Password for your Splunk instance.

    4.  Leave the other field values in their current settings.

    5.  Right-click in the gray header titled Basic Auth Credentials and select **Save**.

    6.  Select **Mark as complete** followed by **Continue**.

        The Configure Splunk HTTP Connection page is displayed.

6.  Configure the Splunk HTTP connection.

    1.  Fill in the fields.

<table id="id_nmr_s2d_r1c"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Connection name, `SG-Splunk Connection`, for example.

</td></tr><tr><td>

Active

</td><td>

Selected.

</td></tr><tr><td>

Credential

</td><td>

Credentials to use for the connection. Select one from the list.

</td></tr><tr><td>

Domain

</td><td>

global.

</td></tr><tr><td>

Connection alias

</td><td>

Select one from the list. **sn\_sec\_sgc\_splunk.SGSplunk**, for example

</td></tr><tr><td>

URL builder

</td><td>

Select the check box. Fill in the new fields.

</td></tr><tr><td>

Host

</td><td>

Splunk domain part of the URL without the 'https'. An example might be `splunk3.com` or an IP address.

</td></tr><tr><td>

Override default port

</td><td>

The Splunk instance port,`8089`, for example.

</td></tr><tr><td>

Protocol

</td><td>

https.

</td></tr><tr><td>

\(Optional\) Use MID server

</td><td>

Select the check box for a dedicated MID Server for the connection, if available.1.  Select **Specific MID Server** from the MID Selection drop down list.
2.  Select a MID Server from the list.
**Note:** A MID Server is required for on-premise connections if the connection is not publicly accessible.

</td></tr></tbody>
</table>    2.  Right-click in the gray header titled HTTP\(s\) Connection and select **Save**.

    3.  Select **Mark as complete** followed by **Continue**.

        The Test Connection page is displayed.

    4.  Set the flag for the **is the servicenow addon installed** \(**is\_snow\_addon\_installed**\).

        By default, the property on the Service Graph Connection Properties tab is set to **false**.

<table id="table_r21_5zc_r1c"><thead><tr><th>

Option

</th><th>

Description

</th></tr></thead><tbody><tr><td>

false

</td><td>

The default query is set to extract only essential information about the forwarder that includes the host name and the operating system.​

</td></tr><tr><td>

true

</td><td>

The query offers more information about the forwarder along with extensive asset details via the ServiceNow add-on. This data is imported only if the add-on is installed on the Splunk instance.

</td></tr></tbody>
</table>7.  Test the connection.

    1.  Select the **Test Connection** link under Related Links.

        If the connection is successful, `201` is displayed in the Status Code field and a message is displayed after a few moments. If your connection test fails, review the Message and Suggestion fields for how to proceed.

    2.  After a successful test, right-click in the gray header titled Service Graph Connections and select **Save**.

    3.  Select **Mark as complete** followed by **Continue**.

        The steps for Add Multiple Instances is displayed. To add multiple instances, proceed to step 9. This step is optional and you might prefer to wait after you confirm you can import data before setting up multiple instances. To set the import schedule, follow the steps below.

8.  To configure the scheduled job, select **Set up scheduled import jobs** from the drop down list under Add Multiple Instances in the header.

    1.  On the Configure the scheduled jobs page, select a record under Scheduled Data Imports.

    2.  Select the frequency from the list for the Run field.

        If you want to run a test import prior to scheduling it, you might prefer to select **Once**.

    3.  Select the **Active** box to activate the scheduled job.

    4.  Edit the fields as required.

        You might prefer to leave these fields in their default settings for the first few runs to confirm data imports.

        |Field|Value|
        |-----|-----|
        |Name|Unique Name for scheduled job.|
        |Application|Read-only: Service Graph Connector for Splunk|
        |Data source|Data source used.|
        |Run as|Run the scheduled job with the credentials of another specified user.|
        |Time|When you want the job to run.|
        |Conditional|Specific conditions under which this job is run.|
        |Use connection|Leave this check box deactivated for the first run. Specifies another connection and credentials for this job.|
        |Concurrent import|Leave check box activated. Splits data into multiple imports sets. See the field message for more information.|
        |Partition Method|Leave as `Custom size`.|
        |Partition size|15,000. Leave this value for the import set size for early scheduling.|
        |Execute pre-import script|Leave check box activated. Specifies a script to run before the import is performed.|
        |Execute post-import script|Leave check box activated. Specifies a script to run after the import is performed.|

    5.  Select **Execute now** to run the job.

        If you do not choose to run the job on-demand, the next job runs according to the schedule you set.

    6.  Right-click in the gray header titled Scheduled Data Import and select **Save**.

    7.  Select **Mark as complete** followed by **Continue**.

        The main task page is displayed.

9.  To add multiple instances, select **Update Data Sources**.

    When indicated, follow the steps listed at the top of the page to switch the application scope with the application picker to open, edit, and save the record.

    1.  On the Update Data Source Access page, select **Data Source**.

    2.  On the page that is displayed, select the **Application Access** tab.

    3.  Review the access settings and update as needed.

    4.  Right-click in the gray header titled Table and select **Save**.

    5.  Select **Mark as complete** followed by **Continue**.

    6.  On the **Update Schedule Data Import** record, select **Schedule Data Import** to open it.

    7.  Select the **Application Access** tab to view the permission settings.

    8.  When you are satisfied with the settings, right-click in the gray header titled Tables and select **Save**.

    9.  Select **Mark as complete** followed by **Continue**.

    10. Follow the steps listed at the top of the page to switch the application scope with the application picker to open, edit, and save the record.

    11. On the Add Another Connection page, select the **Click here** link.

        The Flow Designer connection page is displayed and you can create a new connection.

    12. From this page, select **Add Connection**.

    13. Fill in the fields with your connection information.

        |Field|Description|
        |-----|-----------|
        |Splunk Connection name|Unique name for your connection.|
        |Splunk Connection URL|Connection URL in https format.|
        |User name|Splunk user name.|
        |Password|Splunk password.|

    14. Select **Create Connection**.

        Your connections are displayed on the page.

    15. On the Add Multiple Instance page, select **Mark as complete** followed by **Continue**.

        The Configure MID Server for New HTTP Connection page is displayed.

    16. Locate your new connection and select it to open the record.

        The connection URL is displayed in the Connection URL field.

    17. Select the Use MID server check box to add a MID Server.

        1.  Select **Specific MID Server** from the MID Selection drop down list.
        2.  Select a MID Server from the list.
    18. Right-click in the gray header titled HTTP\(s\) Connection and select **Save**.

    19. Select **Mark as complete** followed by **Continue**.

        The Test New Connections page is displayed.

10. Test the new connection.

    1.  Scroll and select the connection you want to test.

    2.  Select the **Test Connection** link under Related Links.

        If the connection is successful, `201` is displayed in the Status Code field and a message is displayed after a few moments. If your connection test fails, review the Message and Suggestion fields for how to proceed.

    3.  After a successful test, right-click in the gray header titled Service Graph Connections and select **Save**.

    4.  Select **Mark as complete** followed by **Continue**.

        The Configure the scheduled jobs page is displayed

    5.  On the Service Graph Connector for Splunk page for Guided Setup, select **Complete** to finish the configuration.


