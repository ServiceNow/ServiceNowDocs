---
title: ServiceNow Otto for Vault release notes
description: Version history for the ServiceNow Otto for Vault application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-plat-sec-rn-now-assist-vault.html
release: store
topic_type: reference
last_updated: "2026-10-08"
reading_time_minutes: 3
breadcrumb: [ServiceNow Store - ServiceNow AI Platform Security version history release notes, ServiceNow Store version history release notes]
---

# ServiceNow Otto for Vault release notes

Version history for the ServiceNow Otto for Vault application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 3.1.2 - October 2026**
    -   New
        -   Conversational anonymization policy creation. Create a new anonymization policy through the agent — set the policy details and data class, assign an anonymization technique per column, and, for user-specific policies, choose the user reference column. The validated policy is saved and ready for scheduling
        -   Conversational anonymization job creation and scheduling. Using a new or previously published policy, configure a run-once, weekly, or monthly job through the agent, add optional record-level conditions, confirm the schedule, and monitor execution status from the job schedule summary
        -   Real-time anonymization policy creation through the agent. The agent confirms that real-time anonymization is supported, then lets you select target tables and active data patterns, name the policy, and choose the target and child columns. Once created, the policy anonymizes sensitive data as records are created or updated
        -   Field encryption and auto-generate access policies agentic workflow. Request encryption for a table field, review the roles that currently have access to it, and confirm the final list. The workflow creates a module access policy for each confirmed role and then encrypts the field, so you no longer review access control lists or Access Observer logs to build the role list yourself
        -   Data Privacy setup agent. Configure channel-based data privacy through the agent, including policy creation, data pattern selection, and anonymization technique, so that sensitive data is masked before it is sent to the LLM
    -   Changed
        -   The security\_admin role is no longer used as the role masking agent for the Access Observer and Field Encryption agentic workflows. Following least-privilege principles, these workflows run without elevating to security\_admin
        -   Now Assist for Vault is now ServiceNow Otto for Vault. The application name and its references in the product have changed; functionality is unaffected
-   **Version 2.2.2 - August 2026**
    -   Changed:
        -   Starting with Australia Patch 5, Now Assist for Vault is now ServiceNow Otto for Vault. This name change reflects the evolution of AI assistance on the platform into a conversational, agentic AI experience. All existing functionality, configurations, and AI-powered security capabilities are unchanged.
        -   Azure OpenAI is now the default model for all AI assets in ServiceNow Otto for Vault, including the Discovery data pattern grouping skill and the Data Discovery Job Summarization skill. Existing configurations that use the Now LLM Service continue to work as before, and you can still select the Now LLM Service manually.
-   **Version 2.1.1 - June 2026**
    -   Use Now Assist to Vault to enhance your security posture autonomously by identifying, classifying, and protecting sensitive data in your custom applications.
    -   Surface sensitive data access by users automatically by leveraging Now Assist to configure, audit, and summarize your Access Observer logs.
-   **Version 2.0.0 - April 2026**
    -   New:
        -   Use Now Assist to Vault to enhance your security posture autonomously by identifying, classifying, and protecting sensitive data in your custom applications.
        -   Surface sensitive data access by users automatically by leveraging Now Assist to configure, audit, and summarize your Access Observer logs.
-   **Version 1.0.4 - March 2026**

    Changed: Internal fixes for performance and efficiency.

-   **Version 1.0.3 - December 2025**

    Changed: The generate custom data pattern skill uses the Now LLM Service as the default provider. You can switch to another provider as needed.

-   **Version 1.0.1 - October 2025**

    Now Assist for Vault can make it easier for admin to run common tasks like schedule data discovery job, create custom regex data patterns and also understand who has access to decryption key without going to multiple UI's.

-   **Version 1.0.0 - September 2025**

    Now Assist for ServiceNow Vault helps boost productivity by automating and simplifying routine security tasks, enabling security teams to focus on higher-value activities while ensuring consistent enforcement of data protection policies and accelerating incident response.


