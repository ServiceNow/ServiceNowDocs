---
title: Configure a new threat intelligence feed
description: Configure a new threat intelligence feed.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure a new threat intelligence feed

Configure a new threat intelligence feed.

## Before you begin

Role required: sn\_sec\_tisc.admin

To configure a new threat intelligence feed, follow the procedure:

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Integrations** icon.

3.  Select **Threat Intel Feeds** &gt; **All Feeds**.

4.  Select **Configure new source**.

    The various feed types are displayed.

    ![TISC All Feeds - Configure new source](../image/tisc-all-feeds-new-source.png)

5.  Select the respective feed type.

6.  On the form, fill in the fields.

<table id="table_z5f_tqd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the feed.

</td></tr><tr><td>

Description

</td><td>

Description of the feed.

</td></tr><tr><td>

Feed Type

</td><td>

The feed type. For example, MISP.By default, this value is displayed based on the type of feed that you selected from the Catalog.

</td></tr><tr><td>

Logo

</td><td>

Attach the logo of the source feed.**Note:** The size should be 72px/72px.

</td></tr><tr><td>

Industry

</td><td>

Select the industry category such as Aerospace, Agriculture, and so on for which the feed is applicable to.

</td></tr><tr><td>

Source Type

</td><td>

Select the type of source from the list of available source types. List of available sources are:-   Government
-   ISACs
-   Open Source
-   Premium Source
-   Other Source


</td></tr></tbody>
</table>7.  Select **Select**.

8.  Fill in the fields in the Configuration section, as appropriate.

<table id="table_czj_zqd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Expiry period \(days\)

</td><td>

Enter the expiry period for the feed in days. For example, 180 days.**Note:** Data that is ingested from the source will be expired 180 days after the ingestion.

</td></tr><tr><td>

Override Source Expiration

</td><td>

When enabled, the feed record received will have its expiration time overridden to match the profile’s configuration.

</td></tr><tr><td>

Use REST Message

</td><td>

Select **Use REST Message** check box if you need to use REST Message/REST Method functionality that is provided by ServiceNow AI Platform.If this check box is not selected, then the application uses the endpoint provided in **REST Endpoint URL** to fetch the data from the feed. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on ServiceNow AI Platform documentation.

**Important:** The REST message and REST method fields are mandatory when you select REST message.

</td></tr><tr><td>

REST Message

</td><td>

Select the REST Message record from the list of REST message records which are already configured in the instance. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on the ServiceNow AI Platform documentation.**Note:** Select this value when you need to view specific headers, and define the REST related records using the REST message option.

</td></tr><tr><td>

REST Method

</td><td>

Select REST Method from the list of available REST Methods configured for the selected REST Message. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on the ServiceNow AI Platform documentation.

</td></tr><tr><td>

REST endpoint URL

</td><td>

Enter the REST endpoint URL where the data is hosted by the threat intelligence feed.**Note:** For MISP feed types, the REST endpoint URLs that end with `/manifest.json` are supported.

</td></tr><tr><td>

Confidence

</td><td>

Set the confidence for all the applicable records that are ingested through this specific feed.**Note:** Set the confidence between 0-100 for this source.

</td></tr><tr><td>

Override Source Confidence

</td><td>

When enabled, the feed will have its confidence value overridden to match the profile’s configuration.

</td></tr><tr><td>

Data Parsing Mechanism

</td><td>

Select the appropriate data parsing mechanism option. The available options are:-   **Automated IoC Extraction**: This option is selected by default when configuring Text, CSV, or JSON feeds.
-   **Custom Field Mapping**: Select this option if you want to define how the specific fields in your feed data should be mapped to the observable attributes.

Once selected, you can configure the mappings in the **Field Mapping** section. For more detailed information on the custom field mapping, see [Configure Custom Field Mapping](tisc-field-mapping.md).

**Note:** The data parsing mechanism option is only available for Text, CSV, and JSON feeds, where the feeds **Report Processor** is set to `SimpleFeedDatasourceResponseProcessor`.

</td></tr><tr><td>

Authentication Required

</td><td>

Select this check box if authentication is required for your new threat intelligence feed.**Note:** This is only applicable when REST Endpoint URL is being used to retrieve the data.

</td></tr><tr><td>

Authentication Type

</td><td>

The authentication type for the source feed. Following are the authentication types that are configured and provisioned within the base system for the users:-   API ID / API Key
-   API ID / API Secret
-   API Key
-   API Key / API Secret
-   API Username / API Password / API Key
-   Basic Authentication


</td></tr><tr><td>

Headers to be passed with request

</td><td>

Any headers to be passed with the requests can be provided in Request Header Mapping.-   Header should be provided in key-value pair separated by colon\(':'\).
-   Each header key value pair should be provided in a new line.
-   For providing authentication parameters as header values, enclose the required Authentication Label with '$\{' and '\}$'. For example, x-api-key:$\{API Key\}$.


</td></tr><tr><td>

Advanced

</td><td>

Select this check box to define custom integration script and report processor script.**Note:** When you select this check box, the **Integration script** and **Report Processor** fields will appear for you to select the custom scripts.

</td></tr><tr><td>

Integration script

</td><td>

Integration script invokes a call to the REST Endpoint URL using the authentication parameters and the headers as configured in the feed, and then the script fetches the data that is available from the specific feed.Within the base system following are the custom scripts includes available, which are provisioned within the application for the integrations scripts:

-   MITRESourceIntegration: Used for fetching the data from MITRE feeds.
-   RSSFeedDatasourceIntegration: Used for fetching the data from RSS feeds.
-   SimpleFeedDatasourceIntegration: Used for fetching the data from Simple feeds without authentication or Basic Authentication.
-   SimpleMISPFeedDatasourceIntegration: Used for fetching the data from hosted MISP feeds.
The default integration script is based on the feed type that you select. For example, if you select MISP feed type which is a standard format to process and fetch the data then the integrations script is **SimpleMISPFeedDatasourceIntegration**.

**Note:**

For the Custom integration scripts, you can create a script include by extending **FeedDatasourceIntegrationBase** and override the required methods.

</td></tr><tr><td>

Report processor

</td><td>

The report processor script processes data fetched from the feed using the integration script.

 The base system includes the following custom scripts, which are provisioned within the application to support report processor script:

-   AtomFeedDatasourceResponseProcessor: Used for processing RSS feeds in Atom format.
-   MITRECollectionDataProcessor: Used for processing MITRE feeds.
-   RSSFeedDatasourceResponseProcessor: Used for processing RSS feeds.
-   SimpleDataplaneFeedResponseProcessor: Used for processing Dataplane feeds.
-   SimpleFeedDatasourceResponseProcessor: Used for processing Simple feeds using regular expression extraction of observables.
-   SimpleFeodotrackerFeedResponseProcessor: Used for processing Feodotracker feeds.
-   SimpleMISPFeedDatasourceResponseProcessor: Used for processing hosted MISP feeds.
-   TAXIIV2CollectionDataProcessor: Used for processing TAXII Collection data.
 The default report processor for MISP feeds is `SimpleMISPFeedDatasourceResponseProcessor`. This processor is preconfigured by the application and cannot be modified or replaced.

</td></tr></tbody>
</table>9.  Fill in the fields in the Scheduling section, as appropriate.

<table id="table_yt1_rrd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run

</td><td>

Set the frequency at which you want to ingest the records. The feed will run and execute based on the scheduled job interval. The available job intervals are:-   Daily
-   Weekly
-   Monthly
-   Periodically
-   Once
-   On Demand
-   Business Calendar: Entry Start
-   Business Calendar: Entry End
**Note:** By default, the frequency is set to On Demand.

 For more information, see [Scheduled Jobs and how to Automatically run a script of your choosing](https://servicenow.com/docs/bundle/vancouver-platform-administration/page/administer/reference-pages/task/t_ScheduleAScriptExecution.html).

</td></tr><tr><td>

Fetch Data From

</td><td>

The start date from when the data needed to be fetched. This field should be set with the time from when the data needs to be ingested from the corresponding source. Once this value is s, the next ingestion run would fetch the data from the configured time and consecutive ingestion runs would fetch incremental Data based on the Run frequency?.For example, Source is scheduled to ingest the data every hour. The user sets **Fetch Data From** to Jan 12 6:00AM on Jan 12 9:30AM, the ingestion triggering on Jan 12 10:00AM would fetch the data from Jan 12 6:00AM to Jan 12 10:00AM. The next ingestion that triggers at 11:00AM would fetch only the incremental data from Jan 12 10:00AM to Jan 12 11:00AM.

**Note:** This means the scheduled runs will fetch data incrementally starting from the specified date onwards.

**Important:** Also, this is not applicable for Text, CSV, and JSON feeds.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Media URL|Indicates the feed URL.|
    |Feed Comments URL|The link provided by the RSS source.|

    |Field|Description|
    |-----|-----------|
    |Select TISC Tags|Use the tags to annotate or earmark records that are ingested into the system from this source. Start entering the tag name in the **Search** bar to choose the available tags in the application or enter new tag name and click **Add** to assign it to the source.|

10. Select the **Save** action to store and create the feed.

    The provided details are validated, and by default the feeds status is disabled.

11. Select the **Save as Draft** action to only store the feed configurations as draft.

    Users cannot enable a feed when it is saved in draft. i Use the **Save as Draft** option if you're unsure about the configuration details. After you get the configuration details, you can fill the remaining information in the draft version and create it.

12. Select **Enable** to enable the record.

    After the threat intelligence feed record is enabled, you can execute the record to run the integration.

    **Note:**

    -   The threat intelligence feed record is labeled and indicated as **enabled**. Similarly, you can disable the threat intelligence feed by clicking **Disable** button.
    -   You can also enable, disable, or delete a particular feed by using the **Actions** menu of the required feed tile on the **Catalog** or **Threat Intel Feeds** page.
13. Select select **Delete** to delete the threat intelligence feed record.

14. Select **Integrations Run** section to verify the run details.

    **Note:** The threat intelligence feed configuration procedure is same for all other threat intelligence feed types, except for STIX TAXII. For more information on how STIX TAXII is configured, see [Configure a new TAXII Feed](tisc-configure-a-new-taxii-feed.md).


**Parent Topic:**[Threat Intelligence Feeds](../concept/threat-intelligence-feeds.md)

