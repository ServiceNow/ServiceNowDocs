---
title: Configure a new threat intelligence feed
description: Add external threat intelligence sources to your TISC environment. Configure feed parameters, authentication, scheduling, and data processing to automatically ingest threat indicators from various sources.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure a new threat intelligence feed

Add external threat intelligence sources to your TISC environment. Configure feed parameters, authentication, scheduling, and data processing to automatically ingest threat indicators from various sources.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **All** &gt; **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Integrations** icon.

3.  Select **Threat Intel Feeds** &gt; **All Feeds**.

4.  Select **Configure new source**.

    The various feed types are displayed.

    ![Select Feed Type dialog showing feed options with MISP selected.](../image/tisc-all-feeds-new-source.png)

5.  Select the required feed type.

6.  On the form, fill in the fields.

<table id="table_z5f_tqd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the feed.

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

Logo of the source feed.**Note:** The size must be 72px/72px.

</td></tr><tr><td>

Industry

</td><td>

Industry category for which the feed is applicable, such as Aerospace or Agriculture.

</td></tr><tr><td>

Source Type

</td><td>

Type of source. Available source types:-   Government
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

Number of days before ingested feed data expires. For example, 180.**Note:** Ingested data from the source expires 180 days after ingestion.

</td></tr><tr><td>

Override Source Expiration

</td><td>

When selected, the profile configuration overrides the expiration time on incoming feed records.

</td></tr><tr><td>

Use REST Message

</td><td>

When selected, uses REST Message/REST Method functionality provided by ServiceNow AI Platform.When cleared, the application uses the endpoint provided in **REST Endpoint URL** to fetch the data from the feed. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on ServiceNow AI Platform documentation.

**Important:** The REST message and REST method fields are mandatory when you select REST message.

</td></tr><tr><td>

REST Message

</td><td>

REST Message record from the list of REST message records configured in the instance. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on the ServiceNow AI Platform documentation.**Note:** Use this value to view specific headers and define REST related records using the REST message option.

</td></tr><tr><td>

REST Method

</td><td>

REST Method from the list of available REST Methods configured for the selected REST Message. For more information, see [Outbound REST web service](https://servicenow.com/docs/bundle/vancouver-api-reference/page/integrate/outbound-rest/concept/c_OutboundRESTWebService.html) on the ServiceNow AI Platform documentation.

</td></tr><tr><td>

REST endpoint URL

</td><td>

REST endpoint URL where the data is hosted by the threat intelligence feed.**Note:** For MISP feed types, the REST endpoint URLs that end with `/manifest.json` are only supported.

</td></tr><tr><td>

Confidence

</td><td>

Confidence for all applicable records ingested through this specific feed.**Note:** Specify the confidence between 0-100 for this source.

</td></tr><tr><td>

Override Source Confidence

</td><td>

When selected, the profile configuration overrides the feed's confidence value.

</td></tr><tr><td>

Data Parsing Mechanism

</td><td>

Data parsing mechanism. Available options:-   **Automated IoC Extraction**: This option is selected by default when configuring Text, CSV, or JSON feeds.
-   **Custom Field Mapping**: Use this option to define how specific fields in your feed data should be mapped to observable attributes.

Once selected, you can configure the mappings in the **Field Mapping** section. For more detailed information on the custom field mapping, see [Configure Custom Field Mapping](tisc-field-mapping.md).

</td></tr><tr><td>

Authentication Required

</td><td>

When selected, authentication is required for the new threat intelligence feed.**Note:** This is only applicable when REST Endpoint URL is being used to retrieve the data.

</td></tr><tr><td>

Authentication Type

</td><td>

Authentication type for the source feed. Available authentication types:-   API ID / API Key
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

When selected, allows you to define custom integration script and report processor script.**Note:** When this check box is selected, the **Integration script** and **Report Processor** fields displays for you to select the custom scripts.

</td></tr><tr><td>

Integration script

</td><td>

Integration script invokes a call to the REST Endpoint URL using the authentication parameters and the headers as configured in the feed, and then the script fetches the data that is available from the specific feed.Available custom script includes for integration scripts:

-   MITRESourceIntegration: Used to fetch the data from MITRE feeds.
-   RSSFeedDatasourceIntegration: Used to fetch the data from RSS feeds.
-   SimpleFeedDatasourceIntegration: Used to fetch the data from Simple feeds without authentication or Basic Authentication.
-   SimpleMISPFeedDatasourceIntegration: Used to fetch the data from hosted MISP feeds.
The default integration script is based on the feed type that you select. For example, if you select MISP feed type which is a standard format to process and fetch the data then the integrations script is **SimpleMISPFeedDatasourceIntegration**.

**Note:**

For the Custom integration scripts, you can create a script include by extending **FeedDatasourceIntegrationBase** and override the required methods.

</td></tr><tr><td>

Report processor

</td><td>

The report processor script processes data fetched from the feed using the integration script.

 Available custom scripts for report processor:

-   AtomFeedDatasourceResponseProcessor: Used to process RSS feeds in Atom format.
-   MITRECollectionDataProcessor: Used to process MITRE feeds.
-   RSSFeedDatasourceResponseProcessor: Used to process RSS feeds.
-   SimpleDataplaneFeedResponseProcessor: Used to process Dataplane feeds.
-   SimpleFeedDatasourceResponseProcessor: Used to process Simple feeds using regular expression extraction of observables.
-   SimpleFeodotrackerFeedResponseProcessor: Used to process Feodotracker feeds.
-   SimpleMISPFeedDatasourceResponseProcessor: Used to process hosted MISP feeds.
-   TAXIIV2CollectionDataProcessor: Used to process TAXII Collection data.
 The default report processor for MISP feeds is `SimpleMISPFeedDatasourceResponseProcessor`. This processor is preconfigured by the application and cannot be modified or replaced.

</td></tr></tbody>
</table>9.  Fill in the fields in the **Scheduling** section, as appropriate.

<table id="table_yt1_rrd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run

</td><td>

Frequency at which to ingest the records. The feed ingestion runs job and executes based on the scheduled job interval. The available job intervals are:-   Daily
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

Start date from which to fetch the data. Set this field to the time from which data should be ingested from the corresponding source. Once this value is set, the next ingestion run fetches the data from the configured time and consecutive ingestion runs fetch incremental data based on the Run frequency.For example, Source is scheduled to ingest the data every hour. The user sets **Fetch Data From** to Jan 12 6:00AM on Jan 12 9:30AM, the ingestion triggering on Jan 12 10:00AM would fetch the data from Jan 12 6:00AM to Jan 12 10:00AM. The next ingestion that triggers at 11:00AM would fetch only the incremental data from Jan 12 10:00AM to Jan 12 11:00AM.

**Note:** This means the scheduled runs will fetch data incrementally starting from the specified date onwards.

**Important:** The Fetch Data From field doesn't apply to Text, CSV, or JSON feeds.

</td></tr></tbody>
</table>    |Field|Description|
    |-----|-----------|
    |Media URL|URL of the media source used to retrieve threat intelligence feed data.|
    |Feed Comments URL|Link provided by the RSS source for comments.|

    |Field|Description|
    |-----|-----------|
    |Select TISC Tags|Tags to annotate or identify records ingested into the system from this source. Enter the tag name in the **Search** bar to choose available tags or enter a new tag name and select **Add** to assign it to the source.|

10. Select the **Save** action to store and create the feed.

    The system validates the provided details, and by default the feed status is inactive.

11. Select the **Save as Draft** action to only store the feed configurations as draft.

    You cannot enable a feed when it is saved as draft. Use this option when you're unsure about the configuration details.

12. Select **Enable** to enable the record.

    After the threat intelligence feed record is enabled, you can execute the record to run the integration.

    **Note:**

    -   The threat intelligence feed record is labeled and indicated as enabled. Similarly, you can disable the threat intelligence feed by selecting **Disable** button.
    -   You can also enable, disable, or delete a particular feed by using the **Actions** menu of the required feed tile on the **Catalog** or **Threat Intel Feeds** page.
13. Select **Delete** to delete the threat intelligence feed record.

14. Select **Integrations Run** section to verify the run details.

    **Note:** This configuration procedure applies to all threat intelligence feed types except STIX TAXII. For more information on how STIX TAXII is configured, see [Configure a new TAXII Feed](tisc-configure-a-new-taxii-feed.md).


**Parent Topic:**[Threat Intelligence Feeds](../concept/threat-intelligence-feeds.md)

