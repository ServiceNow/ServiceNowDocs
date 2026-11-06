---
title: Wiz AI Security Exposure Management integration
description: Import two categories of security findings related to AI security with the Wiz AI Security Exposure Management \(AI-SEM\) integration.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/wiz-ai-sem-integration.html
release: australia
topic_type: concept
last_updated: "2026-10-22"
reading_time_minutes: 2
keywords: [Wiz, AI-SEM, AI Security Exposure Management, posture findings, Configuration Compliance, AI resources, AI assets]
breadcrumb: [Integrate, Unified Security Exposure Management, Security Operations]
---

# Wiz AI Security Exposure Management integration

Import two categories of security findings related to AI security with the Wiz AI Security Exposure Management \(AI-SEM\) integration.

## Application scope

|Supporting core application|Benefit|Wiz integration|Users|
|---------------------------|-------|---------------|-----|
|[AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/exploring-ai-security-exposure.md)|Import and route AI posture and AI security scan findings from Wiz into test results in the Configuration Compliance application and AI Security Exposure Management for remediation workflows.|Wiz Test Results Integration|AI security teams, vulnerability managers, and vulnerability analysts|

The Wiz AI Security Exposure Management integration supports two categories of security findings related to AI security:

-   Cloud configuration findings in AI assets that include issues such as an AWS bedrock agent not configured with guardrails.
-   Vulnerabilities and configuration issues that are found in AI models, agents, and MCP servers that are deployed in cloud compute instances such as EC2 or containers.

Both finding categories are imported into tables in AI Security Exposure Management.

## Integration overview

AI Security Exposure Management imports these two types of AI security findings with the following integrations.

-   **Wiz Test Results Integration for Configuration Compliance**

    This integration has been enhanced to send a sub-set of cloud configuration findings relevant to AI security to the AI posture findings table in AI Security Exposure Management, rather than creating them as test results in Configuration Compliance.

    To send these findings to AI Security Exposure Management, you must first enable this integration by selecting **Send AI security findings to AI security exposure management** on the [Test Results Configuration tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/vulnerability-response/wiz-test-result-tab-filters.md) for the Wiz Vulnerability Integration.

    This step is required for the following reasons:

    -   The AI asset configuration findings require lookup logic that identifies the correct AI assets in the CMDB instead of mapping all findings to a cloud resource configuration item \(CI\).
    -   Any findings related to AI security must be created in the correct tables so they are visible to AI CoE teams in the AI Control Tower and trigger the relevant governance and security workflows.
-   **Wiz AI Security Findings Integration**

    This is a new integration for Wiz that imports the following data:

    -   Open-source model vulnerabilities that are identified by Wiz as Model Risk findings.
    -   AI posture findings \(configuration findings\) that are identified by Wiz as Agent Risk, or MCP servers that are deployed or hosted in cloud compute instances, such as EC2 or containers. For these types of findings, both the AI asset that is impacted and the compute instance that is hosting the AI asset are made available in the AI posture findings through the discovered AI asset.

