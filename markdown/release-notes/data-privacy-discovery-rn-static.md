---
title: Data Privacy and Discovery release notes
description: The ServiceNow Data Privacy and Data Discovery applications enable you to discover, classify, and protect sensitive data across your platform. Data Privacy provides tools to anonymize and redact personally identifiable information \(PII\), while Data Discovery helps you identify where sensitive data resides. These applications include controls for real-time data protection, anonymization policies, discovery patterns, and granular access control. See the following sections for release notes by version.The Brazil Early Availability release adds significant enhancements to Data Privacy and Data Discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/data-privacy-discovery-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 6
keywords: [Data Privacy, Data Discovery, anonymization, sensitive data, PII, Data Privacy, Data Discovery, anonymization, OCR, tokenization, PII detection]
breadcrumb: [ServiceNow AI Platform security release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Data Privacy and Discovery release notes

The ServiceNow Data Privacy and Data Discovery applications enable you to discover, classify, and protect sensitive data across your platform. Data Privacy provides tools to anonymize and redact personally identifiable information \(PII\), while Data Discovery helps you identify where sensitive data resides. These applications include controls for real-time data protection, anonymization policies, discovery patterns, and granular access control. See the following sections for release notes by version.

## About Data Privacy and Discovery

-   Discover sensitive data across your platform by identifying where personally identifiable information \(PII\) resides in databases, files, emails, and images using multiple detection methods including regex patterns and OCR.
-   Classify and categorize sensitive data to understand the scope and risk profile of PII within your organization.
-   Anonymize sensitive data using multiple techniques including masking, redaction, tokenization, and format-preserving transformation to meet compliance requirements while maintaining data utility.
-   Control access to sensitive data at the record and field level using row-table access \(RTA\) policies and security attributes to enforce least-privilege principles.
-   Monitor and audit data protection operations with activity logs, discovery findings, and anonymization dashboards for defensible compliance reporting.

See Data Privacy documentation and Data Discovery documentation for more information.

## Activation and other requirements

-   **Activation information**

    Data Privacy and Data Discovery are available with activation of the following plugins:

    -   Data Privacy plugin: sn\_dp\_store\_app \(version 9.0 or later\)
    -   Data Discovery plugin: sn\_data\_discovery \(version 9.0 or later\)
    Upon activation, navigate to the Data Privacy or Data Discovery Store app to configure policies, patterns, roles, and settings for your environment.

-   **Upgrade information**

    Before upgrading to this release, review the product documentation for any breaking changes or upgrade considerations specific to your current version. Test upgrades in a non-production instance first to ensure compatibility with your workflows and customizations.

-   **Browser requirements**

    For optimal performance with Data Privacy and Discovery features, use the latest release of Chrome, Firefox, or Safari. Internet Explorer is not supported. Modern browsers with JavaScript enabled are required for all interactive features.

-   **Additional requirements**
    -   Appropriate user roles assigned: Data Privacy Admin, Data Discovery Admin, and other role-based permissions for specific features.
    -   For OCR image discovery: Modern browser with JavaScript enabled; image file size limits apply \(typically 10 MB or less\).
    -   For reversible tokenization: Cryptographic key management system configured with authorized roles defined for de-anonymization access.
    -   For bring your own PII detection: External PII service endpoint accessible with credentials securely stored.
    -   For granular findings storage: Sufficient database storage for storing individual record references; retention policies should be defined.

## Accessibility and localization

-   **Accessibility information**
    -   All user interface elements in Data Privacy and Data Discovery meet WCAG 2.1 Level AA standards for accessibility. The Store apps and all workflows are fully navigable by keyboard and compatible with screen readers including JAWS and NVDA.
    -   Screen reader support includes proper ARIA labels for all UI components including policy configuration, findings inspection, and job management interfaces.
    -   Color contrast ratios meet WCAG AA standards across all features and workflows.
    -   For accessibility questions or to report accessibility issues, contact ServiceNow Support.
-   **Localization information**

    All user-facing strings in Data Privacy and Data Discovery are localized for supported ServiceNow languages at general availability \(GA\). Supported languages include English, French, German, Spanish, Italian, Japanese, Portuguese, Chinese \(Simplified and Traditional\), and Korean. Language packs are installed automatically when the corresponding ServiceNow base system language plugin is active.


## Brazil Early Availability

The Brazil Early Availability release adds significant enhancements to Data Privacy and Data Discovery.

### What's new

-   **Track granular findings in data discovery jobs**

    Move beyond aggregate discovery statistics to inspect exact records containing sensitive data. Customers can now review individual findings, enabling targeted follow-up actions such as classification, anonymization, or encryption. The system tracks and stores granular findings associated with each discovery job, with authorized access control and cleanup capabilities.

-   **Sensitive data discovery from images using OCR**

    Detect sensitive data in uploaded images \(.jpeg, .png\) using optical character recognition \(OCR\). The system extracts text from images and runs it through the Data Discovery API to identify sensitive data patterns in real time as images are uploaded. This extends discovery capabilities to screenshots and other image attachments frequently uploaded in work notes and comments fields.

-   **Data discovery job for Vault customers**

    New and trial customers automatically receive a default discovery job on activation or license enablement, scanning common sources of sensitive data exposure. The automatic scan provides immediate baseline findings without manual configuration, reducing setup complexity and accelerating time-to-value for the platform.

-   **Inbound email channel creation and configuration migration**

    Create a dedicated inbound email channel for discovering and masking sensitive data in inbound emails through the Data Privacy framework. Existing customers automatically migrate their email configurations to the new channel policy during upgrade, streamlining the admin experience and centralizing email security management. New role-based permissions enable inbound email admins to manage channel-specific policies.

-   **Dry run preview capability**

    Preview anonymization results before executing a real job. The dry run feature executes a mock anonymization on sample records selected from the data in scope, showing administrators exactly how their sensitive data will be transformed. This visibility reduces the risk of unintended data changes and enables informed decision-making before irreversible anonymization operations.

-   **Reversible tokenization of sensitive data**

    Anonymize sensitive data using cryptographic tokenization while maintaining reversibility. Authorized roles can de-anonymize tokenized data on demand, enabling format-preserving anonymization with flexible access control. This approach supports use cases where sensitive data must be protected during normal operations but accessible to high-privilege users on a need-to-know basis.

-   **Bring your own PII detection service**

    Use custom PII detection services instead of built-in detection, enabling enterprise customers to meet strict compliance and data sovereignty requirements. The platform provides a single configuration point for integrating customer-provided anonymization services, similar to bring-your-own LLM capabilities, with secure credential management and consistent enforcement across all AI capabilities.


### What's changed

-   **Row-table access for child tables separate from parent table**

    Configure row-table access \(RTA\) policies with independent rules for child tables, no longer limited to the scope of the parent table policy. Inherited fields can now be managed separately from parent table selections, providing greater granularity in data access control.

-   **Inbound email configuration migration on upgrade**

    Existing inbound email configurations are automatically migrated to the new dedicated channel policy during Brazil upgrade. The legacy email plugin integration is superseded by the new inbound email channel. Customers should migrate to the new framework for a consistent experience. Test the migration in a non-production instance before upgrading production environments.

-   **Dry run capability updated for current anonymization framework**

    The dry run capability has been updated to work seamlessly with the current anonymization framework and provides accurate record counts and field-level anonymization previews. Dry run results now show exact transformations that will be applied during actual anonymization job execution.

-   **Default discovery job pre-configuration for Vault customers**

    Default discovery job configuration for Vault customers now includes pre-configured patterns for common PII types including names, email addresses, phone numbers, social security numbers, and credit cards. Customers can modify or disable these default jobs through the Data Discovery Store app.


**UI changes**

-   New Data Discovery findings view to inspect granular records containing sensitive data, with filtering and access controls.
-   Data Privacy Store app updated with dedicated Inbound Email channel management interface and configuration migration workflow.
-   Anonymization dashboard enhanced to display dry run preview results and comparison with actual job execution.
-   Reversible Tokenization policy cards in the Data Privacy Store app for creating and managing tokenization policies with key access and de-anonymization controls.
-   Bring Your Own PII configuration panel in the Data Privacy Store app for managing external PII detection service credentials and settings.
-   RTA policy configuration updated to support independent child table field selection and management.
-   Licensing alerts added to ensure OCR image discovery and other new features display only when appropriate licenses are active.

