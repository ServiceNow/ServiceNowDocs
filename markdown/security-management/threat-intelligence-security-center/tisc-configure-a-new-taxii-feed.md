---
title: Configure a new TAXII Feed
description: You can maintain TAXII feeds for sharing STIX-formatted information. Each TAXII feed contains one or more TAXII collections.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2025-01-20"
reading_time_minutes: 5
breadcrumb: [Understanding STIX TAXII, Threat Intelligence Feeds, Integrating Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Configure a new TAXII Feed

You can maintain TAXII feeds for sharing STIX-formatted information. Each TAXII feed contains one or more TAXII collections.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Click on **Integrations** icon.

3.  Select **Threat Intel Feeds** &gt; **STIX TAXII** &gt; **TAXII Feeds**.

    **Note:** Configure TAXII feed to serve as a profile for all the TAXII Collections within.

4.  Click **Configure new source**.

    The Configure new TAXII Feed page is displayed.

5.  On the form, fill in the fields.

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

Source Type

</td><td>

The type of source such as Open Source, Premium Source, and so on provided for the feed. The available source types are:-   Government
-   ISACs
-   Open Source
-   Premium Source
-   Other Source


</td></tr><tr><td>

Logo

</td><td>

Attach the logo of the source feed.

</td></tr><tr><td>

Industry

</td><td>

Select the industry category such as Aerospace, Agriculture, and so on for which the feed data source is applicable to.

</td></tr></tbody>
</table>    Fill in the fields in the Configuration section, as appropriate.

<table id="table_czj_zqd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

TAXII Version

</td><td>

Select the TAXII Version of the TAXII server that needs to be configured. Supported versions are 2.0 and 2.1.

</td></tr><tr><td>

Configuration Type

</td><td>

Provide a configuration type to fetch TAXII collections. Available values are:-   **Discovery Service URL**: Choose Discovery Service URL to fetch collections from all available API roots within the discovery service of the TAXII server.
-   **API Root URL**: Choose API Root URL to fetch collections from the specific API root of the TAXII server.


</td></tr><tr><td>

Authentication

</td><td>

Select the required option from the drop down list if the authentication is required. The available options are:-   **None**: Select this option if there is no authentication required.
-   **Basic**: Select this option to provide username and password.
-   **API Key**: Select this option to provide an API key.
-   **Choose a REST message**: Select this option for any other type of authentication. The REST message options are:
    -   **Use REST Message**: Select this box if you need a REST message to build a pre-build REST Message. If you don't select then this will use the value in endpoint field. Click the lookup icon, and select the REST message from the list.
    -   **REST Method**: Select this box if you need a REST method. Click the lookup icon, and select the REST method from the list.
**Note:** The REST message and REST method fields become available when the REST message option is selected.

</td></tr><tr><td>

URL

</td><td>

Enter either the TAXII Server Discovery Service URL or specific API Root URL based on the selected configuration type.

</td></tr><tr><td colspan="2">

**Advanced section**

</td></tr><tr><td>

Advanced

</td><td>

Select the check box to choose a different Integration script and Report Processor. Make sure the chosen scripts are compatible with the selected TAXII version. Based on the TAXII version and authentication, these scripts are auto populated by default.

</td></tr><tr><td>

Integration script

</td><td>

Invokes a call to the REST Endpoint URL API using the authentication parameters such as authentication type: User name/Password/API Key and the headers to be passed with the request, and then the script fetches the observables or indicators STIX data that are available for the specific feed.**Note:** The data that is fetched is the raw data only \(no records are created\) which will be attached to the integration process and can then be viewed under the **Integration Run** section.

Within the base system following are the custom scripts includes, which are provisioned within the application for the integrations scripts:

-   TAXIIV2\_0QueryParamAPIKeyIntegrationScript
-   TAXIIV2\_0BasicAuthIntegrationScript
-   TAXIIV2\_1QueryParamAPIKeyIntegrationScript
-   TAXIIV2\_1BasicAuthIntegrationScript
The default integration script is based on the feed type that you select. The script includes runs a simple REST call, saves the response as an attachment, and then returns the attachment to the processor.

</td></tr><tr><td>

Report processor

</td><td>

The report processor invokes a call to the REST Endpoint URL.Within the base system below is the custom scripts includes, which is provisioned within the application for the integrations scripts, **TAXIIV2CollectionDataProcessor**.

</td></tr></tbody>
</table>    Fill in the fields in the Scheduling section, as appropriate.

<table id="table_yt1_rrd_pyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Run Frequency of Collections

</td><td>

The scheduling interval which will be applied to the TAXII collection records. Run frequency for a TAXII collection can be modified in the TAXII collection form view if required.**Note:** This setting will be applied as default to all the TAXII collections that are fetched. There is an option to override the setting in TAXII Collections if required.

 For more information, see [Scheduled Jobs and how to Automatically run a script of your choosing](https://servicenow.com/docs/bundle/vancouver-platform-administration/page/administer/reference-pages/task/t_ScheduleAScriptExecution.html).

</td></tr><tr><td>

Fetch Data From

</td><td>

The start date from when the data needed to be fetched. This field should be set with the time from when the data needs to be ingested from the corresponding source. Once this field is set, the next ingestion run would fetch the data from the configured time and consecutive ingestion runs would fetch incremental Data.For example, Source is scheduled to ingest the data every hour. The user sets **Fetch Data From** to Jan 12 6:00AM on Jan 12 9:30AM, the ingestion triggering on Jan 12 10:00AM would fetch the data from Jan 12 6:00AM to Jan 12 10:00AM. The next ingestion that triggers at 11:00AM would fetch only the incremental data from Jan 12 10:00AM to Jan 12 11:00AM.

**Note:** This means the scheduled runs will fetch data incrementally starting from the specified date onwards.

</td></tr></tbody>
</table>6.  Click **Validate Connection**

    An information message is displayed that the TAXII Feed connection is successful. To fetch the collections proceed to the next step.

7.  Click **Get TAXII Collections**.

    **Note:** If there are any errors, then an error message is displayed that an error occurred while fetching TAXII collections and check logs for more details.

    The TAXII Collections are displayed under the TAXII Collections section, and they are disabled by default.

8.  Enable the TAXII Collections to retrieve the STIX objects available in these TAXII collections.


**Parent Topic:**[Understanding STIX TAXII](../concept/threat-intelligence-security-center-feeds.md)

