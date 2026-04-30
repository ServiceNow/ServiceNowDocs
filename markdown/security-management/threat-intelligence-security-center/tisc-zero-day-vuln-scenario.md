---
title: Automated creation of zero day vulnerability from RSS feed
description: A zero day vulnerability scenario demonstrates how TISC detects and manages vulnerabilities that have not yet received CVE assignments.
locale: en-US
release: yokohama
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2026-03-30"
reading_time_minutes: 1
breadcrumb: [Configure Tagging Rules in TISC, About Rules Engine in TISC, Administer Threat Intelligence Security Center, Threat Intelligence Security Center, Security Operations]
---

# Automated creation of zero day vulnerability from RSS feed

A zero day vulnerability scenario demonstrates how TISC detects and manages vulnerabilities that have not yet received CVE assignments.

Role required: sn\_sec\_tisc.admin

This feature enables automatic detection and processing of zero day vulnerabilities through configurable tagging rules. For more information, see [Configure Tagging Rules in TISC](../task/tisc-tag-rules.md).

**Prerequisite**:

Verify that the **RSS Feeds with Zero Day mentions** tagging rule is enabled. This ensures automatic association of the RSS Feeds with the **Vulnerability Intelligence: ZERODAY** taxonomy.

## Zero Day Vulnerability Processing - Vulnerability Source Record Creation

Zero Day Vulnerability Processing - Vulnerability Source Record Creation.

A Vulnerability Source record is automatically created when:

-   an RSS feed record is associated with a specific Zero Day taxonomy value.
-   an RSS feed record is updated and contains new entities such as CWE IDs, CVE IDs, CPEs, or Product IDs.

**Record identification**: Each Vulnerability Source record is uniquely identified using the RSS feed GUID, ensuring traceability to the original source.

TISC automatically populates the following fields of Vulnerability Source:

|Field|Description|
|-----|-----------|
|Name|Combination of RSS feed GUID and timestamp.|
|Description|Indicates the record is created from the RSS feed, including the GUID reference.|
|Zero day flag|Set to **True**.|
|CVE ID|Populated when exactly one CVE is identified.|
|Additional Context|Includes extracted CVE IDs and Product IDs.|

The following entities are extracted from RSS feeds:

-   CVE IDs \(vulnerabilities\)
-   CWE IDs \(weaknesses\)
-   CPEs and Product IDs \(affected products\)

For more information about the extraction and correlation mechanism, see [KB2936701](https://support.servicenow.com/kb?sys_kb_id=ef0c61718348c3d0cdbbc430feaad32e&id=kb_article_view) article.

