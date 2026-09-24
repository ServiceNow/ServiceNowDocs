---
title: Wiz AI-SEM integration
description: The Wiz AI-SEM \(Security Exposure Management\) integration extends the Test Results Integration with Configuration Compliance that is included with Vulnerability Response Integration with Wiz application. It routes posture findings for AI resources imported from Wiz into AI Security Exposure Management \(AI-SEM\) and Configuration Compliance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/security-management/configuration-compliance/wiz-ai-sem-integration.html
release: brazil
product: Configuration Compliance
classification: configuration-compliance
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Wiz, AI-SEM, AI Security Exposure Management, posture findings, Configuration Compliance, AI resources, AI assets]
breadcrumb: [Integrate, Configuration Compliance, Unified Security Exposure Management, Security Operations]
---

# Wiz AI-SEM integration

The Wiz AI-SEM \(Security Exposure Management\) integration extends the Test Results Integration with Configuration Compliance that is included with Vulnerability Response Integration with Wiz application. It routes posture findings for AI resources imported from Wiz into AI Security Exposure Management \(AI-SEM\) and Configuration Compliance.

## Applications and benefits

|Supporting core application|Benefit|Wiz integration|Users|
|---------------------------|-------|---------------|-----|
|[AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/security-management/exploring-ai-security-exposure.md)|Import and route AI posture and AI security scan findings from Wiz into test results in the Configuration Compliance application and AI Security Exposure Management for remediation workflows.|Wiz Test Results Integration|AI security teams, vulnerability managers, and vulnerability analysts|

## Integration overview

AI-SEM is part of the AI Security application and tracks security exposure for AI assets such as models, agents, datasets, and MCP servers.

Previously, Wiz posture findings for all resource types, including AI resources, created Configuration Compliance test results only. AI resources have no representation in the Configuration Compliance asset model, so findings against them provide limited context. The integration adds a resource category for AI assets and a dedicated processing path. This path maps Wiz posture findings for AI resources into AI Security records, where they can be evaluated alongside other AI asset risk data.

The capability is disabled by default. An administrator opts in from the Wiz configuration form.

## Data flow from Wiz to AI Security

When AI Security Exposure Management routing is enabled, each imported Wiz posture finding for an AI resource is processed as follows:

1.  The integration reads the resource and rule details from the Wiz posture finding payload.
2.  The resource type is matched to an AI Security asset type. Findings for unmapped resource types are skipped and logged as a warning.
3.  An asset, a posture rule, and a posture finding are submitted to AI Security through its import API.

For the field, severity, and status mappings used in this process, see the Wiz to AI Security data mapping reference topic.

## AI resource types and categories

The Wiz resource types table \[sn\_vul\_wiz\_resource\_types\] includes a Category field. Existing resource types are categorized as Host Vulnerabilities or Test Results. The integration adds an AI Security category and the following resource types:

-   AI\_AGENT
-   AI\_AGENT\_REGISTRY
-   AI\_DATASET
-   AI\_EXTENSION
-   AI\_GATEWAY
-   AI\_GUARDRAIL
-   AI\_MODEL
-   AI\_PIPELINE
-   AI\_SECURITY\_FINDING
-   AI\_SERVICE
-   AI\_SKILL
-   AI\_SKILL\_TEMPLATE
-   AI\_TOOL
-   MCP\_SERVER

**Note:** Only five of these resource types map to an AI Security asset type. See the resource type to asset type mapping in the Wiz to AI Security data mapping reference topic. Wiz posture findings for the remaining resource types are recognized as AI resources but are not yet forwarded to AI Security.

## Known limitations

Wiz does not currently include supporting evidence in the posture finding payload, so the evidence field on the AI Security finding is not populated. Evidence population is planned for a future release once Wiz provides that data.

## Related components

The integration extends the AI Security posture rule and test table model, and the Configuration Compliance test table. AI Security findings received from the integration link to posture rules the same way other Configuration Compliance findings do. Those components are owned by the AI Security and Configuration Compliance applications. For more information, see the AI Security and Configuration Compliance documentation.

