---
title: View Premium Threat Feed for CrowdStrike
description: The CrowdStrike feed enables users to ingest indicators, actors, reports, and their associated context from the CrowdStrike Falcon Intelligence feed into TISC.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [View Custom Feed, View Threat Intel Feeds, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# View Premium Threat Feed for CrowdStrike

The CrowdStrike feed enables users to ingest indicators, actors, reports, and their associated context from the CrowdStrike Falcon Intelligence feed into TISC.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations**.

2.  Select **Custom**.

3.  Click on the **Edit** button from the **CrowdStrike Feed** form page.

    **Note:** By default, the CrowdStrike feed is disabled, you must edit the configurations to enable the feed.

    ![CrowdStrike-Premium feed](../image/tisc-crowdstrike-premium-feed.png)

4.  Drill down to the **Configuration Details** section.

5.  Enter the **Client ID**, and **Client Secret**.

    **Note:**

    1.  You must generate your Client ID and Client Secret in case if you don't have it. For more information on the Client ID and Client Secret, see [Defining your first API Client](https://www.crowdstrike.com/blog/tech-center/get-access-falcon-apis/) section.
    2.  Get Client ID and Client Secret from CrowdStrike for required scopes. Below are the scopes that are required for the Client ID and Client Secret from CrowdStrike:
        -   Indicators \(Falcon intelligence\)
        -   Actors \(Falcon Intelligence\)
        -   Reports \(Falcon Intelligence\)
6.  Navigate to **Additional Settings** to configure the filters that will be applied while ingesting indicators from CrowdStrike.

    ![CrowdStrike additional settings tab](../image/tisc-crowdstrike-additional-settings.png)

    The **Additional Settings** tab is primarily used to configure the filters that control how data is ingested into the application.

    These filters allow you to customize the data integration process to meet your specific requirements, ensuring that only the most relevant information is included.

7.  Click **Edit Settings**.

    ![CrowdStrike additional settings tab - Edit](../image/tisc-crowdstrike-additional-settings-edit.png)

8.  Select the required filters.

    **Note:** All the filters configured will be applied in conjunction while ingesting indicators from CrowdStrike.

    The section below provides a detailed explanation of each available option. Review each option in the following table to understand how the filters can be applied to optimize the data ingested into the application.

9.  Select the required values from the below available filters.

<table id="table_flc_vxs_z2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Record types to ingest**

</td></tr><tr><td>

Select record types to ingest

</td><td>

Select the record types that you want to ingest. The available record types are Indicators, Reports, and Actors.**Note:**

If you select only **Indicators** as the record type to ingest, then the related Reports and Actors associated with those indicators will not be ingested automatically.

To ingest the related Reports and Actors, you must select all the three record types: Indicators, Reports, and Actors.

</td></tr><tr><td colspan="2">

**Filters on indicator attributes**

</td></tr><tr><td>

Include deleted indicators for ingestion

</td><td>

Select this check box to allow the ingestion of indicators that have been deleted.**Note:** Deleted indicators will be created as observables only if they were previously ingested. A **Deleted in CrowdStrike** tag is added to indicators that are removed from CrowdStrike.

</td></tr><tr><td>

Indicator types to ingest

</td><td>

Select the specific CrowdStrike indicator types you want to ingest. If none are selected, then all the available indicators will be retrieved by default.

</td></tr><tr><td>

Malicious confidence of indicators to ingest

</td><td>

Select the malicious confidence level of CrowdStrike indicators to ingest. If left blank, all indicators will be fetched from CrowdStrike regardless of their malicious confidence.

</td></tr><tr><td>

Targeted industries of indicators to ingest

</td><td>

Select the targeted industries associated with CrowdStrike indicators to ingest. If none is selected, all the indicators will be fetched from CrowdStrike regardless of targeted industry.

</td></tr><tr><td colspan="2">

**Filters on associated actors**

</td></tr><tr><td>

Fetch indicators only if actors associated to it

</td><td>

Select this check box to fetch indicators only if they are associated with actors.

</td></tr><tr><td>

Ingest indicators only associated to these actors

</td><td>

Specify comma-separated actor names related to the indicators for ingestion. If not provided, all the indicators will be fetched from CrowdStrike regardless of associated actors.

</td></tr><tr><td colspan="2">

Filters on associated reports

</td></tr><tr><td>

Fetch indicators only if reports associated to it

</td><td>

Select this check box to fetch indicators only if they are associated with reports.

</td></tr><tr><td>

Ingest indicators only associated to these reports

</td><td>

Enter comma-separated report names associated with the indicators for ingestion. If left blank, all the reports will be included in the ingestion process.If not provided, all the indicators will be fetched from CrowdStrike regardless of associated reports.

</td></tr><tr><td colspan="2">

**Filters on associated malware families**

</td></tr><tr><td>

Fetch indicators only if malware families associated to it

</td><td>

Select this check box to fetch indicators only if they are associated with malware families.

</td></tr><tr><td>

Ingest indicators only associated to these malware families

</td><td>

Enter comma-separated malware family names associated with the indicators for ingestion. If left blank, all malware families will be included in the ingestion process.If not provided, all the indicators will be fetched from CrowdStrike regardless of malware families.

</td></tr><tr><td colspan="2">

**Mapping of Indicator Malicious confidence to TISC confidence****Note:** The High, Medium, and Low values are the source value or malicious confidence received from CrowdStrike.

</td></tr><tr><td>

High

</td><td>

Enter a confidence value \(0–100\) for indicators with high malicious confidence. **Note:** If a matching malicious confidence mapping is found in the **Additional Settings**, it will override the value provided in the **Details** section even if a confidence value is manually entered.

</td></tr><tr><td>

Medium

</td><td>

Enter a confidence value \(0–100\) for indicators with medium malicious confidence.

</td></tr><tr><td>

Low

</td><td>

Enter a confidence value \(0–100\) for indicators with low malicious confidence.

</td></tr><tr><td>

Unverified

</td><td>

Enter a confidence value \(0–100\) for indicators with unverified malicious confidence.

</td></tr></tbody>
</table>    **Note:** With the same additional settings you’ve defined above, you can duplicate the feed when creating a new one.

10. Click **Update** on the **Additional Settings** dialog box to save the modified additional settings.

11. Click **Enable** to enable CrowdStrike Feed for ingestion.

    **Note:** The premium feed is same as other feeds except the response that is parsed during the configuration. A specific response is parsed to CrowdStrike by adding the Client ID and Client Secret.

    **What type of data is fetched from CrowdStrike:**

    1.  Indicators from CrowdStrike that are updated after the configured ingestion time and matching the filters configured as part of additional settings. These indicators from CrowdStrike will then be mapped to observables in TISC. Below are the indicator types that are ingested in TISC:
        -   SHA256 Hash
        -   MD5 Hash
        -   SHA1 Hash
        -   URL
        -   Domain
        -   IP Address
        -   Mutex Name
        -   File Name
        -   Email Address
        -   Username
        -   IP Address Block
    2.  Threat Actors from CrowdStrike that are updated after the configured ingestion time will be mapped to Threat Actors in TISC.
    3.  Reports from CrowdStrike that are updated after the configured ingestion time will be mapped to threat reports in TISC based on the matching attributes.
    4.  In addition to the entities mentioned above, the following related data is also fetched:

        1.  Threat actors, reports, and indicators related to the previously ingested indicators.
        2.  Threat actors and indicators associated with all reports ingested during the current ingestion process.
        **Note:** Filters configured in **Additional Settings** will also be applied when ingesting the indicators associated with the previously ingested indicators, reports, or actors.

12. Click **Duplicate** to duplicate the feed.

    For more information, see [Duplicate threat intelligence feeds](tisc-duplicate-feeds.md).


-   **[System Properties for CrowdStrike](../concept/premium-threat-feed-system-properties.md)**  
The following details the system properties for CrowdStrike.

**Parent Topic:**[View Custom Feed](view-oob-custom-feeds.md)

