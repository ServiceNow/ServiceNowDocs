---
title: Security Operations Integration Configurations
description: Many of the integrations included in the base system require little or no setup, and operate in the same way. Certain integrations, such as the Qualys Cloud Platform, however, require separate steps for setting up the integration. Others support different sets of scan and lookup types and different rate limits.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [ServiceNow Security Operations integration development guidelines, Security Operations Integration Reference, Security Operations common functionality, Security Operations]
---

# Security Operations Integration Configurations

Many of the integrations included in the base system require little or no setup, and operate in the same way. Certain integrations, such as the Qualys Cloud Platform, however, require separate steps for setting up the integration. Others support different sets of scan and lookup types and different rate limits.

This section describes the differences between the supported integrations and points you to more documentation, as needed.

-   [Carbon Black integration](../../secops-integration-sir/secops-integration-carbonblack/reference/carbon-black-landing-page.md): allows you to investigate and respond to security incidents by using the Carbon Black APIs to query and interact with endpoints associated with security incidents.
-   [Check Point Anti-bot - Email Parser integration](../../secops-integration-sir/secops-integration-checkpt-antibot-emailparser/concept/checkpt-antibot-integration.md#): uses an email parser that consumes email notifications from Check Point Anti-bot to create security incidents.
-   [Elasticsearch Incident Enrichment integration](../../secops-integration-sir/secops-integration-elasticsearch-inc-enrichment/reference/elasticsearch-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [Have I been pwned? integration](../../secops-integration-sir/secops-integration-haveibeenpwned/reference/haveibeenpwned-landing-page.md): allows the list of breached accounts \(email addresses and usernames\) to be quickly searched via a RESTful service.
-   [HPE Security ArcSight ESM - Email Parser integration](../../secops-integration-sir/secops-integration-hpe-arcsight-esm-emailparser/concept/arcsight-emailparser-integration.md#): uses an email parser that consumes email notifications from HPE ArcSight ESM to create security incidents.
-   [HPE ArcSight Logger - Incident Enrichment integration](../../secops-integration-sir/secops-integration-hpe-arcsight-logger-inc-enrichment/reference/arcsight-logger-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [IBM QRadar - Incident Enrichment Integration](../../secops-integration-sir/secops-integration-qradar-inc-enrichment/reference/qradar-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [McAfee ESM - Email Parser integration](../../secops-integration-sir/secops-integration-intel-mcafee-esm-emailparser/concept/mcafee-esm-emailparser-integration.md): uses an email parser that consumes email notifications from McAfee ESM to create security incidents.
-   [McAfee ESM - Incident Enrichment Integration](../../secops-integration-sir/secops-integration-intel-mcafee-esm-inc-enrichment/reference/mcafee-esm-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [OPSWAT Metadefender integration overview](../../secops-integration-threat/secops-integration-opswat-metadefender/concept/c_Metadefenderintegration.md#): allows threat data, detected by the third-party Metadefender scanner, to be downloaded to the Threat Intelligence application for tracking, prioritization, and resolution.
-   [Palo Alto Networks - AutoFocus integration](../../secops-integration-sir/secops-integration-palo-alto-autofocus/reference/palo-alto-autofocus-landing-page.md): Palo Alto Networks AutoFocus, a threat intelligence cloud service, allows you to search for session information related to security incident observables.
-   [Palo Alto Networks - Firewall integration](../../secops-integration-sir/secops-integration-palo-alto-firewall/reference/palo-alto-firewall-landing-page.md): Palo Alto Networks Firewall allows you to set up and maintain firewalls for preventing known and unknown threats across the network, cloud, and endpoints.
-   [Palo Alto Networks - WildFire integration](../../secops-integration-sir/secops-integration-palo-alto-wildfire/reference/palo-alto-wildfire-landing-page.md): Wildfire integration allows you to programmatically query analysis jobs on Wildfire and retrieve historical results through a simple XML API interface.
-   [Understanding the Qualys Vulnerability Integration](../../secops-integration-vr/qualys/concept/c_QualysVulnIntegration.md): Qualys Cloud Platform is used in Vulnerability Response.
-   [Splunk - Incident Enrichment integration](../../secops-integration-sir/secops-integration-splunk-inc-enrichment/reference/splunk-in-enrich-landing-page.md): searches your logs and adds relevant sighting information to your security incidents.
-   [VirusTotal integration](../../secops-integration-threat/secops-integration-virustotal/reference/virustotal-landing-page.md): used in Threat Intelligence. To use this lookup source, you must [activate the VirusTotal Integration plugin](../task/install-config-3rd-party-integs.md).
-   [WhoisXML API integration setup](../../secops-integration-threat/secops-integration-whois/concept/whois-integration-setup.md): provides consistent, well-structured data from a Whois lookup. Keeps accurate Whois data accessible 24/7.

-   **[Activate and configure third-party integrations](../task/install-config-3rd-party-integs.md)**  
You can activate the plugins for third-party integrations and configure them for use from the same screen.
-   **[Create an integration](../../security-operations-integrations/task/create-integrations.md)**  
You can create an integration and add the associated integration card to the Security Integrations screen. This procedure is intended for partners who create third-party integrations.

**Parent Topic:**[ServiceNow Security Operations integration development guidelines](../../security-operations-integrations/concept/c_IntegrationWritingGuidelines.md)

**Related topics**  


[Types of ServiceNow integrations provided](../../security-operations-integrations/concept/c_TypesOfIntegrationsProv.md)

[Tips for writing integrations](../../security-operations-integrations/concept/c_BestPractisesIntegrations.md)

[Integration troubleshooting](../../security-operations-integrations/concept/c_IntegrationTroubleshooting.md)

