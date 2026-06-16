---
title: Threat Intelligence Security Center for Security Operations release notes
description: Version history for the Threat Intelligence Security Center for Security Operations on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-secops-rn-threat-intel-sec-center-secops.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 11
breadcrumb: [ServiceNow Store - Security Incident Response release notes, ServiceNow Store - Security Operations release notes, ServiceNow Store release notes]
---

# Threat Intelligence Security Center for Security Operations release notes

Version history for the Threat Intelligence Security Center for Security Operations on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.5.0 - June 2026**
    -   New:
        -   AI-powered case summarization for threat intelligence workflows helps analysts create concise summaries with overviews, findings, actions, and next steps.
        -   Playbooks are now integrated with case management, including a sample Threat Hunting playbook for guided investigations.
    -   Changed:
        -   MITRE Extraction rule supports combined Techniques and Tactics via regex.
        -   Added Malware to ingested record types; expanded relationships in Premium Threat Feed for CrowdStrike.
        -   Relationship Graphs show immediate connections and allow node filtering.
    -   Fixed:
        -   TISC Add-on for Splunk Enterprise supports historical data and flexible expiration.
        -   Fixed duplicate tag creation during feed ingestion.
        -   Added archival rules for specific observables.
        -   Link modal now correctly applies filters and select-all functions.
-   **Version 4.3.0 - April 2026**
    -   New:
        -   Automatically generate zero-day vulnerability records from flagged RSS feeds, extracting and correlating CPE, CWE, and CVE details.
        -   Create security incident records directly from detected vulnerabilities for faster incident response.
        -   Initiate vulnerability assessments from detected vulnerabilities for faster risk evaluation.
        -   Access threat intelligence from the Google Project Zero RSS feed, now included in the feed catalog.
        -   MISP and STIX parsers now extract CVE IDs from vulnerability names during ingestion, and automatically populate the CVE ID field.
        -   Vulnerability records are automatically correlated with related CVEs found in related records or enrichment data.
        -   Vulnerabilities and related intelligence now appear in the TISC Context tab of Security Incidents, providing analysts direct access to risk data during investigations.
        -   A sample workflow and flow actions automate the initiation of vulnerability assessments.
    -   Fixed:
        -   An issue where tags could not be selected in the UI form when their values did not appear in the top dropdown results.
        -   An issue where objects imported within a case were not added as artifacts to that case.
        -   An issue where intelligence reports could not be renamed using the Edit option when the report was opened in a separate tab.
        -   To enhance performance, the four correlation rules that generate potential relationships from observables are disabled by default.
-   **Version 4.2.0 - March 2026**
    -   New:
        -   RSS Feed Enhancements: The RSS feed schema, forms, and parsers now support tags, taxonomies, and expiration. Users can directly assign tags and taxonomies and link them to Threat Intelligence Library entities, improving classification and traceability.
        -   MITRE Extraction Rules: Automatic extraction of MITRE ATT&amp;CK techniques is now available during feed ingestion and insight creation, enhancing threat mapping.
        -   Tagging Rules: Customizable automated tagging is now supported for RSS feed records.
        -   Vulnerability Intelligence Enhancements: The vulnerability schema now includes CVSS scores, exploit data, and remediation details. Additional support for remediations, identifiers, attributes, and vendor comments has been added. Products, CWEs, and Vendors are now entities with relationship linking.
        -   Core Processing Enhancements: Parent identification, de-duplication, and aggregation have been improved to prioritize the latest source updates. Duplicate source cleanup ensures greater consistency.
        -   New integration: Integration with Have I Been Pwned \(HIBP\) allows for observable enrichment.
        -   UI/UX Improvements: Threat Intelligence Library list views have been reorganized for easier navigation.
    -   Fixed:
        -   Resolved feed migration issues.
        -   Updated Observable Fetch API to return readable tags and taxonomies.
        -   Fixed TAXII update ingestion issues.
        -   Addressed string size limits impacting aggregation.
        -   Corrected MISP re-publish ingestion.
        -   Fixed Splunk Add-on delta pull gaps.
-   **Version 4.0.1 - December 2025**
    -   New:
        -   Threat Intelligence External Sharing:
            -   The general availability of external sharing capabilities enables secure and seamless dissemination of threat intelligence both on-demand and automatically, utilizing standardized formats such as STIX 2.1 and MISP through template-based interfaces.
            -   Supported sharing modes now include TISC-to-external agencies \(CISA, ISAC, etc.\), external product integrations \(SIEMs, EDR, etc.\), TAXII-based sharing between TISC instances across parent and subsidiary organizations, as well as inbound intelligence from external entities.
            -   Enhancements to user experience, processing, and performance incorporate additional UI actions, options for sharing MITRE techniques as labels or tags, configuration controls for lossless data transfer between TISC instances, and expanded capabilities for reviewing and tracking shared intelligence.
    -   Intelligence Reports:
        -   A dedicated reporting section has been introduced in the Threat Intelligence Library, allowing users to generate reports outside of case management with any available intelligence, supported by several base templates. Case-level visibility restrictions are now enforced within the reporting module for case reports to strengthen access control.
        -   Library searches have been improved to include reports, returning results that match report descriptions and content.
        -   RPZ API for Sinkhole Integration:
            -   An API has been developed to facilitate the export of threat intelligence in RPZ format for DNS sinkhole deployments, supporting domains, IPv4 and IPv6 addresses, and CIDR ranges.
    -   Enhancements:
        -   Investigation Canvas &amp; Relationship Graph:
            -   Internal intelligence records, including security incidents and vulnerabilities, may now be added as nodes to the Investigation Canvas and Relationship Graph.
            -   Timeline capabilities have been incorporated into the Investigation Canvas, enabling temporal analysis with flexible event-type configurations.
            -   User experience has been further enhanced with multi-node actions, bulk operation support, and clear differentiation in activity stream updates between canvas-only node removals and library deletions.
        -   MITRE Framework Improvements:
            -   The user experience has been refined through additional confirmation prompts, enhanced context for node selection \(type and value\), and default display of all MITRE techniques.
            -   Filters applied on the MITRE card now persist through canvas pop-outs.
        -   Data Collection Enhancements:
            -   New configuration options enable direct integration with MISP servers via API, facilitating dynamic event ingestion with advanced filtration.
            -   Enhanced parsing logic supports additional entity types from MISP.
            -   Deduplication and aggregation improvements ensure that the latest records precede prior entries in CrowdStrike Feed integrations; new filters under additional settings offer greater control over ingested data.
            -   The Import Intelligence feature now accommodates STIX objects and relationships, and directly imports intelligence exported from other TISC instances.
            -   The advanced field mapper for TEXT, CSV, and JSON feeds now allows multiple field mappings and scripted transformations \(e.g., mapping several source fields to 'additional context'\). Raw sample data is displayed, preserving delimiters and special characters, and regular expressions can now be used for delimiter selection.
        -   Additional Minor Enhancements:
            -   Observable Fetch API supports filtering by tags and taxonomies.
            -   Automated flow actions are available for taxonomy assignment to library records.
            -   Manual record deletion now removes the selected library record, its sources, and related entities from the Threat Intelligence Library
    -   Fixed:
        -   Addressed an issue where UUIDs were generated instead of observable values during TISC-to-TISC sharing.
        -   Implemented batch processing to substantially increase scheduled job performance and reduce completion times.
        -   Optimized the URL Observables with Same Domain correlation rule for improved execution speed and memory efficiency.
        -   Resolved excessive relationship loading and memory usage during high-volume ingestion deduplication.
        -   Fixed a UI issue affecting comment border visibility in the TISC Workspace Activity Stream.
        -   Corrected the behavior of the Name and Aliases fields to ensure complete data retention for entity records such as threat actors.
        -   Remedied improper enforcement of Query Range ACL on the Email Log list in the Administration section.
        -   Updated ingestion logic to create distinct kill chains per MITRE source, eliminating duplicate phase names within a single chain.
        -   Rectified mismatched counts between processed observables and those shared during automated high-risk IOC sharing flows.
        -   Amended the default setting for the Exploit Status field from Exploit Available to None.
        -   Issues with tag application in the case detail view.
        -   An issue that was preventing observables from being sent from SIR to TISC.
-   **Version 3.14.3 - October 2025**
    -   New:
        -   Custom Feeds now supports MISP configuration. This allows events and attributes to be gathered directly through the MISP API using advanced filters like event publication status, creator organization, tags, threat level, and distribution level.
        -   A flow action is added which enables the automated addition of Taxonomies to library records.
    -   Fixed: An issue where tags were not applied in the case detail view has been resolved.
-   **Version 3.14.2 - September 2025**
    -   Fixed:
        -   Added a field in the CrowdStrike feed's additional settings section to filter by "Records type to ingest."
        -   Resolved an issue that was preventing observables from being sent from SIR to TISC.
-   **Version 3.14.0 - August 2025**
    -   New:
        -   Import Intelligence: Introduced functionality to import observables into the Allowlist or Denylist directly from the Import Intelligence module.
        -   CrowdStrike Feed: Enabled mapping of CrowdStrike qualitative confidence levels to TISC quantitative confidence within the advanced settings of the CrowdStrike feed.
        -   Feed Enhancements: Added support for custom field mapping in feed configurations, applicable to TEXT, CSV, and JSON formats.
        -   MITRE Extraction: Expanded MITRE technique and tactic extraction rules to facilitate extraction from Observable Enrichment results.
        -   SIR Workspace Integration: Provided options to include confidence levels, tags, and notes when transferring observables from the SIR workspace to TISC.
        -   Investigation Canvas Upgrade:
            -   Enhanced the Investigation Canvas with a redesigned layout to improve graphical visualization and promote more intuitive node distribution.
            -   Incorporated features for creating new nodes, grouping or ungrouping nodes, and clearing the entire canvas.
            -   Introduced an option to create and link a new case directly from the canvas.
            -   Implemented a capability to retrieve all associated records simultaneously via the Fetch Related Records action on a node.
            -   Added Legend to help users identify various node and edge types, enhancing graph interpretation.
            -   Updated the MITRE ATT&amp;CK card to allow creation of saved filters for TTPs of specific adversaries and other technique attributes. Selected nodes now appear as pills on the MITRE card for improved contextual awareness.
        -   MITRE ATT&amp;CK Enhancements: Enabled assignment of priorities and tags to MITRE techniques.
        -   Threat Intelligence Security Center for Splunk: Modified the GET Observable API to allow configuration of additional observable attributes for inclusion in Splunk KV Lookup.
    -   Fixed: Resolved an issue causing the CrowdStrike integration to enter an infinite loop.
-   **Version 3.12.0 - May 2025**
    -   New:
        -   Export Options for Threat Intelligence Library: Added support to export observables, indicators, and cases from the list views in STIX 2.1 JSON, CSV, and Excel formats.
        -   Additional API filter settings for CrowdStrike feed configuration: Added settings to ingest indicators of interest based on associations to threat actors, threat reports, or malware families, including an option to include indicators deleted on CrowdStrike.
        -   Create security incidents from TISC Cases: New UI action to create a security incident directly from a TISC case with an option to associate observable artifacts to the security incident.
        -   MITRE Repository mapping improvements: Ability to extend MITRE Repository data by mapping entities from the Threat Intelligence library.
        -   Duplicate feed configurations: New UI action to easily duplicate a Threat Intelligence Feed configuration.
        -   Feed improvements: Automatically skip any commented lines in the List feeds during ingestion.
    -   Changed:
        -   Renamed Course of Actions to Courses of Action.
        -   Renamed Inbound Filtering Rules to Inbound Data Exclusion Rules.
    -   Fixed:
        -   Mismatch in count of processed source records and total aggregated records in Observable table when large sets of data is ingested.
        -   RSS feeds fetching data that are older than the date specified in Fetch Data From field.
        -   OutOfMemory caused by job Refresh Affected CIs, Assets and Services for Vulnerabilities.
        -   IPv6 Addresses are ingested as IPv4 addresses, when ingested through CrowdStrike.
        -   Expiry days field is not taking values greater than 100 in the expiration rules.
        -   Few security related issues.
-   **Version 3.8.0 - February 2025**
    -   New:
        -   Added info icon on the canvas header from a case to view and access the canvas details.
        -   User now has ability to create a new canvas from a case.
    -   Fixed:
        -   Cyware feed is now working in the domain separated rated instances.
        -   Fixed ACL related issues on taxonomies and report templates.
        -   TISC query button on Splunk sighting search will be present now irrespective of configuration being active or inactive.
-   **Version 3.7.0 - November 2024**
    -   New:
        -   All observables, indicators, and entities now support MITRE technique associations.
        -   MITRE techniques can now be rolled up from artifacts at a case level both manually and automatically.
        -   Seamless migration of cases, observables, entities, and indicators from SIR Threat Intelligence to TISC.
        -   Integration with Palo Alto is now available to manage External Dynamic Lists \(EDLs\) directly from TISC.
        -   Integration with CrowdStrike Falcon EDR is now available for continuous monitoring and real-time alerting based on TISC intelligence.
        -   Introduced a new Investigation Canvas for deeper and interactive case analysis.
        -   Enhanced the user experience on relationship visualizations.
        -   Work notes will be posted on linking and unlinking artifacts in case management for easier tracking.
        -   Supports bulk taxonomy values upload.
    -   Changed:
        -   Removed MITRE attack from case management form view and included as part of Investigation canvas feature.
        -   New aliases can now be added directly from the form views.
-   **Version 3.5.0 - August 2024**
    -   New:
        -   TISC API 2.0 allows creating observables in TISC.
        -   Expiration rules allows granular definition of expiration policies at data source and record type combinations.
        -   Webhooks support for trigger based notifications from TISC.
        -   Sample automation flows to automate the analyst actions.
        -   Help Center: TISC help center helps you to easily navigate, quickly find the required help documentation that describes the features and more.
    -   Changed:
        -   Threat score calculator now supports criteria definition on security incidents from SIR.
        -   In SIR workspace, TISC context tab now shows the related information for the selected observables.
        -   In SIR workspace, introduced new UI actions to add security incidents and observables directly to TISC case.
-   **Version 3.0.3 - July 2024**
    -   Fixed:
        -   Improvement to de-duplication and aggregation processing logic for Threat Actors, Campaigns, and Attack Patterns.
        -   Critical issue in Indicators aggregation processing logic which was creating duplicate parent records.
        -   UI fixes under Threat Intelligence Security Center Administration module.
-   **Version 3.0.2 - May 2024**
    -   New:
        -   Sample notification rules for alerts based on threat intelligence.
        -   Default archival and cleanup rules for TISC related tables to remove irrelevant and older data.
        -   Case reporting to create report templates, generate, and share status reports based on the investigation summaries.
        -   Domain separation support.
        -   TISC API v1.0 to integrate with security tools.
    -   Changed:
        -   Couple of widgets are replaced with KPI indicators on the TISC Homepage.
        -   Performance improvements.
        -   Core improvements.
-   **Version 2.0.2 - March 2024**
    -   Changed:
        -   Added more OSINT feeds.
        -   Added Recorded future to the Premium feeds.
-   **Version 1.0.0 - February 2024**

    Capture the TI enhancements/TI2.0 strategy related features.


