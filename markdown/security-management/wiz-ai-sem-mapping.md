---
title: Wiz AI Security Exposure Management Integration data mapping
description: Wiz resource types, severities, statuses, and posture finding fields map to AI Security values when AI Security Exposure Management routing is enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/wiz-ai-sem-mapping.html
release: australia
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 1
keywords: [Wiz, AI Security Exposure Management, data mapping, posture findings]
breadcrumb: [Wiz AI Security Exposure Management integration, Integrate, Unified Security Exposure Management, Security Operations]
---

# Wiz AI Security Exposure Management Integration data mapping

Wiz resource types, severities, statuses, and posture finding fields map to AI Security values when AI Security Exposure Management routing is enabled.

## Resource type to asset type mapping

|Wiz resource type|AI Security asset type|
|-----------------|----------------------|
|AI\_AGENT|agent|
|AI\_DATASET|dataset|
|AI\_MODEL|model|
|AI\_TOOL|tool|
|MCP\_SERVER|mcp\_server|
|AI\_AGENT\_REGISTRY|ai\_function \(generic\)|
|AI\_EXTENSION|ai\_function \(generic\)|
|AI\_GATEWAY|ai\_function \(generic\)|
|AI\_GUARDRAIL|ai\_function \(generic\)|
|AI\_PIPELINE|ai\_function \(generic\)|
|AI\_SERVICE|ai\_function \(generic\)|
|AI\_SKILL|ai\_function \(generic\)|
|AI\_SKILL\_TEMPLATE|ai\_function \(generic\)|

AI\_SECURITY\_FINDING is not included in this mapping. Posture findings for that resource type continue to create Configuration Compliance test results only, not AI Security records.

## Severity mapping

|Wiz severity|AI Security source severity|
|------------|---------------------------|
|CRITICAL|1|
|HIGH|2|
|MEDIUM|3|
|LOW|4|
|INFORMATIONAL|5|

## Status mapping

|Wiz status|AI Security state|
|----------|-----------------|
|OPEN|1|
|RESOLVED|101|
|REJECTED|3|

## Input fields

|Wiz posture finding field|AI Security target|
|-------------------------|------------------|
|Resource ID|Asset ID|
|Resource name|Asset name|
|Resource provider ID|Asset object ID|
|Rule ID|Posture rule ID|
|Rule name or description|Posture rule short description|
|Rule name|Posture finding short description|
|Rule description|Posture finding description|
|Rule function as control|Posture finding detection category|
|Finding ID and target external ID|Posture finding external ID|
|Severity \(mapped\)|Posture finding source severity|
|Status \(mapped\)|Posture finding state|
|Remediation|Posture finding remediation plan|

