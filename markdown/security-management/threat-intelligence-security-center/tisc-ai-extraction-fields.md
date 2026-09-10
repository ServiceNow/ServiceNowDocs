---
title: AI extraction supported entities and fields
description: Threat entity types that AI extraction identifies in an uploaded document, and the AI-generated fields that it adds to the extracted records.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/threat-intelligence-security-center/tisc-ai-extraction-fields.html
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: reference
last_updated: "2026-08-14"
reading_time_minutes: 1
keywords: [AI extraction, Analysis Score, Analysis Reasoning]
breadcrumb: [Import data using AI, Import Intelligence in TISC, Use, Threat Intelligence Security Center, Security Operations]
---

# AI extraction supported entities and fields

Threat entity types that AI extraction identifies in an uploaded document, and the AI-generated fields that it adds to the extracted records.

## Supported threat entities

|Record type|Supported types|
|-----------|---------------|
|Observables|IPv4, IPv6, domain, URL, MD5, SHA1, SHA256, email address, IPv4 CIDR, IPv6 CIDR, AS number, and MAC address.|
|Objects|CVE, threat actor, malware, and campaign.|

## AI-generated fields

|Field|Description|
|-----|-----------|
|Analysis Score|AI-assessed confidence from 0 through 100, based on contextual signals and enrichment. The score indicates how confidently the entity was identified and classified.|
|Analysis Reasoning|AI-generated explanation of the score assessment, stored as a set of attributes. See the following table.|

|Attribute|Description|
|---------|-----------|
|Score Reasoning|Justification for the assigned analysis score.|
|Source context|Words that surround the entity in the source document, so that you can locate the entity in its original context.|
|Attribution|Threat actor, campaign, or malware associated with the entity in the source document. Attribution is derived from the document content, not from the threat intelligence repository.|
|Usage|How the associated threat entity uses the extracted entity. For example, an IP address used as a command and control server.|

**Note:**

When you submit the import, the Analysis Score and Analysis Reasoning values are carried into the Additional context section of the source and aggregated records.

The Confidence value on the extracted records comes from the Confidence field that you set in the definitions section of the import. It isn't AI-generated.

To support extraction of a higher number of threat entities, use Content Understanding v6.2.0 or higher. For more information, see [Content Understanding](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/content-understanding-landing.md).

**Parent Topic:**[Import data using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/import-data-using-ai.md)

**Related topics**  


[Import data using AI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/threat-intelligence-security-center/import-data-using-ai.md)

