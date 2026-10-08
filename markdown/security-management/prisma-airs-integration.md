---
title: Palo Alto Prisma AIRS integration
description: The Vulnerability Response Integration with Palo Alto Prisma AIRS imports AI security scan results, posture findings, and model validation data into your ServiceNow AI Platform instance. Use the data to help you detect security risks, drive remediation workflows, and verify compliance with AI security requirements.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/security-management/prisma-airs-integration.html
release: australia
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 3
breadcrumb: [Integrate, Unified Security Exposure Management, Security Operations]
---

# Palo Alto Prisma AIRS integration

The Vulnerability Response Integration with Palo Alto Prisma AIRS imports AI security scan results, posture findings, and model validation data into your ServiceNow AI Platform instance. Use the data to help you detect security risks, drive remediation workflows, and verify compliance with AI security requirements.

## Prisma AI Runtime Security \(AIRS\)

Palo Alto Networks' Prisma AIRS \(AI Runtime Security\) is a security platform that discovers, monitors, and protects AI models, APIs, and data pipelines across an organization. It provides risk assessment, data leakage prevention, prompt injection defense, and runtime anomaly detection for AI deployments.

## Prisma AIRS AI Red Teaming

AI Red Teaming is a Prisma AIRS capability that automatically simulates adversarial attacks against AI models — including prompt injection, jailbreaks, bias, toxicity, and hallucination — and maps findings to frameworks such as OWASP LLM Top 10 and MITRE ATLAS. It helps organizations proactively identify and fix AI security weaknesses before attackers can exploit them.

## The ServiceNow AI Platform Prisma AIRS integration

This integration, developed by ServiceNow engineering, enables you to import current Palo Alto Prisma AIRS data into your ServiceNow AI Platform instance. With this imported data, you can see how AI security scans and model validation results are tracked so you can evaluate your exposure to AI-related vulnerabilities.

## How it works

-   A user with the required role configures the connection to Prisma AIRS through a dedicated configuration UI. The user provides the **API URL**, **Client ID**, **Client Secret**, **TSG ID**, and **Auth URL**. These credentials are validated and then securely saved in the instance parameters for future use by the integration.
-   The integration can be executed manually or scheduled to run automatically to pull scan results and model validation data from Prisma AIRS into your ServiceNow AI Platform instance.
-   After the data is imported, it is validated and processed automatically through transform maps.
-   You view the processed data mapped to records in modules created for this integration under AI Security.

## Data retrieved from the integration

This integration retrieves three types of data from the Palo Alto Prisma AIRS integration:

-   **AI Security Scans**

    Detects vulnerabilities in AI model files, such as malicious code in serialized models including Keras Lambda layers with dangerous patterns.

-   **Model Validation Results**

    Tests performed on AI models against various attack scenarios to identify weaknesses, including prompts, responses, and threat signatures.

-   **Red Team Scan Guardrails**

    Guardrail policy configuration applied during Red Team scans, including the policy identifier, name, and configuration for each guardrail.


Scan findings, posture findings, and validation findings are stored in the AI Security Exposures module.

## Prerequisites

ServiceNow plugins required:

-   Vulnerability Response Integration Framework \(sn\_vul\_int\_fw\)
-   AI Security \(sn\_sec\_ai\)

Prisma AIRS account requirements:

-   Active Prisma AIRS subscription
-   Client ID
-   Client Secret
-   API base URL
-   Authorization URL
-   Palo Alto Prisma tenant service group \(TSG\) ID

-   **[Install the Vulnerability Response integration with Palo Alto Prisma AIRS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/install-prisma-airs-integration.md)**  
Use this task to set up the Vulnerability Response integration with Palo Alto Prisma AIRS and import AI security scan results, posture findings, and model validation data into your ServiceNow AI Platform® instance.
-   **[Viewing imported data for the Vulnerability Response Integration with Palo Alto Prisma AIRS](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/view-prisma-airs-data.md)**  
View and work with imported data from the Vulnerability Response Integration with Palo Alto Prisma AIRS integration on records and dashboards in your ServiceNow AI Platform instance.
-   **[Field mapping for the Prisma AIRS integration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/palo-alto-prisma-airs-mapping.md)**  
These tables map Prisma AIRS payload fields to target tables and columns in your ServiceNow ServiceNow AI Platform instance.

**Parent Topic:**[Unified Security Exposure Management integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/security-management/integrating-usem.md)

