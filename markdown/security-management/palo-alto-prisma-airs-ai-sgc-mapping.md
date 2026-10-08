---
title: Palo Alto Prisma AIRS to ServiceNow data mapping
description: Prisma AIRS API fields map to ServiceNow fields for AI models, vulnerability scans, red teaming scans, and compliance data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/palo-alto-prisma-airs-ai-sgc-mapping.html
release: zurich
topic_type: reference
last_updated: "2026-09-15"
reading_time_minutes: 1
keywords: [Palo Alto Prisma AIRS, data mapping, field mapping, AI models, vulnerability scans, red teaming]
breadcrumb: [AI Service Graph Connector for Palo Alto Prisma AIRS, Integrations, Unified Security Exposure Management, Security Operations]
---

# Palo Alto Prisma AIRS to ServiceNow data mapping

Prisma AIRS API fields map to ServiceNow fields for AI models, vulnerability scans, red teaming scans, and compliance data.

## View imported data

|Data|Table name|Where to view|
|----|----------|-------------|
|AI models|cmdb\_ai\_model\_product\_model|AI Discovery and AI Control Tower asset inventory|
|Vulnerability scans|sn\_ai\_prsmair\_disc\_sg\_vulnerability\_scans|**Filter navigator** &gt; **Table name**|
|Vulnerability scan violations|sn\_ai\_prsmair\_disc\_sg\_vulnerability\_scans\_violations|**Filter navigator** &gt; **Table name**|
|Red teaming scans|sn\_ai\_prsmair\_disc\_sg\_red\_teaming\_scan|**Filter navigator** &gt; **Table name**|
|Red teaming attacks|sn\_ai\_prsmair\_disc\_sg\_red\_teaming\_attack|**Filter navigator** &gt; **Table name**|
|Red teaming compliance|sn\_ai\_prsmair\_disc\_sg\_red\_teaming\_compliance|**Filter navigator** &gt; **Table name**|

Summarized vulnerability and red teaming metrics also appear on the AI Security Operations dashboard.

## AI models

|Prisma AIRS field|Target field|
|-----------------|------------|
|uuid|uuid|
|name|name|
|latest\_version\_revision|version|
|\(constant: Prisma AIRS\)|manufacturer|
|latest\_version\_outcome|latest\_version\_outcome|
|latest\_version\_source\_types|latest\_version\_source\_types|
|latest\_version\_formats|latest\_version\_formats|
|latest\_version\_scan\_time|latest\_version\_scan\_time|
|tsg\_id|tsg\_id|

Each imported AI model also creates a linked digital asset \(ALM\) record for application lifecycle management tracking, keyed by the model's unique identifier.

## Vulnerability scans

|Prisma AIRS field|Target field|
|-----------------|------------|
|uuid|scan\_uuid|
|tsg\_id|tsg\_id|
|model\_uri|model\_uri|
|owner|owner|
|scan\_origin|scan\_origin|
|security\_group\_uuid|security\_group\_uuid|
|security\_group\_name|security\_group\_name|
|model\_version\_uuid|model\_version\_uuid|
|scanner\_version|scanner\_version|
|sdk\_version|sdk\_version|
|eval\_outcome|eval\_outcome|

## Vulnerability scan violations

|Prisma AIRS field|Target field|
|-----------------|------------|
|uuid|violation\_uuid|
|scan\_uuid \(parent\)|scan\_uuid|
|tsg\_id|tsg\_id|
|description|description|
|threat|threat|
|operator|operator|
|module|module|
|rule\_instance\_uuid|rule\_instance\_uuid|
|rule\_name|rule\_name|
|rule\_description|rule\_description|
|rule\_instance\_state|rule\_instance\_state|

## Red teaming scans

|Prisma AIRS field|Target field|
|-----------------|------------|
|uuid|scan\_id|
|target\_id|target\_id|
|target.name|target\_name|
|status|status|
|job\_type|job\_type|
|asr|attack\_success\_rate|
|score|score|

## Red teaming attacks

|Prisma AIRS field|Target field|
|-----------------|------------|
|attack\_id|attack\_id|
|scan\_id \(parent\)|scan\_id|
|target\_id|target\_id|
|category|category|
|category\_display\_name|category\_display\_name|
|sub\_category|sub\_category|
|severity|severity|
|attack\_type|attack\_type|

## Red teaming compliance

|Prisma AIRS field|Target field|
|-----------------|------------|
|\(resolved attack reference\)|attack|
|compliance\_frameworks.id|compliance\_framework\_id|
|compliance\_frameworks.techniques.id|technique\_id|
|compliance\_frameworks.techniques.description|technique\_description|

**Parent Topic:**[Palo Alto Prisma AIRS AI Service Graph Connector](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/palo-alto-prisma-airs-ai-sgc.md)

