---
title: Using AI remediation workflows with Employee Center
description: AI Security Exposure Management integrates with Employee Center and third-party security tools to enable AI asset owners to remediate AI posture findings \(configuration issues\) directly through lightweight tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/security-management/ai-security-exposure-employee-workflow.html
release: zurich
topic_type: concept
last_updated: "2026-09-03"
reading_time_minutes: 4
keywords: [AI security, remediation, Employee Center, vulnerability management]
breadcrumb: [AI Security Exposure Management, Use, Unified Security Exposure Management, Security Operations]
---

# Using AI remediation workflows with Employee Center

AI Security Exposure Management integrates with Employee Center and third-party security tools to enable AI asset owners to remediate AI posture findings \(configuration issues\) directly through lightweight tasks.

## Remediation workflow overview

AI Security Exposure Management routes an eligible AI exposure finding to a corresponding AI exposure task that is created in Employee Center. AI exposure tasks are routed directly to asset owners. These tasks can reduce time to remediate \(TTR\).

An AI exposure task is created for any AI posture finding that matches the filter of the sn\_sec\_ai.create\_employee\_tasks\_ai\_posture system property. This approach distributes remediation tasks to the individuals who own and manage AI assets, allowing them to address security issues directly. Multiple remediation paths are available and thus reduces the burden on centralized vulnerability teams.

This approach is also useful for security posture findings identified in AI agents or associated AI assets in no-code or low-code platforms such as Microsoft Copilot studio. These agents are created by business users for productivity gains and don't involve application developers.

The system uses third-party integrations to import AI posture findings for misconfigurations identified in agents, tools, and other AI assets and match them to AI asset owners. Tasks in Employee Center are automatically created based on AI asset ownership and displayed along with other requests. Each task is associated with a distinct AI asset.

The AI exposure task provides asset owners with a streamlined interface to either resolve the configuration issue or request an exception quickly.

## Task routing and assignment

When AI Security Exposure Management detects a finding, the creates a task and routes it to the appropriate AI asset owner in Employee Center. The integration with third-party AI security platforms identify the owners of each AI asset, ensuring that tasks reach the correct owners. Task records and states are synched to AI posture findings that can be monitored by analysts and managers in the AI Security Exposure Management module dashboard.

Each employee typically receives one task per AI asset and security finding combination they own.

## Remediation options

The remediation workflow uses a simplified resolve-or-request-exception model. Asset owners can take one of two actions:

-   Mark the task as resolved by remediating the underlying security issue.
-   Request an exception if the finding does not apply to their use case or if mitigating controls are already in place

This lightweight approach helps with routing tasks to end users or employees directly. It enables them to remediate critical misconfigurations in the AI agents they create without requiring vulnerability analysts to triage and analyze each finding.

## Examples of common AI security issues addressed

The Employee Center remediation workflow addresses several categories of AI security exposures found at the employee level:

-   **Over scoped connectors**

    Connectors in platforms such as Microsoft Copilot Studio that have excessive permissions beyond what is required for their intended function. Asset owners can review and reduce connector permissions to align with the principle of least privilege.

-   **Permissions problems in shared skills**

    AI skills or capabilities that are shared across multiple users or teams with inappropriate access controls. Asset owners can adjust permissions to restrict access to authorized users only.

-   **AI infrastructure configuration issues**

    Misconfigurations in AI agents, tools, prompts, or MCP servers that create security exposures. Asset owners can correct configuration settings to align with security policies.


## Task lifecycle and completion

When an asset owner resolves a finding, the associated AI exposure task moves to the complete tab in Employee Center. The system monitors scan imports of the underlying exposure to verify that the issue has been addressed. If the exposure persists or reappears, the system creates a new task to alert the asset owner.

This continuous monitoring approach confirms that resolved findings remain closed and that new or recurring exposures receive prompt attention. Asset owners can track their remediation progress and view historical tasks through the Employee Center interface.

## Benefits of distributed remediation

Integrating AI exposure remediation with Employee Center provides several advantages:

-   Reduces the burden on centralized vulnerability management teams by distributing remediation tasks to asset owners
-   Decreases AI vulnerability response time by enabling direct action from individuals who understand the asset and its context
-   Scales remediation efforts across large organizations without overwhelming any single team
-   Provides asset owners with visibility into security issues affecting their AI assets
-   Streamlines the remediation process through a simplified task interface that does not require specialized security expertise

-   **[Resolve tasks for AI assets in Employee Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/ai-security-exposure-management-employee-task.md)**  
Resolve the finding or request an exception from Employee Center AI posture findings.

**Parent Topic:**[Exploring AI Security Exposure Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/security-management/exploring-ai-security-exposure.md)

