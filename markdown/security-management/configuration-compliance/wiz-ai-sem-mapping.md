---
title: Wiz to AI Security data mapping
description: How Wiz resource types, severities, statuses, and posture finding fields map to AI Security values when AI Security Exposure Management routing is enabled.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/configuration-compliance/wiz-ai-sem-mapping.html
release: brazil
product: Configuration Compliance
classification: configuration-compliance
topic_type: reference
last_updated: "2026-09-10"
reading_time_minutes: 1
keywords: [Wiz, AI Security Exposure Management, data mapping, posture findings]
breadcrumb: [Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Wiz to AI Security data mapping

How Wiz resource types, severities, statuses, and posture finding fields map to AI Security values when AI Security Exposure Management routing is enabled.

## Resource type to asset type mapping

|Wiz resource type|AI Security asset type|
|-----------------|----------------------|
|AI\_AGENT|agent|
|AI\_DATASET|dataset|
|AI\_MODEL|model|
|AI\_TOOL|tool|
|MCP\_SERVER|mcp\_server|

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

