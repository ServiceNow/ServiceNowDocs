---
title: Data protection
description: Learn how ServiceNow security tools such as the Key Management Framework, Field Encryption, and Data Classification work to keep your data secure.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-20"
reading_time_minutes: 3
breadcrumb: [Agentic AI security and governance]
---

# Data protection

Learn how ServiceNow security tools such as the Key Management Framework, Field Encryption, and Data Classification work to keep your data secure.

Now Assist keeps your data secure throughout the AI lifecycle. Additional controls let you manage how personally identifiable information \(PII\) is handled, who can make data sharing decisions, and how sensitive data is discovered and protected across your instance.

## Data transit, storage, and privacy controls

The following topics, all in Now Assist Admin, describe how Now Assist handles your data and how to configure privacy controls for your instance.

-   **[User data usage policy for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/user-data-usage-policy-now-assist.md)**

    Understand how Now Assist transmits, processes, and protects your data, including options to mask sensitive data and control data sharing for model improvements.

-   **[Configuring Data Privacy for Now Assist](configure-now-assist-data-privacy.md)**

    Configure how PII is de-identified before it reaches the large language model, including which data types are caught and how anonymization rules are applied.

-   **[Configure Now Assist privacy policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/configure-privacy-policies.md)**

    Set up privacy policies to control how sensitive information is anonymized during AI processing.

-   **[Assign the data steward role](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/assign-data-steward-role.md)**

    Assign a data steward, the role responsible for making data sharing decisions for Now Assist on your instance.

-   **[Opt out of data sharing for Now Assist](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/opt-out-of-data-sharing-for-now-assist.md)**

    Opt your instance out of data sharing with ServiceNow for AI model improvements from the Admin console Settings page.


## Sensitive data discovery and classification

The following topics describe how to use Now Assist for Vault and Now Assist Data Kit to discover, classify, and protect sensitive data on your instance.

-   **[Key Management Framework](../../encryption/concept/encryption.md)**

    Use the Key Management Framework to create and manage encryption keys that control access to sensitive data on your instance, including keys used by AI agents and agentic workflows.

-   **[Field Encryption](../../encryption/concept/field-encryption.md)**

    Encrypt individual fields on your instance to protect sensitive data at rest, ensuring that AI agents can only access encrypted fields when they have the appropriate permissions.

-   **[Data classification](../../data-privacy-store/concept/dps-data-classification.md)**

    Define and apply data classification labels to identify sensitive content across your instance, helping you understand what data your AI agents can access and where protection controls are needed.

-   **[Now Assist for Vault](../../now-assist-vault/concept/now-assist-vault-landing.md)**

    Learn about the generative AI skills available in Now Assist for Vault for generating custom data patterns, checking role access for encrypted columns, and scheduling data discovery jobs.

-   **[Schedule a Data Discovery job with Now Assist for Vault](../../now-assist-vault/task/schedule-data-discovery-job-now-assist-vault.md)**

    Schedule one-time or recurring Data Discovery jobs to detect sensitive data such as PII or PHI that may be present in inputs to the LLM.

-   **[Check role access for an encrypted column with Now Assist for Vault](../../now-assist-vault/task/check-role-access-now-assist-vault.md)**

    Identify which user roles have access to encryption and decryption keys in your instance to monitor your encryption access posture.

-   **[Generate a custom data pattern by using Now Assist for Vault](../../now-assist-vault/task/generate-custom-data-pattern-now-assist-vault.md)**

    Create a custom regular expression data pattern from a plain-language description and add it as an active data pattern on your instance.

-   **[Find and cleanse sensitive data](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/intelligent-experiences/now-assist-data-kit/sensitive-data.md)**

    Now Assist Data Kit: Scan your datasets for sensitive data including PII, and cleanse identified data before it is used in AI evaluations.


**Parent Topic:**[Agentic AI security and governance](now-assist-security.md)

