---
title: Field mapping for the Prisms AIRS integration
description: Review source and target fields and view imported data on tables and records in your ServiceNow ServiceNow AI Platform instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/palo-alto-prisma-airs-mapping.html
release: australia
topic_type: reference
last_updated: "2026-09-03"
reading_time_minutes: 3
breadcrumb: [Explore the Palo Alto Prisma AIRS Integration for AI Security Exposure Management, Integrate, Unified Security Exposure Management, Security Operations]
---

# Field mapping for the Prisms AIRS integration

Review source and target fields and view imported data on tables and records in your ServiceNow ServiceNow AI Platform instance.

## Field mapping for scan findings

The following tables show how Prisma AIRS payload fields map to ServiceNow AI Platform target tables and columns for scan finding data.

|Input field \(payload key\)|Target table|Target column|
|---------------------------|------------|-------------|
|asset.asset\_type|sn\_sec\_ai\_src\_ci|asset\_type|
|asset.asset\_id|sn\_sec\_ai\_src\_ci|source\_asset\_id|
|asset.asset\_name|sn\_sec\_ai\_src\_ci|asset\_name|
|asset.version|sn\_sec\_ai\_src\_ci|version|
|asset.asset\_name|cmdb\_ai\_model\_product\_model|name|
|asset.version|cmdb\_ai\_model\_product\_model|version|
|vulnerability.source\_vul\_id|sn\_sec\_ai\_vul\_entry|id|
|vulnerability.description|sn\_sec\_ai\_vul\_entry|description|
|scan.scan\_id|sn\_sec\_ai\_scan\_summary|scan\_id|
|scan.scan\_name|sn\_sec\_ai\_scan\_summary|scan\_name|
|scan.start\_time|sn\_sec\_ai\_scan\_summary|start\_time|
|scan.end\_time|sn\_sec\_ai\_scan\_summary|end\_time|
|scan.scan\_status|sn\_sec\_ai\_scan\_summary|scan\_status|
|file.file\_id|sn\_sec\_ai\_file|id|
|file.file\_path|sn\_sec\_ai\_file|path|
|file.file\_size|sn\_sec\_ai\_file|size|
|file.file\_name|sn\_sec\_ai\_file|name|
|file.format|sn\_sec\_ai\_file|format|
|file.last\_scanned|sn\_sec\_ai\_file|last\_scanned|
|scan\_finding.short\_description|sn\_sec\_ai\_scan\_finding|short\_description|
|scan\_finding.detection\_category|sn\_sec\_ai\_scan\_finding|detection\_category|
|scan\_finding.source\_severity|sn\_sec\_ai\_scan\_finding|source\_severity|

|Field|Target table|Target column|Source|
|-----|------------|-------------|------|
|source|sn\_sec\_ai\_src\_ci|source|metadata \(integration source\)|
|is\_model\_scanned|sn\_sec\_ai\_src\_ci|is\_model\_scanned|Set to true \(reporting\_type=SCAN\)|
|product\_model|sn\_sec\_ai\_src\_ci|product\_model|chain output \(AISecModelCIHandler\)|
|cmdb\_ci|sn\_sec\_ai\_src\_ci|cmdb\_ci|chain output \(AISecModelCIHandler\)|
|source|sn\_sec\_ai\_vul\_entry|source|metadata|
|source|sn\_sec\_ai\_scan\_summary|source|metadata|
|src\_ci|sn\_sec\_ai\_scan\_summary|src\_ci|chain output \(discovered\_ai\_asset\)|
|source|sn\_sec\_ai\_file|source|metadata|
|model|sn\_sec\_ai\_file|model|chain output \(discovered\_ai\_asset\)|
|source|sn\_sec\_ai\_scan\_finding|source|metadata|
|src\_ci|sn\_sec\_ai\_scan\_finding|src\_ci|chain output \(discovered\_ai\_asset\)|
|vulnerability|sn\_sec\_ai\_scan\_finding|vulnerability|chain output \(AISecVulEntryHandler\)|
|scan\_summary|sn\_sec\_ai\_scan\_finding|scan\_summary|chain output \(AISecScanSummaryHandler\)|
|file|sn\_sec\_ai\_scan\_finding|file|chain output \(AISecFileHandler\)|

Tables populated by scan findings:

-   AI Scan Findings \(sn\_sec\_ai\_scan\_finding\)
-   AI Scan Summaries \(sn\_sec\_ai\_scan\_summary\)
-   Discovered AI Assets \(sn\_sec\_ai\_src\_ci\)
-   AI Vulnerability Entries \(sn\_sec\_ai\_vul\_entry\)
-   Model Files \(sn\_sec\_ai\_file\)

## Field mapping for Posture findings

|Input field \(payload key\)|Target table|Target column|
|---------------------------|------------|-------------|
|asset.asset\_type|sn\_sec\_ai\_src\_ci|asset\_type|
|asset.asset\_id|sn\_sec\_ai\_src\_ci|source\_asset\_id|
|asset.asset\_name|sn\_sec\_ai\_src\_ci|asset\_name|
|asset.version|sn\_sec\_ai\_src\_ci|version|
|asset.asset\_name|cmdb\_ai\_model\_product\_model|name|
|asset.version|cmdb\_ai\_model\_product\_model|version|
|posture\_rule.rule\_id|sn\_sec\_ai\_posture\_rule|id|
|posture\_rule.short\_description|sn\_sec\_ai\_posture\_rule|short\_description|
|finding\_evidence.category|sn\_sec\_ai\_finding\_evidence|category|
|finding\_evidence.details|sn\_sec\_ai\_finding\_evidence|details|

|Field|Target table|Target column|Source|
|-----|------------|-------------|------|
|source|sn\_sec\_ai\_src\_ci|source|metadata \(integration source\)|
|product\_model|sn\_sec\_ai\_src\_ci|product\_model|chain output \(AISecModelCIHandler\)|
|cmdb\_ci|sn\_sec\_ai\_src\_ci|cmdb\_ci|chain output \(AISecModelCIHandler\)|
|source|sn\_sec\_ai\_posture\_rule|source|metadata|
|source|sn\_sec\_ai\_posture\_finding|source|metadata|
|ai\_posture\_rule|sn\_sec\_ai\_posture\_finding|ai\_posture\_rule|chain output \(AISecPostureRuleHandler\)|
|src\_ci|sn\_sec\_ai\_posture\_finding|src\_ci|chain output \(discovered\_ai\_asset\)|
|source|sn\_sec\_ai\_finding\_evidence|source|metadata|
|finding|sn\_sec\_ai\_finding\_evidence|finding|chain output \(AISecPostureFindingHandler\)|

Tables populated by posture findings:

-   AI Posture Finding \(sn\_sec\_ai\_posture\_finding\)
-   AI Posture Rule \(sn\_sec\_ai\_posture\_rule\)
-   Discovered AI Assets \(sn\_sec\_ai\_src\_ci\)
-   Finding Evidence \(sn\_sec\_ai\_finding\_evidence\)
-   AI Model Product Model \(cmdb\_ai\_model\_product\_model\)

## Field mapping for Validation findings

|Input field \(payload key\)|Target table|Target column|
|---------------------------|------------|-------------|
|asset.asset\_type|sn\_sec\_ai\_src\_ci|asset\_type|
|asset.asset\_id|sn\_sec\_ai\_src\_ci|source\_asset\_id|
|asset.asset\_name|sn\_sec\_ai\_src\_ci|asset\_name|
|asset.version|sn\_sec\_ai\_src\_ci|version|
|asset.asset\_name|cmdb\_ai\_model\_product\_model|name|
|asset.version|cmdb\_ai\_model\_product\_model|version|
|threat\_signature.threat\_category|sn\_sec\_ai\_threat\_signature|threat\_category|
|threat\_signature.threat\_sub\_category|sn\_sec\_ai\_threat\_signature|threat\_sub\_category|
|threat\_signature.attack\_technique|sn\_sec\_ai\_threat\_signature|attack\_technique|
|threat\_signature.attack\_threat|sn\_sec\_ai\_threat\_signature|attack\_threat|
|threat\_signature.mitre\_technique\[\].technique\_id|sn\_sec\_cmn\_mitre\_technique|technique\_id|
|threat\_signature.mitre\_technique\[\].technique\_name|sn\_sec\_cmn\_mitre\_technique|technique\_name|
|threat\_signature.mitre\_technique \(resolved\)|sn\_sec\_ai\_threat\_signature|mitre\_technique\_list|
|validation\_finding.prompt|sn\_sec\_ai\_validation\_finding|prompt|
|validation\_finding.short\_description|sn\_sec\_ai\_validation\_finding|short\_description|
|threat.prompt|sn\_sec\_ai\_validation\_threat|prompt|
|threat.response|sn\_sec\_ai\_validation\_threat|response|
|threat.source\_severity|sn\_sec\_ai\_validation\_threat|source\_severity|
|threat.status|sn\_sec\_ai\_validation\_threat|status|
|threat.last\_seen|sn\_sec\_ai\_validation\_threat|last\_seen|

|Field|Target table|Target column|Source|
|-----|------------|-------------|------|
|source|sn\_sec\_ai\_src\_ci|source|metadata \(integration source\)|
|is\_model\_validated|sn\_sec\_ai\_src\_ci|is\_model\_validated|Set to true \(reporting\_type=VALIDATION\)|
|product\_model|sn\_sec\_ai\_src\_ci|product\_model|chain output \(AISecModelCIHandler\)|
|cmdb\_ci|sn\_sec\_ai\_src\_ci|cmdb\_ci|chain output \(AISecModelCIHandler\)|
|source|sn\_sec\_ai\_threat\_signature|source|metadata|
|prompt\_hash|sn\_sec\_ai\_validation\_finding|prompt\_hash|auto-generated \(SHA256 of prompt\)|
|response\_hash|sn\_sec\_ai\_validation\_finding|response\_hash|auto-generated \(SHA256 of response\)|
|ai\_threat\_signature|sn\_sec\_ai\_validation\_finding|ai\_threat\_signature|chain output \(AISecThreatSignatureHandler\)|
|src\_ci|sn\_sec\_ai\_validation\_finding|src\_ci|chain output \(discovered\_ai\_asset\)|
|source|sn\_sec\_ai\_validation\_finding|source|metadata|
|prompt\_hash|sn\_sec\_ai\_validation\_threat|prompt\_hash|auto-generated \(SHA256 of prompt\)|
|response\_hash|sn\_sec\_ai\_validation\_threat|response\_hash|auto-generated \(SHA256 of response\)|
|ai\_validation\_finding|sn\_sec\_ai\_validation\_threat|ai\_validation\_finding|chain output \(AISecValidationFindingHandler\)|
|source|sn\_sec\_ai\_validation\_threat|source|metadata|

Tables populated by validation findings:

-   AI Threat Signatures \(sn\_sec\_ai\_threat\_signature\)
-   AI Validation Threats \(sn\_sec\_ai\_validation\_threat\)
-   AI Validation Findings \(sn\_sec\_ai\_validation\_finding\)

**Parent Topic:**[Explore the Palo Alto Prisma AIRS Integration for AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/security-management/prisma-airs-integration.md)

