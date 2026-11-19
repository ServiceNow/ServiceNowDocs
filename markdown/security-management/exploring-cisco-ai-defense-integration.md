---
title: Cisco AI Defense integration for AI security exposure management
description: The Vulnerability Response Integration with Cisco AI Defense imports AI model vulnerabilities and AI model validation data \(results from automated red teaming or pentests\) into your ServiceNow AI Platform instance. Use this data to detect security risks, drive remediation workflows, and verify compliance with AI security requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/exploring-cisco-ai-defense-integration.html
release: australia
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 3
breadcrumb: [Integrate, Unified Security Exposure Management, Security Operations]
---

# Cisco AI Defense integration for AI security exposure management

The Vulnerability Response Integration with Cisco AI Defense imports AI model vulnerabilities and AI model validation data \(results from automated red teaming or pentests\) into your ServiceNow AI Platform instance. Use this data to detect security risks, drive remediation workflows, and verify compliance with AI security requirements.

## Cisco AI Defense

Cisco AI Defense is a security platform that helps organizations discover and assess security risks in AI assets, including model vulnerabilities, behavioral weakness discovered through red teaming or validation runs, and configuration or posture issues.

## The ServiceNow®Vulnerability Response Integration with Cisco AI Defense

The ServiceNow®Vulnerability Response Integration with Cisco AI Defense enables you to import current Cisco AI Defense data into your ServiceNow AI Platform instance. With this imported data, you can track vulnerabilities in open-source models, AI validation results, and security policies to evaluate your exposure to AI-related vulnerabilities.

## Key features

-   A user with the integration-specific role configures the connection to Cisco AI Defense through a dedicated configuration UI. The user provides the API token, which is validated and then saved in the instance parameters for future use by the integration.
-   The integration can be executed manually or scheduled to run automatically to pull model vulnerabilities and AI model validation data from Cisco AI Defense into your ServiceNow AI Platform AI instance.
-   After the data is imported, it is validated and processed automatically through transform maps.
-   You view the processed data mapped to records in modules created for this integration under AI Security.

## Data retrieved from Cisco AI Defense

This integration retrieves three types of data from Cisco AI Defense:

-   **AI model vulnerabilities**

    Detects vulnerabilities in AI model files, such as malicious code in serialized models including Keras Lambda layers with dangerous patterns.

-   **AI validation results**

    Results of tests performed on AI models against various attack scenarios to identify weaknesses, including prompts, responses, and threat signatures.

-   **AI security policies and guardrails**

    Policy configuration imported from Cisco AI Defense, including policy status and connection type, and the guardrail rules linked to each policy.


All data is stored in your CMDB in ServiceNow AI Platform AI Security tables for tracking, remediation, and reporting.

## Prerequisites

Before activating and using the Cisco AI Defense integration, confirm you have the following:

Required plugins:

-   Vulnerability Response Integration Framework \(sn\_vul\_int\_fw\)
-   AI Security \(sn\_sec\_ai\)
-   AI Discovery \(sn\_ai\_disc\)

Cisco AI Defense account requirements:

-   Active Cisco AI Defense subscription
-   API access credentials \(Tenant API Key\)

Your ServiceNow AI Platform instance name is required.

## Integrations

Navigate to **All** &gt; **Cisco AI Defense Integration** &gt; **Integrations**

|Integration|Description|
|-----------|-----------|
|Cisco AI Defense Model Validation Details Integration|Retrieves detailed validation results|
|Cisco AI Defense Model Validation Integration|Retrieves validation job summaries|
|Cisco AI Defense Policies Integration|Retrieves policies|
|Cisco AI Defense Policy Details Integration|Retrieves policy details|
|Cisco AI Defense Scan Details Integration|Retrieves detailed model vulnerability scan findings|
|Cisco AI Defense Scans Integration|Retrieves vulnerability scan summaries|

-   **[Install the Vulnerability Response Integration with Cisco AI Defense](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/install-cisco-ai-defense-integration.md)**  
Install and configure the ServiceNow AI Platform Integration with Cisco AI Defense application in your ServiceNow AI Platform® instance to import scan results and model validation data from Cisco AI Defense.
-   **[Vulnerability Response Integration with Cisco AI Defense data mapping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/use-cisco-ai-defense-integration.md)**  
View and work with imported data from the Vulnerability Response Integration with Cisco AI Defense scan results and model validation data on records and dashboards in your ServiceNow AI Platform instance.

**Parent Topic:**[Unified Security Exposure Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/integrating-usem.md)

