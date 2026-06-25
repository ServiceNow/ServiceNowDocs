---
title: Security Operations Integration Configurations
description: Many of the integrations included in the base system require little or no setup, and operate in the same way. Certain integrations, such as the Qualys Cloud Platform, however, require separate steps for setting up the integration. Others support different sets of scan and lookup types and different rate limits.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/third-party-integrations.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [ServiceNow Security Operations integration development guidelines, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration Configurations

Many of the integrations included in the base system require little or no setup, and operate in the same way. Certain integrations, such as the Qualys Cloud Platform, however, require separate steps for setting up the integration. Others support different sets of scan and lookup types and different rate limits.

This section describes the differences between the supported integrations and points you to more documentation, as needed.

-   [Carbon Black integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/carbon-black-landing-page.md): allows you to investigate and respond to security incidents by using the Carbon Black APIs to query and interact with endpoints associated with security incidents.
-   [Check Point Anti-bot - Email Parser integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/checkpt-antibot-integration.md): uses an email parser that consumes email notifications from Check Point Anti-bot to create security incidents.
-   [Elasticsearch Incident Enrichment integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/elasticsearch-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [Have I been pwned? integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/haveibeenpwned-landing-page.md): allows the list of breached accounts \(email addresses and usernames\) to be quickly searched via a RESTful service.
-   [HPE Security ArcSight ESM - Email Parser integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/arcsight-emailparser-integration.md): uses an email parser that consumes email notifications from HPE ArcSight ESM to create security incidents.
-   [HPE ArcSight Logger - Incident Enrichment integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/arcsight-logger-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [IBM QRadar - Incident Enrichment Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/qradar-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [McAfee ESM - Email Parser integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/mcafee-esm-emailparser-integration.md): uses an email parser that consumes email notifications from McAfee ESM to create security incidents.
-   [McAfee ESM - Incident Enrichment Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/mcafee-esm-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [OPSWAT Metadefender integration overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/c_Metadefenderintegration.md): allows threat data, detected by the third-party Metadefender scanner, to be downloaded to the Threat Intelligence application for tracking, prioritization, and resolution.
-   [Palo Alto Networks - AutoFocus integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/palo-alto-autofocus-landing-page.md): Palo Alto Networks AutoFocus, a threat intelligence cloud service, allows you to search for session information related to security incident observables.
-   [Palo Alto Networks - Firewall integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/palo-alto-firewall-landing-page.md): Palo Alto Networks Firewall allows you to set up and maintain firewalls for preventing known and unknown threats across the network, cloud, and endpoints.
-   [Palo Alto Networks - WildFire integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/palo-alto-wildfire-landing-page.md): Wildfire integration allows you to programmatically query analysis jobs on Wildfire and retrieve historical results through a simple XML API interface.
-   [Understanding the Qualys Vulnerability Integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/vulnerability-response/c_QualysVulnIntegration.md): Qualys Cloud Platform is used in Vulnerability Response.
-   [Splunk - Incident Enrichment integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/security-incident-response/splunk-in-enrich-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [VirusTotal integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/virustotal-landing-page.md): used in Threat Intelligence. To use this lookup source, you must [activate the VirusTotal Integration plugin](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/install-config-3rd-party-integs.md).
-   [WhoisXML API integration setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/whois-integration-setup.md): provides consistent, well-structured data from a Whois lookup. Keeps accurate Whois data accessible 24/7.

-   **[Activate and configure third-party integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/install-config-3rd-party-integs.md)**  
You can activate the plugins for third-party integrations and configure them for use from the same screen.
-   **[Create an integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/create-integrations.md)**  
You can create an integration and add the associated integration card to the Security Integrations screen. This procedure is intended for partners who create third-party integrations.

**Parent Topic:**[ServiceNow Security Operations integration development guidelines](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/c_IntegrationWritingGuidelines.md)

**Related topics**  


[Types of ServiceNow integrations provided]()

[Tips for writing integrations]()

[Integration troubleshooting]()

