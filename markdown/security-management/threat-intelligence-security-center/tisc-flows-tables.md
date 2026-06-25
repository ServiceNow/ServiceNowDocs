---
title: Automated flows tables
description: The following tables helps you to understand the relationship tables between entities and enrichment tables that are used in automated flows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-flows-tables.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administer, Threat Intelligence Security Center, Security Operations]
---

# Automated flows tables

The following tables helps you to understand the relationship tables between entities and enrichment tables that are used in automated flows.

## Relationship tables between entities

|Table|Entity|
|-----|------|
|Related Indicator Observable|sn\_sec\_tisc\_m2m\_indicator\_observable|
|Related Indicator|sn\_sec\_tisc\_m2m\_indicator|
|Related Observable|sn\_sec\_tisc\_m2m\_observable|
|Object-Object Relationship|sn\_sec\_tisc\_m2m\_object|
|Related Indicator Object|sn\_sec\_tisc\_m2m\_object\_indicator|
|Object-Observable Relationship|sn\_sec\_tisc\_m2m\_object\_observable|

## Enrichment table

|Table|Entity|
|-----|------|
|Threat Lookup Results|sn\_sec\_tisc\_lookup\_result|
|Sightings|sn\_sec\_tisc\_sighting|
|Observable Enrichment Result|sn\_sec\_tisc\_observable\_enrichment\_result|

**Parent Topic:**[Working with automated flows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment]()

[Automated sharing of high-risk IOC's with trusted partners]()

[Automatically add threat intelligence to a TAXII collection]()

[Create vulnerability assessment for zero day]()

[Analyze, assess, and disseminate observables]()

[Analyze and assess threat IoC’s]()

[Vulnerability Management Support]()

[Zero-day vulnerability tracking]()

[Automatic Threat Actor priority tagging]()

