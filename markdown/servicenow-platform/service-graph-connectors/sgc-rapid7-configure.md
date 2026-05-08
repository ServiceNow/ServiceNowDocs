---
title: Configure the Service Graph Connector for Rapid7
description: Configure your connections, set up scheduled imports, verify successful connections and optionally add multiple instances in the Guided Setup.
locale: en-US
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Rapid7, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Configure the Service Graph Connector for Rapid7

Configure your connections, set up scheduled imports, verify successful connections and optionally add multiple instances in the Guided Setup.

## Before you begin

To use this Service Graph Connector, you need a subscription to a Subscription Unit that is based in the IT Operations Management \(ITOM\) Visibility application or in the ITOM Discovery application. As defined in the section titled "Managed IT Resource Types" in [ServiceNow Subscription Unit Overview](https://www.servicenow.com/products/entitlements-packages.html) for your subscription, for managed IT resources that are created or modified in the CMDB by this Service Graph Connector, but that aren’t yet managed by ITOM Visibility or ITOM Discovery, these resources will increase Subscription Unit consumption from that application. Review your current Subscription Unit consumption within ITOM Visibility or ITOM Discovery to ensure available capacity.

-   The [Integration Commons for CMDB](../../../configuration-management/concept/integration-commons-for-cmdb.md) store app, which is automatically installed.
-   The CMDB CI class models store app, which is automatically installed. See [CMDB CI Class Models app](../../../configuration-management/concept/cmdb-ci-class-models.md).
-   The ITOM Discovery License plugin \(com.snc.itom.discovery.license\). You must activate this plugin.
-   ITOM Licensing plugin \(com.snc.itom.license\). For more information, see Request Discovery.
-   The Datastream Action plugin \(com.glide.hub.action\_type.datastream\), which is automatically installed.
-   Observability Commons for CMDB \(sn\_observability\), which is only required for event ingestion. This app must be installed prior to installing the connector for Event Management to work. For more information, see [Observability Commons for CMDB](https://store.servicenow.com/sn_appstore_store.do#!/store/application/97e04562072020107add6a77c4a9351a) on the ServiceNow Store.

Roles required:

-   admin for tasks in the Guided Setup
-   insightIDR viewer role for the API token

## Procedure

1.  Navigate to **All** &gt; **Service Graph Connectors** &gt; **Rapid7** &gt; **Setup** in the navigation panel in your instance.

2.  On the Welcome to Guided Setup Home page, select **Continue**.

3.  On the Experience page that is displayed, select **Best Experience** followed by **Continue**.

    On the Service Graph Connector for Rapid7 page, there are three tasks displayed:

    -   Configure the connection
    -   Add multiple instances
    -   Set up scheduled imports
4.  Select **Configure the connection** to expand it.

    There are three steps:

    -   Configure Rapid7 authentication credentials
    -   Configure Rapid7 HTTP Connection
    -   Test Connection
5.  Select **Configure Rapid7 authentication credentials** and fill in the fields.

    1.  Enter a name for the credentials, for example **SGRapid7.Credential**.

    2.  Verify the **Active** check box is selected.

    3.  In the API Key field, enter your Rapid7 InsightVM API key.

    4.  Leave the other field values in their current settings.

    5.  Right-click in the gray header titled API Key Credentials and select **Save**.

    6.  Select **Mark as complete** followed by **Continue**.

        The Configure Rapid7 HTTP Connection page is displayed.

6.  Configure Rapid7 HTTP Connection.

    1.  Fill in the fields,

        |Field|Value|
        |-----|-----|
        |Name|Connection name, `SGRapid7`, for example.|
        |Active|Selected.|
        |Credential|Credentials to use for the connection. Select one from the list.|
        |Connection alias|Select one from the list. **sn\_sec\_sgc\_rapid7.SGRapid7**, for example|
        |URL builder|Select the check box. Fill in the new fields.|
        |Connection URL|URL that includes 'https', for example, https://us.api.insight.rapid7.com|
        |Host|Rapid7 domain part of the URL without the 'https'. An example might be `us.api.insight.rapid7.com`.|
        |Protocol|`https`|

    2.  Right-click in the gray header titled HTTP\(s\) Connection and select **Save**.

    3.  Select **Mark as complete** followed by **Continue**.

        The Test Connection page is displayed.

7.  Test the connection.

    1.  Select the **Test Connection** link under Related Links.

        If the connection is successful, `200` is displayed in the Status Code field and a message is displayed. If your connection test fails, review the Message and Suggestion fields for how to proceed.

    2.  Right-click in the gray header titled Service Graph Connections and select **Save**.

    3.  Select **Mark as complete** followed by **Continue**.

        The steps for Add Multiple Instances is displayed. This step is optional and you might prefer to wait after you confirm you can import data before setting up multiple instances.

8.  To configure the scheduled job, navigate back to the Guided Setup page and select **Set up scheduled import jobs**.

    1.  Follow the steps listed at the top of the page to switch the application scope with the application picker to open, edit, and save the record.

        You must select the Active check box to activate the scheduled job.

    2.  Select a record.

    3.  Fill in the fields.

        |Field|Value|
        |-----|-----|
        |Name|Unique Name for scheduled job.|
        |Application|Read-only: Service Graph Connector for Rapid7.|
        |Data source|Data source used.|
        |Run|How often you want the job to run. If you want to run a test import prior to scheduling it, you might prefer to select **Once**.|
        |Run as|Run the scheduled job with the credentials of another specified user.|
        |Time|When you want the job to run.|
        |Active|Select the check box to activate the job.|
        |Conditional|Specific conditions under which this job is run.|
        |Use connection|Leave this check box deactivated for the first run. Specifies another connection and credentials for this job.|
        |Concurrent import|Leave check box activated. Splits data into multiple imports sets. See the field message for more information.|
        |Partition Method|Leave as `Custom size`.|
        |Partition size|15,000. Leave this value for the import set size for early scheduling.|
        |Execute pre-import script|Leave check box activated. Specifies a script to run before the import is performed.|
        |Execute post-import script|Leave check box activated. Specifies a script to run after the import is performed.|

    4.  Select **Execute now** to run the job.

        If you do not choose to run the job on-demand, the next job runs according to the schedule you set.

    5.  Right-click in the gray header titled Scheduled Data Imports and select **Save**.

    6.  Select **Mark as complete** followed by **Continue**.

9.  Return to Guided setup and add multiple instances.

    When indicated, follow the steps listed at the top of the page to switch the application scope with the application picker to open, edit, and save the record.

10. Select **Update Data Sources**.

    1.  On the Update Data Source Access page, select **Data Source**.

    2.  On the page that is displayed, select the **Application Access** tab.

    3.  Review the access settings and update as needed.

    4.  Right-click in the gray header titled Table and select **Save**.

    5.  Select **Mark as complete** followed by **Continue**.

    6.  Select Schedule **Update Schedule Data Import**.

    7.  Select the **Application Access** tab to view the permission settings.

    8.  When you are satisfied with the settings, right-click in the gray header titled Tables and select **Save**.

    9.  Select **Mark as complete** followed by **Continue**.

    10. Follow the steps listed at the top of the page to switch the application scope with the application picker to open, edit, and save the record.

    11. On the Add Another Connection page, select the **Click here** link.

        The Workflow Studio connection page is displayed and you can create a new connection.

    12. From this page, select **Add Connection**.

    13. Fill in the fields with your connection information.

        |Field|Description|
        |-----|-----------|
        |Rapid7 Connection name|Unique name for your connection.|
        |Rapid7 Connection URL|Connection URL.|
        |API Key|Rapid7 API key.|

    14. Select **Create Connection**.

        Your connections are displayed on the Rapid7 page.

    15. Select **Mark as complete** followed by **Continue**.

        The Test New Connections page is displayed. Locate your new connection and note the status is '`Pending`'.

    16. Scroll and select the **Test Connection** link.

        If the connection is successful, 200 is displayed in the Status Code field and a message is displayed. If your connection test fails, review the Message and Suggestion fields for how to proceed.

    17. Right-click in the gray header titled Service Graph Connections and select **Save**.

    18. Select **Mark as complete** followed by **Continue**.

        The Configure the scheduled jobs page is displayed.

    19. Repeat the steps listed previously in step 8.

    20. On the Service Graph Connector for Rapid7 page for Guided Setup, select **Complete** to finish the configuration.


