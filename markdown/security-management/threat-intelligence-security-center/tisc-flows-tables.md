---
title: Automated flows tables
description: The following tables helps you to understand the relationship tables between entities and enrichment tables that are used in automated flows.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Working with automated flows, Administration, Threat Intelligence Security Center, Security Operations]
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

**Parent Topic:**[Working with automated flows](tisc-automated-flows.md)

**Related topics**  


[Automated IOC Enrichment](../task/tisc-ioc-enrichment.md)

[Analyze, assess, and disseminate observables](../task/tisc-disseminate-observables.md)

[Analyze and assess threat IoC’s](../task/tisc-analyze-ioc.md)

[Vulnerability Management Support](../task/tisc-vul-mgmt.md)

[Zero-day vulnerability tracking](../task/tisc-zero-vul.md)

