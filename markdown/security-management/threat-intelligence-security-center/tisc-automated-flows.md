---
title: Working with automated flows
description: Use these defined steps to learn how you can use the automated flows in TISC and its capabilities.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-automated-flows.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Administer, Threat Intelligence Security Center, Security Operations]
---

# Working with automated flows

Use these defined steps to learn how you can use the automated flows in TISC and its capabilities.

Create flows that run with TISC roles. In TISC the flows are created for the following:

-   Automated IOC Enrichment
-   Analyze, assess and disseminate on the IoC’s related to threat
-   Analyze, assess the IoC’s related to the threat and create incident.
-   Vulnerability Management Support.
-   Zero-day vulnerability tracking.
-   Automatic Threat Actor priority tagging.

**Note:** All the flows are templates which are shipped in draft state for the users to customize or copy according to their own needs.

## Reusable Actions

|Flow action|Description|
|-----------|-----------|
|Add Tag To Entity|Adding tag to an entity which supports it \(observable/indicator/object\).|
|Remove tag from entity|Removing tag to an entity which supports it \(observable/indicator/object\).|
|Check if IP address is in CIDR range|Checking if an IP address in inside a CIDR range.|
|Check if IP address is in range|Checking if an IP address is in between from and to range.|

-   **[Automated IOC Enrichment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-ioc-enrichment.md)**  
Learn how to automate enrichment of IOC’s using flows when they match a certain criterion.
-   **[Automated sharing of high-risk IOC's with trusted partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-automated-sharing-flow.md)**  
Learn how to automate sharing of high-risk IOC's with trusted partners.
-   **[Automatically add threat intelligence to a TAXII collection](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-taxii-automated-flow.md)**  
Learn how to automatically add threat intelligence to a TAXII server collection.
-   **[Create vulnerability assessment for zero day](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-create-vul-assess.md)**  
Create a vulnerability assessment to evaluate and document security risks from zero day vulnerabilities in your environment. Use this when you want to assess the potential impact of newly discovered vulnerabilities that lack available patches.
-   **[Analyze, assess, and disseminate observables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-disseminate-observables.md)**  
Learn how to analyze and disseminate observables which are related to threat.
-   **[Analyze and assess threat IoC’s](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-analyze-ioc.md)**  
Learn how to analyze an IOC’s which are a threat and notifying the security incident team.
-   **[Vulnerability Management Support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-vul-mgmt.md)**  
Learn how a new vulnerability is created in TISC with a related vulnerability in VR.
-   **[Zero-day vulnerability tracking](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-zero-vul.md)**  
Learn how to analyze RSS Feeds coming into the system.
-   **[Automatic Threat Actor priority tagging](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-threat-actor-priority-tagging.md)**  
Learn how to enable automatic tagging of Threat Actors based on their origin locations.
-   **[Automated flows tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-flows-tables.md)**  
The following tables helps you to understand the relationship tables between entities and enrichment tables that are used in automated flows.

