---
title: Configure Premium Threat Feed for CrowdStrike
description: The CrowdStrike feed enables users to ingest indicators, actors, reports, malware, vulnerabilities, and their associated context from the CrowdStrike Falcon Intelligence feed into TISC.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/premium-threat-feed-for-crowdstrike.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-08-17"
reading_time_minutes: 7
breadcrumb: [View Custom Feed, View Threat Intel Feeds, Threat Intelligence Feeds, Integrate, Threat Intelligence Security Center, Security Operations]
---

# Configure Premium Threat Feed for CrowdStrike

The CrowdStrike feed enables users to ingest indicators, actors, reports, malware, vulnerabilities, and their associated context from the CrowdStrike Falcon Intelligence feed into TISC.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Integrations**.

2.  Select **Custom**.

3.  On the **CrowdStrike Feed** form page, select **Edit**.

    **Note:** By default, the CrowdStrike feed is disabled. Edit the configurations to enable the feed.

    \[Omitted image "tisc-crowdstrike-premium-feed.png"\] Alt text: CrowdStrike-Premium feed

4.  Select **Details**.

5.  Enter the **Client ID**, and **Client Secret**.

    **Note:**

    1.  Generate your Client ID and Client Secret if you don't have them. For more information on the Client ID and Client Secret, see [Defining your first API Client](https://www.crowdstrike.com/blog/tech-center/get-access-falcon-apis/) section.
    2.  Get Client ID and Client Secret from CrowdStrike for required scopes. The following scopes are required for the Client ID and Client Secret from CrowdStrike:
        -   Indicators \(Falcon intelligence\)
        -   Actors \(Falcon Intelligence\)
        -   Reports \(Falcon Intelligence\)
        -   Malware Families \(Falcon Intelligence\)
        -   Vulnerabilities \(Falcon Intelligence\)
6.  Select **Additional Settings** to configure the filters to apply while ingesting indicators from CrowdStrike.

    \[Omitted image "tisc-crowdstrike-additional-settings.png"\] Alt text: CrowdStrike additional settings tab

    These filters allow you to customize the data integration process to meet your specific requirements, ensuring that only the most relevant information is included.

7.  Select **Edit Settings**.

8.  Select the required filters.

    **Note:** All configured filters are applied together while ingesting indicators from CrowdStrike.

    The following section provides a detailed explanation of each available option. Review each option in the following table to understand how filters optimize data ingestion.

9.  Select the required values from the available filters.

<table id="table_flc_vxs_z2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Record types to ingest**

</td></tr><tr><td>

Select record types to ingest

</td><td>

Select the record types that you want to ingest. The available record types are:-   Indicators
-   Reports
-   Actors
-   Malware
-   Vulnerabilities
**Note:**

If you don't select a record type, all the record types are ingested.

</td></tr><tr><td colspan="2">

**Filters on indicator attributes**

</td></tr><tr><td>

Include deleted indicators for ingestion

</td><td>

Select this check box to allow the ingestion of indicators that have been deleted.**Note:** Deleted indicators are created as observables only if they were previously ingested. A **Deleted in CrowdStrike** tag is added to indicators removed from CrowdStrike.

</td></tr><tr><td>

Indicator types to ingest

</td><td>

Select the specific CrowdStrike indicator types you want to ingest. If none are selected, all available indicators are retrieved by default.

</td></tr><tr><td>

Malicious confidence of indicators to ingest

</td><td>

Select the malicious confidence level of CrowdStrike indicators to ingest. If left blank, all indicators are fetched from CrowdStrike regardless of malicious confidence.

</td></tr><tr><td>

Targeted industries of indicators to ingest

</td><td>

Select the targeted industries associated with CrowdStrike indicators to ingest. If none are selected, all indicators are fetched from CrowdStrike regardless of targeted industry.

</td></tr><tr><td colspan="2">

**Filters on associated actors**

</td></tr><tr><td>

Fetch indicators only if actors associated to it

</td><td>

Select this check box to fetch indicators only if they are associated with actors.

</td></tr><tr><td>

Ingest indicators only associated to these actors

</td><td>

Specify comma-separated actor names related to the indicators for ingestion. If not provided, all indicators are fetched from CrowdStrike regardless of associated actors.

</td></tr><tr><td colspan="2">

**Filters on associated reports**

</td></tr><tr><td>

Fetch indicators only if reports associated to it

</td><td>

Select this check box to fetch indicators only if they are associated with reports.

</td></tr><tr><td>

Ingest indicators only associated to these reports

</td><td>

Enter comma-separated report names associated with the indicators for ingestion. If left blank, all reports are included in the ingestion process.If not provided, all indicators are fetched from CrowdStrike regardless of associated reports.

</td></tr><tr><td colspan="2">

**Filters on associated malware families**

</td></tr><tr><td>

Fetch indicators only if malware families associated to it

</td><td>

Select this check box to fetch indicators only if they are associated with malware families.

</td></tr><tr><td>

Ingest indicators only associated to these malware families

</td><td>

Enter comma-separated malware family names associated with the indicators for ingestion. If left empty, all malware families are included in the ingestion process.If not provided, all indicators are fetched from CrowdStrike regardless of malware families.

</td></tr><tr><td colspan="2">

**Mapping of Indicator Malicious confidence to TISC confidence****Note:** The High, Medium, Low, and Unverified values are the source value for malicious confidence received from CrowdStrike.

</td></tr><tr><td>

High

</td><td>

Enter a confidence value \(0–100\) for indicators with high malicious confidence. **Note:** If a matching malicious confidence mapping is found in the **Additional Settings**, it overrides the value provided in the **Details** section even if a confidence value is manually entered.

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
</table><table id="table_vul_filters"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

**Filters on vulnerability attributes**

</td></tr><tr><td>

Severity of vulnerabilities to ingest

</td><td>

Select the severities of CrowdStrike vulnerabilities to ingest. If left empty, all vulnerabilities are fetched regardless of severity.

</td></tr><tr><td>

Exploit status of vulnerabilities to ingest

</td><td>

Select the exploit statuses of CrowdStrike vulnerabilities to ingest. If left empty, all vulnerabilities are fetched regardless of exploit status.

</td></tr><tr><td>

CVSS v3 severity of vulnerabilities to ingest

</td><td>

Select the Common Vulnerability Scoring System \(CVSS\) v3 severities of CrowdStrike vulnerabilities to ingest. If left empty, all vulnerabilities are fetched regardless of CVSS v3 severity.

</td></tr><tr><td>

Minimum CVSS v3 base score

</td><td>

Enter the minimum CVSS v3 base score for ingestion, such as 9.5. Only vulnerabilities with a score above this value are ingested.

</td></tr><tr><td>

CVE IDs of vulnerabilities to ingest

</td><td>

Enter comma-separated CVE IDs to ingest. If left empty, all vulnerabilities are considered for ingestion.

</td></tr><tr><td colspan="2">

**Filters on published date**

</td></tr><tr><td>

Fetch vulnerabilities published on or after

</td><td>

Select the date on or after which CVEs were published. Populate both date fields to ingest CVEs published within a date range.

</td></tr><tr><td>

Fetch vulnerabilities published on or before

</td><td>

Select the date on or before which CVEs were published. Populate both date fields to ingest CVEs published within a date range.

</td></tr><tr><td colspan="2">

**Filters on associated actors**

</td></tr><tr><td>

Fetch vulnerabilities only if actors associated to it

</td><td>

Select this check box to ingest only the vulnerabilities that have associated actors.

</td></tr><tr><td>

Ingest vulnerabilities only associated to these actors

</td><td>

Enter comma-separated actor names. If left empty, all actors are considered for vulnerability ingestion.

</td></tr><tr><td colspan="2">

**Filters on associated threats**

</td></tr><tr><td>

Fetch vulnerabilities only if threats associated to it

</td><td>

Select this check box to ingest only the vulnerabilities that have associated threats.

</td></tr><tr><td>

Ingest vulnerabilities only associated to these threats

</td><td>

Enter comma-separated threat names. If left empty, all threats are considered for vulnerability ingestion.Threats in CrowdStrike correspond to malware in TISC.

</td></tr><tr><td colspan="2">

**Filters on associated products**

</td></tr><tr><td>

Fetch vulnerabilities only if products associated to it

</td><td>

Select this check box to ingest only the vulnerabilities that have associated products.

</td></tr><tr><td>

Ingest vulnerabilities only associated to these products

</td><td>

Enter comma-separated product names. If left empty, all products are considered for vulnerability ingestion.

</td></tr><tr><td colspan="2">

**Filters on associated vendors**

</td></tr><tr><td>

Fetch vulnerabilities only if vendors associated to it

</td><td>

Select this check box to ingest only the vulnerabilities that have associated vendors.

</td></tr><tr><td>

Ingest vulnerabilities only associated to these vendors

</td><td>

Enter comma-separated vendor names. If left empty, all vendors are considered for vulnerability ingestion.

</td></tr></tbody>
</table>    **Note:** With the same additional settings you have defined, you can duplicate the feed when creating a new one.

10. Select **Update** on the **Additional Settings** dialog box to save the modified additional settings.

11. Select **Enable** to enable CrowdStrike Feed for ingestion.

    **Note:**

    -   When you enable the feed, its configuration fields are set to read-only and the **Save** button is hidden. To change the configuration, disable the feed first.

    -   The premium feed is the same as other feeds except the response that is parsed during configuration. A specific response is parsed to CrowdStrike by adding the Client ID and Client Secret.
    **What type of data is fetched from CrowdStrike:**

    1.  Indicators from CrowdStrike that are updated after the configured ingestion time and match the filters configured in additional settings. These indicators from CrowdStrike are then mapped to observables in TISC. The following indicator types are ingested in TISC:
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
    2.  Threat Actors from CrowdStrike that are updated after the configured ingestion time are mapped to Threat Actors in TISC.
    3.  Reports from CrowdStrike that are updated after the configured ingestion time are mapped to threat reports in TISC based on matching attributes.
    4.  Malwares from CrowdStrike that are updated after the configured ingestion time are mapped to malwares in TISC based on matching attributes.
    5.  Vulnerabilities from CrowdStrike that are updated after the configured ingestion time, are mapped to Vulnerabilities in TISC based on matching attributes.
    6.  Data is related based on the source CrowdStrike feed and ingestion. Relationships can be established when entities originate from:

        1.  The same CrowdStrike feed and the same ingestions.
        2.  The same CrowdStrike feed and different ingestions.
        3.  Different CrowdStrike feeds.
        **Note:** Filters configured in **Additional Settings** are also applied when ingesting indicators associated with previously ingested indicators, reports, or actors.

12. Select **Duplicate** to duplicate the feed.

    For more information, see [Duplicate threat intelligence feeds](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-duplicate-feeds.md).


-   **[System Properties for CrowdStrike](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/premium-threat-feed-system-properties.md)**  
The following details the system properties for CrowdStrike.

**Parent Topic:**[View Custom Feed](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/view-oob-custom-feeds.md)

