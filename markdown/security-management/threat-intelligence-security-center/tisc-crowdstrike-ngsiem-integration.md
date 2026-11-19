---
title: Configure CrowdStrike NextGen SIEM sighting search
description: Configure the CrowdStrike NextGen SIEM integration with your Falcon API credentials so that analysts can search CrowdStrike log data for activity that matches an observable.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/threat-intelligence-security-center/tisc-crowdstrike-ngsiem-integration.html
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-12"
reading_time_minutes: 2
keywords: [configure, crowdstrike, nextgen siem, sighting search]
breadcrumb: [Get started with Sighting Search Configurations, Configure Sighting Search, TISC Enrichment integrations, TISC Integrations, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure CrowdStrike NextGen SIEM sighting search

Configure the CrowdStrike NextGen SIEM integration with your Falcon API credentials so that analysts can search CrowdStrike log data for activity that matches an observable.

## Before you begin

Download CrowdStrike NextGen SIEM integration from the ServiceNow Store and install it.

Role required: sn\_sec\_tisc.admin

**Important:**

-   Obtain the CrowdStrike API base URL, client ID, and client secret from your Falcon subscription.
-   To add a link from each sighting back into the Falcon console, obtain the Falcon console URL. This URL is different from the API base URL.

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center**.

2.  Select **Integrations** &gt; **Enrichment Integrations** &gt; **Sighting Search**.

3.  Select **Configure new enrichment**.

4.  In the configuration window, select CrowdStrike NextGen SIEM.

5.  In **Enrichment Integration**, enter the **Name** and **Description**.

    The **Integration Category**, **Integration type**, and **Vendor Name** fields are read-only.

6.  Complete the integration configuration fields.

<table id="table_csngsiem_config_fields"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

CrowdStrike API Base URL

</td><td>

Base URL of the CrowdStrike API for your Falcon cloud region.

</td></tr><tr><td>

Console URL

</td><td>

Base URL of the Falcon web console. Used only to build the sighting search link on each sighting so that an analyst can reopen the same search in Falcon. If this field is empty, no link is added.

</td></tr><tr><td>

Repository

</td><td>

List of Falcon repositories to run the search, for example:-   search-all
-   investigate\_view
-   third-party
-   falcon\_for\_it\_view
-   forensics\_view
-   3pi\_parsers


</td></tr><tr><td>

Client ID

</td><td>

Client ID of the OAuth 2.0 client credentials grant.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret of the OAuth 2.0 client credentials grant. The value is stored encrypted.

</td></tr><tr><td>

Max Result

</td><td>

Maximum number of log events that a sighting search returns.

</td></tr><tr><td>

Default lookback period for automated runs \(days\)

</td><td>

Default number of days of log data that a sighting search covers. A run-time search window overrides this value. Default value is 7.

</td></tr><tr><td>

Include raw data samples in search results

</td><td>

Select this option to store the matched raw events and attach them to the sighting record as a JSON file. When the option is cleared, only counts, and occurrences are kept.

</td></tr></tbody>
</table>    **Note:**

    The API base URL, client ID, and client secret are required. The remaining fields are optional and fall back to their default values.

7.  Save the configuration tile.

8.  Select **Enable** to turn on the configuration.


## Result

When a sighting search against CrowdStrike NextGen SIEM finds a match, the result is saved as a Sighting record. Open the record to view the Sighting Configuration Items related list, which shows the configuration items \(CIs\) associated with the sighting. The system uses *ComputerName* if available; otherwise, it uses the *host* field.

## What to do next

Select one or more CI rows from the Sighting Configuration Items list and select **Add As Configuration Item**to link the selected CI\(s\) to the sighting's Observable record. These records appear under the **Related Configuration Items** related list on the Observable form. For information on how to run a sightings search, see [Run Sighting Search](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-run-sighting-search.md).

**Parent Topic:**[Get started with Sighting Search Configurations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/threat-intelligence-security-center/tisc-get-sighting-configs.md)

