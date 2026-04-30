---
title: Threat Intelligence Security Center release notes
description: The ServiceNow Threat Intelligence Security Center \(TISC\) application empowers your organization to connect security and IT teams so you can respond faster and more efficiently to threats.
locale: en-US
release: xanadu
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
---

# Threat Intelligence Security Center release notes

The ServiceNow® Threat Intelligence Security Center \(TISC\) application empowers your organization to connect security and IT teams so you can respond faster and more efficiently to threats.

## Threat Intelligence Security Center highlights for the Xanadu release

-   Visualize node connections between entities like observables, IOCs, and threat actors, and link cases or canvases to enrich analysis.
-   Enable continuous monitoring and real-time alerts based on intelligence from TISC with CrowdStrike Falcon EDR integration.
-   Block malicious IPs, URLs, and domains using External Dynamic List \(EDL\) capabilities with Threat Intelligence data and Palo Alto Networks integration.
-   Manage the analyst actions through automation flows.
-   Conduct research on threats to support the reactive and proactive needs of security teams.​
-   Create and track threat investigations using Case Management.​

See [Threat Intelligence Security Center](https://www.servicenow.com/docs/access?context=tisc-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US) for more information.

## New in the Xanadu release

-   ****

    All observables, indicators, and entities now supports MITRE technique associations.


-   **[Roll up of MITRE technique associations](https://www.servicenow.com/docs/access?context=tisc-mitre-roll-up&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    MITRE techniques can now be rolled up from artifacts at a case level both manually and automatically.


-   **[Palo Alto Networks integration](https://www.servicenow.com/docs/access?context=palo-alto-networks-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Integration with Palo Alto is now available to manage External Dynamic Lists \(EDLs\) directly from TISC.


-   **[CrowdStrike Falcon EDR integration](https://www.servicenow.com/docs/access?context=crowdstrike-edr-integration&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Integration with CrowdStrike Falcon EDR is now available for continuous monitoring and real-time alerting based on TISC intelligence.


-   **[Working with Investigation Canvases](https://www.servicenow.com/docs/access?context=tisc-investigation-canvases&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Introduced a new Investigation Canvas for deeper and interactive case analysis.


-   **[View details in Relationship Graph](https://www.servicenow.com/docs/access?context=objects-visualizer&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Enhanced the user experience on relationship visualizations.


-   **[Bulk import Taxonomies](https://www.servicenow.com/docs/access?context=tisc-import-taxonomy&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Supports bulk taxonomy values upload.


-   **[TISC API References](https://www.servicenow.com/docs/access?context=tisc-api-references&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Creating observables in TISC is now available through the implementation of TISC API 2.0.

-   **[Defining Expiration Rules](https://www.servicenow.com/docs/access?context=tisc-expiration-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Define expiration policies at a more granular level by creating expiration rules for data source and record type combinations.

-   **[Working with Webhooks](https://www.servicenow.com/docs/access?context=tisc-webhooks&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Initiate trigger-based notifications by using Webhooks.

-   **[Working with automated flows](https://www.servicenow.com/docs/access?context=tisc-automated-flows&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Automate analyst actions through sample automation flows.

-   **[Add observables to TISC Case](https://www.servicenow.com/docs/access?context=observables-to-case&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Add security incident and observables directly to a TISC case in the Security Incident Response Workspace.

-   **[MITRE ATT&amp;CK Technique Extraction Rules](https://www.servicenow.com/docs/access?context=mitre-extraction-rules&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Capture automatically extracted MITRE techniques to the intelligence records such as observables, indicators, and all STIX entities.


## Changed in this release

-   **[TISC Library Repository](https://www.servicenow.com/docs/access?context=tisc-ioc&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    New aliases can now be added directly from the form views of the threat intelligence library.


## UI changes

-   **[View related info from TISC](https://www.servicenow.com/docs/access?context=tisc-related-info-sir&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    In the Security Incident Response Workspace, the **TISC Context** tab now shows the related information for selected observables.

-   **[Custom Threat Score Calculator in TISC](https://www.servicenow.com/docs/access?context=using-custom-threat-score-calculator&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The Customer Threat Score Calculator automatically defines threat score criteria for security incidents based on user-defined criteria.


## Activation information

Install Threat Intelligence Security Center by requesting it from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

-   **[Security Operations common functionality](https://www.servicenow.com/docs/access?context=sec-ops-common-functionality&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    When any of the plugins for the main Security Operations applications \(Security Incident Response, Vulnerability Response, Threat Intelligence, or Configuration Compliance\) are activated, the Security Support Common plugin is activated.


## Related ServiceNow applications and features

-   **[Vulnerability Response](https://www.servicenow.com/docs/access?context=vuln-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    Vulnerability Response is part of the Security Operations application suite. Together, these applications connect security to your IT department, increase the speed and efficiency of your response, and provide you with an overview of your security posture.

-   **[Threat Intelligence](https://www.servicenow.com/docs/access?context=threat-intel-landing-page&version=xanadu&pubname=xanadu-security-management&ft:locale=en-US)**

    The ServiceNow® Threat Intelligence application displays indicators of compromise \(IoC\) and enables you to enrich security incidents with threat intelligence data.


**Parent Topic:**[Security Operations release notes](security-operations-rn-landing.md)

