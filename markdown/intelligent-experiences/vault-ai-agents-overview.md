---
title: ServiceNow Vault AI agents
description: The following AI agents are available for ServiceNow Vault.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/vault-ai-agents-overview.html
release: brazil
topic_type: concept
last_updated: "2026-08-04"
reading_time_minutes: 3
breadcrumb: [ServiceNow Vault AI agents, AI agents library, AI agents and agentic workflows, Enable AI Experiences]
---

# ServiceNow Vault AI agents

The following AI agents are available for ServiceNow Vault.

-   **[Access Observer configuration manager AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-access-observer-configuration-manager-ai-agent.md)**  
This ServiceNow Vault agent helps users to manage Access Observer configurations for specific fields
-   **[Access validation for privacy advanced configurations AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-access-validation-for-privacy-advanced-configurations-ai-agent.md)**  
This ServiceNow Vault agent checks a user's access to manage privacy policy advanced configuration.
-   **[Create Data Privacy advanced configuration AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-create-data-privacy-advanced-configuration-agent-ai-agent.md)**  
This ServiceNow Vault agent helps users fetch, create, activate, and link data privacy policy configurations across data channels.
-   **[Custom app recommendations AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-custom-app-recommendations-agent-ai-agent.md)**  
This ServiceNow Vault agent lists the custom apps on the instance, and shows recommendations along with the available protections for the selected apps.
-   **[Data Discovery policy and job manager AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-data-discovery-policy-and-job-manager-agent-ai-agent.md)**  
This ServiceNow Vault agent checks whether a given list of tables supports data discovery scanning. The agent then creates data discovery job policies using these tables, and creates discovery job policies and schedules and data discovery jobs using the created policy.
-   **[Data Discovery recommendation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-data-discovery-recommendation-agent-ai-agent.md)**  
This ServiceNow Vault agent provides job info, findings, attributes, and related details for a list of tables provided. The agent also returns scan recommendations you can use to create policy and schedule the discovery job by another agent.
-   **[Data Discovery util AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-data-discovery-util-agent-ai-agent.md)**  
This ServiceNow Vault agent assists data stewards in scheduling and managing data discovery jobs by verifying required roles, entitlements, and subscriptions. The agent categorizes discovered data patterns into compliance groups to support regulatory and security requirements. It also help user to add tags to data patterns on demand.
-   **[Data Discovery workflow lookup AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-data-discovery-workflow-lookup-agent-ai-agent.md)**  
This ServiceNow Vault agent receives provide recommendation for different tables associated with workflows, and identifies what kind of sensitive data can present in those tables such as PII,PFI,PCI,PHI,FCI.
-   **[Data pattern list AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-data-pattern-list-agent-ai-agent.md)**  
This ServiceNow Vault agent helps users associate data patterns to an data privacy policy configuration. It retrieves the list of available data patterns, captures the user’s selections, extracts the related sys\_ids, assigns data patterns to data privacy policy configuration and validates it.
-   **[DP record selector agent AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-dp-record-selector-agent-ai-agent.md)**  
This ServiceNow Vault agent fetches data using tools or topics to display list of choices related to the action.
-   **[Edit Data Privacy advanced configuration mapping AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-edit-data-privacy-advanced-configuration-mapping-agent-ai-agent.md)**  
This ServiceNow Vault agent helps users complete tasks related to edit data privacy advanced configuration mapping agent.
-   **[Edit privacy advanced configuration AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-edit-privacy-advanced-configuration-agent-ai-agent.md)**  
This ServiceNow Vault agent helps users complete tasks related to edit privacy advanced configuration agent.
-   **[Summarize Access Observer logs AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-summarize-access-observer-logs-ai-agent.md)**  
This ServiceNow Vault agent summarizes access observer logs and provides detailed breakdowns by caller type, users, and roles for specific table and column combinations.
-   **[Vault crypto module manager AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-vault-crypto-module-manager-ai-agent.md)**  
This ServiceNow Vault agent manages the Vault crypto module configuration and access policies. The agent handles encrypted field configurations for fields, and manages module access policies for roles.
-   **[Anonymization Policy Creation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-anonymization-policy-creation-agent-ai-agent.md)**  
The agent guides Data Privacy administrators through creating an anonymization policy. It captures the data channel, policy name, and data class, creates a draft policy, recommends anonymization techniques by data type, and then tries to publish the policy, explaining anything that must be fixed first.
-   **[Real Time Anonymization\(RTA\) Policy Configuration AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-real-time-anonymization-rta-policy-configuration-agent-ai-agent.md)**  
The agent creates Real-Time Anonymization \(RTA\) policies that mask or anonymize sensitive column values as they're accessed. It guides the user through naming the policy, selecting the target columns to anonymize, and choosing any child tables that should inherit the same protection.
-   **[Field Access Auditor AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-field-access-auditor-ai-agent.md)**  
The agent retrieves the non-elevated user roles that have access to a table field, lets the user add or remove roles, and returns the finalized list of roles.
-   **[Anonymization Job Scheduler AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-anonymization-job-scheduler-agent-ai-agent.md)**  
The agent helps Data Privacy administrators schedule anonymization jobs against existing records by using a published anonymization policy. It checks for conflicting jobs, configures the job frequency, targets, and conditions, offers an optional dry run, and asks for explicit confirmation because starting a job is irreversible.
-   **[Real Time Anonymization\(RTA\) Validation AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-real-time-anonymization-rta-validation-agent-ai-agent.md)**  
The agent confirms that Real-Time Anonymization \(RTA\) policy creation is supported for the user, and helps the user configure the tables and active data patterns that an RTA policy requires. The agent can add tables and add or remove active data patterns.
-   **[Real Time Anonymization\(RTA\) Test AI agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/vault-real-time-anonymization-rta-test-agent-ai-agent.md)**  
The agent tests Real-Time Anonymization \(RTA\) by taking a text string from the user and returning the anonymized version.

**Parent Topic:**[ServiceNow AI agents library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/intelligent-experiences/ai-agent-landing-page.md)

