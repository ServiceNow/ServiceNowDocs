---
title: Threat Intelligence Security Center Knowledge Base articles
description: This section provides a curated list of key Knowledge Base \(KB\) articles related to Threat Intelligence Security Center \(TISC\). These resources include best practices, configuration guidance, compatibility information, and operational workflows to help you effectively manage threat intelligence and security within TISC.
locale: en-US
release: zurich
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: reference
last_updated: "2026-02-26"
reading_time_minutes: 3
breadcrumb: [Reference, Threat Intelligence Security Center, Security Operations]
---

# Threat Intelligence Security Center Knowledge Base articles

This section provides a curated list of key Knowledge Base \(KB\) articles related to Threat Intelligence Security Center \(TISC\). These resources include best practices, configuration guidance, compatibility information, and operational workflows to help you effectively manage threat intelligence and security within TISC.

The following knowledge base articles provide guidance on TISC concepts, configuration, integration, and best practices. The articles are maintained in the ServiceNow internal knowledge base and are referenced from the parent index article [KB1778603](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1778603).

|KB ID|Title|Description|
|-----|-----|-----------|
|[KB1778603](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1778603)|Knowledge base links for Threat Intelligence Security Center|A consolidated index of all knowledge base articles related to TISC. Use this article as the starting point for locating TISC documentation resources.|
|[KB1748938](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1748938)|Difference Between Threat Intelligence Security Center \(TISC\) and Threat Intelligence Module in SIR \(SIR-TI\)|Explains the key architectural and functional differences between the standalone TISC product and the Threat Intelligence module available within Security Incident Response \(SIR-TI\).|
|[KB1778607](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1778607)|How SIR/TI and TISC Integration Works|Describes the integration architecture and data flow between the SIR Threat Intelligence module and the Threat Intelligence Security Center, including synchronization behavior and supported configurations.|
|[KB1706151](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1706151)|Migration of Data from Existing Threat Intelligence to Threat Intelligence Security Center|Provides a step-by-step guide for migrating threat intelligence data from the legacy SIR-TI module to TISC, including pre-migration checks, data mapping, and validation steps.|
|[KB1587754](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1587754)|Parent Identification Logic for Various Entities in TISC|Explains the logic TISC uses to identify and assign parent entities across different threat intelligence record types such as observables, indicators, and threat groups.|
|[KB1587756](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1587756)|De-duplication Logic for Various Entities in TISC|Describes how TISC identifies and resolves duplicate records across threat intelligence entities to maintain data integrity and reduce noise in the threat intelligence repository.|
|[KB1587758](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1587758)|Aggregation Logic for Various Entities in TISC|Details the rules and processes TISC uses to aggregate threat intelligence data ingested from multiple sources into unified, consolidated entity records.|
|[KB1648039](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1648039)|Best Practices Guide for TISC|Provides recommended practices for deploying, configuring, and maintaining the Threat Intelligence Security Center for optimal performance, data accuracy, and operational efficiency.|
|[KB1909534](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1909534)|Security Control List \(AllowList, DenyList, WatchList\) for Threat Intelligence Security Center|Documents the configuration and usage of security control lists in TISC, including AllowList, DenyList, and WatchList. Also notes a known behavior: searches with a larger number of characters return more results compared to searches with fewer characters.|
|[KB2148681](https://support.servicenow.com/kb?sys_kb_id=0d2295ee4721e2102c31b98a436d43ec&id=kb_article_view)|TISC Intelligence Exchange Use Case Guide|Covers common use cases for exchanging threat intelligence data between TISC instances and with external platforms, including configuration steps and representative scenarios.|
|[KB2332774](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2332774)|TISC Outbound Intelligence in MISP Format|Explains how to configure TISC to share outbound threat intelligence in MISP-compatible format so that external consumers and partner instances can ingest the data.|
|[KB2197697](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2197697)|TISC MISP Processing – MISP to TISC Mapping|Provides field-level mapping details for ingesting and processing MISP threat intelligence data within TISC, including object type conversions and attribute handling.|
|[KB2326271](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2326271)|TISC CrowdStrike Custom Feed – Internal Field Mapping|Documents the internal field mapping applied when TISC processes CrowdStrike custom feed data, enabling consistent normalization of CrowdStrike indicators into the TISC data model.|
|[KB2677048](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB2677048)|Improving Observable/Indicator Deduplication Job Performance – Duplicate Records from Same Source Cleanup|Describes techniques and configurations to improve the performance of the TISC deduplication job, with guidance on cleaning up duplicate observable and indicator records that originate from the same source.|

## Related Resources

For additional information about TISC configuration and administration, see the ServiceNow product documentation for Security Operations and the TISC release notes for the current release.

