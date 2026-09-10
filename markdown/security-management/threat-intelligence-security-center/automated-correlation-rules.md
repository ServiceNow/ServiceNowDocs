---
title: Automated correlation
description: Automated correlation automatically establishes relationships between threat intelligence records based on predefined rules, helping you identify connections between observables, indicators, and threat objects.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/security-management/threat-intelligence-security-center/automated-correlation-rules.html
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-04-06"
reading_time_minutes: 3
keywords: [automated correlation, threat intelligence, observables, indicators]
breadcrumb: [Threat Intel Library, Use, Threat Intelligence Security Center, Security Operations]
---

# Automated correlation

Automated correlation automatically establishes relationships between threat intelligence records based on predefined rules, helping you identify connections between observables, indicators, and threat objects.

The correlation process automatically establishes relationships or potential relationships between threat intelligence records based on predefined rules.

In the **Related Records** section, relationships are listed in the object details view and **Potential relationships** are listed separately.

The following list describes relationships and potential relationships.

-   Relationships: Relates two observables or an observable and STIX Domain Object \(SDO\).
-   Potential relationships: Establish potentially possible relationships between two SDOs, two observables, or an observable and SDO by using automated correlation.

**Important:** Automated correlation is disabled by default. Set *sn\_sec\_tisc.disable\_correlation\_rules* to `true` to enable it. For more information, see [Components installed with Threat Intelligence Security Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-components-installed.md).

## Correlation rule considerations

-   The correlation rules that generate potential relationships are disabled by default. To enable these rules, see [Configure correlation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/configure-correlation-rules.md).
-   Each potential relationship table has a default limit of 1,000,000 records for each domain. This is done to maintain optimal instance performance while managing threat intelligence data volume.
-   The following observables must be of malicious or suspicious reputation for the correlation rule to trigger: Artifact, Domain Name, File, IPv4 address, IPv6 address, MD5 Hash, SHA1 Hash, SHA256 Hash, SHA512 Hash, and URL.

**Note:** The following rules are deprecated:

-   Relate Indicators with Objects Based on Common Observables
-   Relate Observables Based on Communication

|Name|Description|Action|Default status|
|----|-----------|------|--------------|
|File Hash Linkage|Links files, artifacts, and hash observables that share the same hash values so that you can identify variants and copies of known malicious files.|Creates a relationship|Enabled|
|URL Domain Grouping|Groups URL observables that share the same domain and path, regardless of protocol, port number, or query parameters.|Creates a potential relationship|Disabled|
|Network Source Attribution|Links network observables to the domain and IP address \(IPv4 and IPv6\) observables that are the source of the traffic.|Creates a relationship|Enabled|
|Network Destination Attribution|Links network observables to the domain and IP address \(IPv4 and IPv6\) observables that are the destination of the traffic.|Creates a relationship|Enabled|
|Communication Path Correlation|Maps communication flows by relating the source and destination observables that are recorded in a network observable.|Creates a potential relationship|Disabled|
|Subdomain &amp; Parent Domain Linking|Relates a domain observable to its immediate parent domain and its direct subdomains.|Creates a relationship|Enabled|
|Domain-to-IP Resolution Mapping|Connects domain observables to the IP addresses that they resolve to in DNS records.|Creates a relationship|Enabled|
|Certificate-Domain Association|Associates SSL/TLS certificate observables with their corresponding domain names.|Creates a relationship|Enabled|

-   **[Configure correlation rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/configure-correlation-rules.md)**  
Enable or disable the Correlation rules or customize them according to your business requirements.
-   **[Configure potential relationship table limits](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/tisc-update-potential-relationship-record-limit.md)**  
Configure the maximum potential relationship records that automated correlation can create. By default, each potential relationship table has a limit of 1,000,000 records for each domain.

**Parent Topic:**[Threat Intel Library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/security-management/threat-intelligence-security-center/threat-intelligence-security-center-library.md)

**Related topics**  


[TISC Data Model]()

[TISC Library Objects form view]()

[TISC Library Repository]()

[Access Vulnerability Downstream actions]()

[Deleting threat intelligence library records]()

[Export intelligence data]()

[Confirm Potential Relationships from Related Records]()

