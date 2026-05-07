---
title: Configure a new TAXII Feed
description: You can maintain TAXII feeds for sharing STIX-formatted information. Each TAXII feed contains one or more TAXII collections.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [About STIX TAXII, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure a new TAXII Feed

You can maintain TAXII feeds for sharing STIX-formatted information. Each TAXII feed contains one or more TAXII collections.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select the Integrations icon.

3.  Select **Threat Intel Feeds** &gt; **STIX TAXII** &gt; **TAXII Feeds**.

    **Note:** Configure TAXII feed to serve as a profile for all the TAXII Collections within.

4.  Select **Configure new source**.

    The Configure new TAXII Feed page is displayed.

5.  On the form, fill in the fields.

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

Source Type

</td><td>

Type of source provided for the feed. The available source types are:-   Government
-   ISACs
-   Open Source
-   Premium Source
-   Other Source


</td></tr><tr><td>

Logo

</td><td>

Logo of the source feed.

</td></tr><tr><td>

Industry

</td><td>

Industry category for which the feed data source is applicable.

</td></tr></tbody>
</table>    Fill in the fields in the Configuration section, as appropriate.

<table id="table_czj_zqd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TAXII Version

</td><td>

TAXII Version of the TAXII server to be configured. Supported versions are 2.0 and 2.1.

</td></tr><tr><td>

Configuration Type

</td><td>

Configuration type to fetch TAXII collections. Available values are:-   **Discovery Service URL**: Choose Discovery Service URL to fetch collections from all available API roots within the discovery service of the TAXII server.
-   **API Root URL**: Choose API Root URL to fetch collections from the specific API root of the TAXII server.


</td></tr><tr><td>

Authentication

</td><td>

Required option from the list if authentication is required. The available options are:-   **None**: Select this option if there is no authentication required.
-   **Basic**: Select this option to provide username and password.
-   **API Key**: Select this option to provide an API key.
-   **Choose a REST message**: Select this option for any other type of authentication. The REST message options are:
    -   **Use REST Message**: Select this check box if you need a REST message to build a pre-build REST Message. If you clear this check box, the system uses the value in the endpoint field. Select the lookup icon, and select the REST message from the list.
    -   **REST Method**: Select this check box if you need a REST method. Select the lookup icon, and select the REST method from the list.
**Note:** The REST message and REST method fields are set to available when the REST message option is selected.

</td></tr><tr><td>

URL

</td><td>

TAXII Server Discovery Service URL or specific API Root URL based on the selected configuration type.

</td></tr><tr><td colspan="2">

**Advanced section**

</td></tr><tr><td>

Advanced

</td><td>

Check box to choose a different Integration script and Report Processor. Verify the chosen scripts are compatible with the selected TAXII version. Based on the TAXII version and authentication, these scripts are auto populated by default.

</td></tr><tr><td>

Integration script

</td><td>

Invokes a call to the REST Endpoint URL API using authentication parameters. The script fetches observables or indicators STIX data available for the specific feed.**Note:** The fetched data is raw data only with no records created. The data is attached to the integration process and can be viewed under the **Integration Run** section.

The base system includes custom script includes provisioned within the application for integration scripts:

-   TAXIIV2\_0QueryParamAPIKeyIntegrationScript
-   TAXIIV2\_0BasicAuthIntegrationScript
-   TAXIIV2\_1QueryParamAPIKeyIntegrationScript
-   TAXIIV2\_1BasicAuthIntegrationScript
The default integration script is based on the selected feed type. The script include runs a simple REST call, saves the response as an attachment, and returns the attachment to the processor.

</td></tr><tr><td>

Report processor

</td><td>

The report processor invokes a call to the REST Endpoint URL.The base system includes the custom script include **TAXIIV2CollectionDataProcessor**, which is provisioned within the application for integration scripts.

</td></tr></tbody>
</table>    Fill in the fields in the Scheduling section, as appropriate.

<table id="table_yt1_rrd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run Frequency of Collections

</td><td>

Scheduling interval applied to the TAXII collection records. Run frequency for a TAXII collection can be modified in the TAXII collection form view if required.**Note:** This setting is applied as default to all fetched TAXII collections. There is an option to override the setting in TAXII Collections if required. TAXII

 For more information, see [Scheduled Jobs and how to Automatically run a script of your choosing](https://servicenow.com/docs/bundle/vancouver-platform-administration/page/administer/reference-pages/task/t_ScheduleAScriptExecution.html).

</td></tr><tr><td>

Fetch Data From

</td><td>

Start date from when the data needs to be fetched. Set this field with the time from when data needs to be ingested from the corresponding source. After setting this field, the next ingestion run fetches data from the configured time and consecutive runs fetch incremental data.For example, a source is scheduled to ingest data every hour. If you set **Fetch Data From** to Jan 12 6:00AM on Jan 12 9:30AM, the ingestion triggering on Jan 12 10:00AM fetches data from Jan 12 6:00AM to Jan 12 10:00AM. The next ingestion at 11:00AM fetches only incremental data from Jan 12 10:00AM to Jan 12 11:00AM.

**Note:** This means the scheduled runs will fetch data incrementally starting from the specified date onwards.

</td></tr></tbody>
</table>6.  Select **Validate Connection**

    An information message is displayed that the TAXII Feed connection is successful. To fetch the collections proceed to the next step.

7.  Select **Get TAXII Collections**.

    **Note:** If there are any errors, then an error message is displayed that an error occurred while fetching TAXII collections and check logs for more details.

    The TAXII Collections are displayed under the TAXII Collections section, and they are inactive by default.

8.  Enable the TAXII Collections to retrieve the STIX objects available in these TAXII collections.


**Parent Topic:**[About STIX TAXII](../concept/threat-intelligence-security-center-feeds.md)

