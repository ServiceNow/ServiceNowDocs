---
title: ServiceNow Vault release notes
description: The ServiceNow Vault application provides a set of data security tools that protect sensitive information from unauthorized access, corruption, or theft throughout its entire life cycle. ServiceNow Vault was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [vault, release notes]
---

# ServiceNow Vault release notes

The ServiceNow® Vault application provides a set of data security tools that protect sensitive information from unauthorized access, corruption, or theft throughout its entire life cycle. ServiceNow Vault was enhanced and updated in the Australia release.

## ServiceNow Vault highlights for the Australia release

[Australia Patch 1](../quality/australia-patch-1.md)

-   Enhance your security posture by securing the data in your custom applications with Ask Now Assist.
-   Surface sensitive data access by users automatically by leveraging Now Assist to configure, audit, and summarize your Access Observer logs.

[Early availability](../quality/australia-all-other-fixes.md)

-   Identify potential threats and data leaks using the new AI Insights section within the ServiceNow Vault console dashboard.
-   Use guided setup to begin autoclassifying sensitive data within your custom applications.

See [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md) for more information.

**Important:** ServiceNow Vault is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Important information for upgrading ServiceNow Vault to Australia

ServiceNow Vault is a bundle of the following products:

-   [ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-vault-landing.md)
-   [Data Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-discovery/data-discovery-landing.md)
-   [Data Privacy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/data-privacy-landing.md)
-   [Zero Trust Access \(ZTA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/session-access.md)
-   [Field Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/field-encryption.md)
-   [Code Signing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/code-signing-landing.md)
-   [Log Export Service \(LES\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/les-intro.md)

**Note:** Field Encryption, Data Discovery, and Data Privacy can be automatically installed using Vault Console.

## New in the Australia release

-   **[Guided setup for custom applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/use-vault-guided-setup.md)**

    Use Ask Now Assist to enhance your security posture autonomously by identifying, classifying, and protecting sensitive data in your custom applications.

-   **[Securing custom apps with the Vault agents agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-securing-custom-apps-agents.md)**

    Propose data classifications and available protections for a custom application. When you install Now Assist for Vault, this agentic workflow is turned on by default.

-   **[Access Observer configuration agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-access-observer-config.md)**

    View, create, deactivate, and delete Access Observer settings for a particular field. The access observer configuration agentic workflow helps you monitor the people and processes that access data on your instance. When you install Now Assist for Vault, this agentic workflow is turned on by default.

-   **[Summarize Access Observer logs agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-access-observer-logs.md)**

    Review and summarize access logs for a specific field, identifying access sources, users, and their roles. For example, you can ask Now Assist to summarize access logs to view users who accessed a field, along with their roles and how they accessed the data. When you install Now Assist for Vault, this agentic workflow is turned on by default.

-   **[Field encryption with Vault module agentic workflow](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/now-assist-vault-field-encryption-module.md)**

    Encrypt specific fields and configure secure access to users with designated roles using the field encryption with vault module agentic workflow. When you install Now Assist for Vault, this agentic workflow is turned on by default.


-   **[Sensitive data monitoring in AI Insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/vault-tools.md)**

    Identify unprotected sensitive data across your configured tables using the AI Insights section in the Vault console dashboard. View users entering sensitive data in unprotected columns and channels, grouped by sensitive data patterns. This information can further be used to prioritize protection efforts.

-   **[Guided setup for custom applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/use-vault-guided-setup.md)**

    Autoclassify and protect the occurrences of sensitive data within your custom applications using guided setup for Vault. This flow helps you to quickly start using Vault capabilities in your own applications.


## Activation information

Install ServiceNow Vault and Now Assist for Vault by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[Data Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-discovery/data-discovery-landing.md)**

    Run a discovery scan to look for data patterns that might be sensitive data. After it's discovered, data can be reviewed or classified for further protection and management.

-   **[Data Classification](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-classification/data-classification.md)**

    Create data classes and organize your data into data classes for better data management. After it's classified, data can be protected at the class level.

-   **[Data anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/dps-data-anonymization.md)**

    Anonymize data by data class with different anonymization techniques to preserve data patterns while removing sensitive data. Data anonymization can help when sanitizing instances for development or removing specific user data because of rights to be forgotten.

-   **[Encryption](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/encryption-landing.md)**

    Securely protect sensitive data while providing access for authorized users, which helps you increase protections from bad actors.

-   **[Zero Trust Access \(ZTA\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/session-access.md)**

    Use continuous authentication on classified sensitive data in real time.


**Parent Topic:**[ServiceNow AI Platform security release notes](now-platform-security-rn-landing.md)

