---
title: Threat Intelligence Security Center release notes
description: The ServiceNow Threat Intelligence Security Center application enables your organization to connect security and IT teams so you can respond faster and more efficiently to threats. Threat Intelligence Security Center was enhanced and updated in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# Threat Intelligence Security Center release notes

The ServiceNow® Threat Intelligence Security Center application enables your organization to connect security and IT teams so you can respond faster and more efficiently to threats. Threat Intelligence Security Center was enhanced and updated in the Zurich release.

## Threat Intelligence Security Center highlights for the Zurich release

-   External sharing is now generally available, allowing secure and automated sharing of threat intelligence in STIX 2.1 and MISP formats.
-   Redesigned the Investigation Canvas with activity timelines, added internal intelligence, improved node design and interactions, enhanced related records to retrieve all the associated records, and upgraded the MITRE card with filter capabilities for a smoother experience.
-   Introduced the ability to import events directly from the MISP server.
-   Implemented a unified mapping experience for the text based feeds such as TEXT, CSV, and JSON import formats.
-   Implemented confidence mapping for the CrowdStrike \(CS\) Feed as part of additional settings. You can now map the malicious confidence levels of CrowdStrike indicators to the observable confidence values.

See [Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US) for more information.

**Important:** Threat Intelligence Security Center is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## New in the Zurich release

-   **[Configure Threat Intelligence External Sharing](https://www.servicenow.com/docs/access?context=tisc-intel-sharing&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Take advantage of external sharing for secure, automated, and on-demand dissemination of threat intelligence using STIX 2.1 and MISP formats. Supports sharing across external agencies \(CISA, ISAC\), integrations \(SIEMs, EDRs\), TAXII-based TISC instances, and inbound intelligence from external entities.


-   **[About Report Templates in TISC](https://www.servicenow.com/docs/access?context=tisc-report-templates&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Generate reports outside case management using base templates through a new reporting section in the Threat Intelligence Library.


-   **[Configure custom MISP API feed](https://www.servicenow.com/docs/access?context=tisc-premium-misp&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Import events, attributes, and objects from the MISP server into the Threat Intelligence Library.


-   **[Configure Custom Event Types for Timeline](https://www.servicenow.com/docs/access?context=tisc-config-timeline&version=zurich&pubname=zurich-security-management&ft:locale=en-US) and [Using Timeline in Investigation Canvas](https://www.servicenow.com/docs/access?context=tisc-timeline-events&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Define, visualize, and manage timeline events associated with nodes through the Investigation Canvas.


-   **[Configuring TISC add-on in Splunk](https://www.servicenow.com/docs/access?context=tisc-configure-splunk&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Include optional attributes during configuration that can be stored in the Splunk KV Store.

-   **[Configure custom CrowdStrike feed](https://www.servicenow.com/docs/access?context=premium-threat-feed-for-crowdstrike&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Map CrowdStrike Indicator Malicious confidence to TISC confidence.

-   **[View Threat Intel Feeds](https://www.servicenow.com/docs/access?context=base-system-threat-intel-feeds&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Map specific source values to required observable fields during import process.


## UI changes

-   ****

    Introduced **Add From Internal Intelligence** option to include the data from the internal systems.


-   **[Define an Observable](https://www.servicenow.com/docs/access?context=define-an-observable&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Introduced a notice when deleting an observable record to help prevent accidental removal of its associated source records.


-   **[Configure Custom Field Mapping](https://www.servicenow.com/docs/access?context=tisc-field-mapping&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The list view has been replaced with a code editor in the Sample data \(Input\) section of the field mapping, preserving the original structure and formatting of raw data.


-   **[Creating an investigation canvas](https://www.servicenow.com/docs/access?context=tisc-create-canvas&version=zurich&pubname=zurich-security-management&ft:locale=en-US) Clear canvas button**

    A **Clear canvas** button to clear the canvas permanently removes all nodes from the investigation canvas.


-   **[Manage Techniques](https://www.servicenow.com/docs/access?context=tisc-manage-techniques&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Introduced Priority levels and TISC Tags to categorize and tag MITRE Techniques more effectively.


-   **[Components installed with Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-components-installed&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Introduced a new system property to configure the default Traffic Light Protocol \(TLP\) level.


-   **[Import data using structured file](https://www.servicenow.com/docs/access?context=import-data-using-structured-file&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Introduced an **Add Observable\(s\) to Security Control List** drop-down list to enable the importing of Allow listed observables directly through Import Intelligence.


-   **Coral theme**

    Coral is now the default theme for new portal, web, and mobile experiences with Next Experience or Core UI enabled. This theme provides a fresh look and feel, featuring brand-neutral illustrations to enhance your user experience. A dark theme option is available for web and mobile experiences.


## Changed in this release

-   ****

    Aggregate and analyze the data from internal systems through internal intelligence included in the Investigation Canvas module to help you identify potential threats more effectively.


-   **[Import Intelligence in TISC](https://www.servicenow.com/docs/access?context=importing-threat-intelligence&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Enhanced the Import Intelligence functionality to support direct import of allow list observables.

-   **[Working with Investigation Canvas](https://www.servicenow.com/docs/access?context=tisc-investigation-canvases&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The Investigation Canvas feature has been extended to include customized nodes, node relationships, and node legends, as well as the grouping and ungrouping of nodes.

-   **[Investigation canvas and MITRE ATT&amp;CK](https://www.servicenow.com/docs/access?context=investigation-and-mitre&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    Navigate and use the MITRE-ATT&amp;CK model within the Investigation Canvas more effectively by taking advantage of enhanced filtering options.


## Activation information

Install Threat Intelligence Security Center by requesting it from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home). Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Accessibility information

-   **Dark theme**

    The new Coral theme includes a dark theme option for web and mobile experiences. This option is commonly used to alleviate eye strain and improve readability.


## Related ServiceNow applications and features

-   **[Threat Intelligence](https://www.servicenow.com/docs/access?context=threat-intel-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The ServiceNow Threat Intelligence application displays indicators of compromise \(IoC\) and enables you to enrich security incidents with threat intelligence data.

-   **[Security Incident Response](https://www.servicenow.com/docs/access?context=sir-landing-page&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    With Security Incident Response manage the life cycle of your security incidents from initial analysis to containment, eradication, and recovery. Security Incident Response enables you to get a comprehensive understanding of incident response procedures performed by your analysts, and understand trends and bottlenecks in those procedures with analytic-driven dashboards and reporting.

-   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&version=zurich&pubname=zurich-security-management&ft:locale=en-US)**

    The Security Support Common plugin is activated when any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated.


**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

