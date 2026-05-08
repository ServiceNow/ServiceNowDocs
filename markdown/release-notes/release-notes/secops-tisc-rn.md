---
title: Threat Intelligence Security Center release notes
description: The ServiceNow Threat Intelligence Security Center application enables your organization to connect security and IT teams so you can respond faster and more efficiently to threats. Threat Intelligence Security Center was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
---

# Threat Intelligence Security Center release notes

The ServiceNow® Threat Intelligence Security Center application enables your organization to connect security and IT teams so you can respond faster and more efficiently to threats. Threat Intelligence Security Center was enhanced and updated in the Australia release.

## Threat Intelligence Security Center highlights for the Australia release

-   Introduced observable enrichment through the Have I been pwned? integration, enabling analysts to determine whether email address and domain observables appear in known data breaches and review associated breach metadata.
-   Enhanced the vulnerability schema to support additional intelligence fields such as CVSS scoring, exploit details, and remediation information and RSS feed processing with support for additional fields such as tags, taxonomies, and expiration time, and enabled linking RSS feed to related artifacts.
-   Added support for managing vulnerability intelligence in the Threat Intelligence Library, including related products, vendors, CWEs, and associated remediations, identifiers, attributes, and vendor comments.
-   Added automated tagging and MITRE-ATT&amp;CK extraction rules to apply tags, taxonomies, and associate relevant techniques. Added automated cleanup of duplicate source records generated during the aggregation process.
-   Added automated zero day vulnerability detection from RSS feeds with enhanced correlation, streamlined Security Incident Response workflows, and integrated intelligence context in Security Incident to support faster threat analysis.

See Threat Intelligence Security Center for more information.

**Important:** Threat Intelligence Security Center is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Australia release

-   **Have I Been Pwned integration**

    Added support in TISC for Have I been pwned? \(HIBP\) observable enrichment, enabling analysts to identify whether observables have been exposed in known data breaches instances.


-   **Configure Tagging Rules in TISC**

    Introduced automated tagging of RSS feed records using configurable tagging rules to apply tags and taxonomies.


-   **Create a CWE record**

    Introduced CWEs as related entities with support for relationship linking.


-   **Create Remediations**

    Introduced remediations as related entities with support for relationship linking and added support for managing remediations.


-   **Create a Product**

    Introduced products as related entities with support for relationship linking.


-   **Create a Vendor to a Vulnerability**

    Associated vendors as related entities with support for relationship linking.


-   **Automated creation of zero day vulnerability**

    Automatically generate zero day vulnerability records from flagged RSS feeds with extracted and linked CPE, CWE, and CVE details for enhanced threat analysis. The catalog now includes the RSS feed for **Google Project Zero**, enabling real-time detection of emerging threats.


-   **Create Vulnerability Assessment from a Vulnerability**

    Initiate vulnerability assessments directly from identified issues for faster risk evaluation. Sample workflows and flow actions are included to automate the assessment process.


-   **Create Security Incident from a Vulnerability Record**

    Create security incident records directly from detected vulnerabilities to expedite incident response and streamline threat management workflows.


-   **Enable security incidents for vulnerabilities**

    View vulnerabilities and related intelligence in the **TISC Context** tab of Security Incident Response Workspace, allowing analysts to quickly access risk data during investigations without navigating to separate records.


## UI changes

-   **TISC Library Repository**

    Enhanced Threat Intelligence Library list views by grouping observables, indicators, threat entities, RSS feed, and vulnerability artifacts into appropriate categories for improved navigation.


-   **Create Vulnerability Assessment from a Vulnerability**

    Introduced a new button **Create Vulnerability Assessment** to conduct a vulnerability assessment for a specific vulnerability.


-   **Create Security Incident from a Vulnerability Record**

    Introduced a new button **Create Security Incident** to facilitate identifying vulnerabilities and enable faster incident response within the threat analysis.


-   **Threat Intelligence Security Center Catalog**

    Introduced a new catalog entry which includes the RSS feed for **Google Project Zero**, enabling real-time detection of emerging threats.


## Changed in this release

-   **MITRE ATT&amp;CK Technique Extraction Rules and View extracted MITRE ATT&amp;CK Techniques**

    Enabled MITRE-ATT&amp;CK extraction rules for RSS feed to map and associate MITRE-ATT&amp;CK techniques.


-   **View RSS Feeds**

    Enhanced the RSS feed schema and parsers to support additional fields, including tags, taxonomies, status, and expiration time.


-   **Export intelligence data, Sharing of Outbound Intelligence Records from GUI, and Add to TAXII Collections from Library List View**

    Enhanced STIX 2.1 export to include Traffic Light Protocol \(TLP\) definitions applied to intelligence objects as TLP 2.0 marking definition objects. For more information, see Marking Definition.


-   **System properties for TISC Reports**

    The system property `sn_sec_tisc.reporting.email_template_sn_sec_tisc_case` is no longer supported in TISC. It has been renamed to `sn_sec_tisc.default_report_email_template`, effective with the latest release.


-   **Configure custom MISP API feed**

    Enhanced MISP API feed ingestion to handle events when the published timestamp is greater than the modified timestamp.


-   **Define Vulnerability and Access the Vulnerability Entities**

    Enhanced the vulnerability schema to support additional vulnerability intelligence fields related to CVSS scoring, exploit details, and remediation information.


## Activation information

Install Threat Intelligence Security Center by requesting it from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **Threat Intelligence**

    The ServiceNow Threat Intelligence application displays indicators of compromise \(IoC\) and enables you to enrich security incidents with threat intelligence data.

-   **Security Incident Response**

    With Security Incident Response manage the life cycle of your security incidents from initial analysis to containment, eradication, and recovery. Security Incident Response enables you to get a comprehensive understanding of incident response procedures performed by your analysts, and understand trends and bottlenecks in those procedures with analytic-driven dashboards and reporting.

-   **Vulnerability Response**

    Vulnerability Response is part of the Security Operations application suite. Together, these applications connect security to your IT department, increase the speed and efficiency of your response, and give you a definitive view of your security posture.

-   **Security Operations common functionality**

    The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

