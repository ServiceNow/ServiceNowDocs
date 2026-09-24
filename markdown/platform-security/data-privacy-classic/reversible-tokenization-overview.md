---
title: Tokenization
description: Tokenization masks sensitive data for unauthorized users using tokens, and stores a mapping of those tokens to the original data on the instance. Users with authorized roles can retrieve the original data by prompting within the ServiceNow Otto panel.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/data-privacy-classic/reversible-tokenization-overview.html
release: brazil
product: Data Privacy \(Classic\)
classification: data-privacy-classic
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 4
breadcrumb: [Data privacy, Data Privacy, Platform Privacy]
---

# Tokenization

Tokenization masks sensitive data for unauthorized users using tokens, and stores a mapping of those tokens to the original data on the instance. Users with authorized roles can retrieve the original data by prompting within the ServiceNow Otto panel.

Tokenization addresses scenarios where organizations need to:

-   Anonymize sensitive data in a format-preserving manner that maintains data utility
-   Protect sensitive information visible in user interfaces and reports
-   Allow authorized high-privilege users to view original data when needed \(e.g., incident investigation\)
-   Maintain detailed audit trails of who accessed sensitive data and when
-   Support compliance requirements that may later require data restoration

Tokenization uses cryptographic keys to create a deterministic mapping between original sensitive values and their tokenized equivalents. The original values are securely stored and can only be accessed by users with the appropriate detokenization permissions.

## Key concepts

-   **Tokenization:** The process of replacing sensitive data with a token \(a substitute value\) while maintaining a reversible mapping.
-   **Detokenization:** The process of converting a token back to its original sensitive value, available only to authorized roles.
-   **Tokenization policy:** A configuration that defines which data entities \(fields, patterns\) are tokenized and how the tokenization is applied.
-   **Data pattern:** A specific type of sensitive information that the policy targets \(e.g., credit card numbers, social security numbers, email addresses\).
-   **Format preservation:** The property of tokenization that maintains the format and structure of the original data \(e.g., a 9-digit social security number remains 9 digits after tokenization\).
-   **Cryptographic key:** The secret key used to create and verify the token-to-value mapping, ensuring only authorized systems can generate or reverse tokens.
-   **Child table tokenization:** Applying tokenization rules to data in related child tables independently from the parent table, maintaining separate tokenization contexts.

## How tokenization works

Tokenization follows these principles:

1.  **Token Generation:** When a tokenization policy is activated, sensitive data matching the defined patterns is replaced with deterministic tokens. The same original value always produces the same token.
2.  **Mapping Storage:** The mapping between original values and tokens is securely stored with the cryptographic key used for generation.
3.  **Real-Time Processing:** For real-time tokenization, data is tokenized as it is accessed or displayed, based on the user's permissions.
4.  **Authorized Access:** Users with detokenization permissions can request to view original values. This access is logged and audited.
5.  **Format Preservation:** The tokenization process maintains the format of the original data, ensuring applications and reports continue to function with the tokenized values.

## Common use cases

-   **Data Protection:** Anonymize sensitive customer or employee data in incident records or support tickets while allowing escalations to management when needed.
-   **Compliance:** Meet regulatory requirements \(GDPR, HIPAA, CCPA\) by restricting who can see sensitive data while maintaining the ability to restore it for legitimate purposes.
-   **Development and Testing:** Use tokenized production data in development environments without exposing real sensitive information, while allowing specific users to restore data when necessary for debugging.
-   **Multi-Tenant Scenarios:** Prevent tenant administrators from viewing data of other tenants unless they have explicit detokenization permissions.
-   **Audit and Investigation:** Allow security and compliance teams to tokenize data in logs while enabling privileged investigators to view original values when investigating security incidents.

## Child table tokenization

Tokenization can be applied independently to child tables without affecting parent table tokenization:

-   **Separate contexts:** Child tables maintain their own tokenization context, allowing different policies for related data.
-   **Independent tokens:** The same sensitive value in a parent table and child table can be tokenized differently.
-   **Flexible configuration:** Administrators can choose to tokenize parent data, child data, or both, depending on security requirements.

## Best practices

-   **Principle of least privilege:** Grant detokenization permissions only to users who have a legitimate business need to access the original values.
-   **Audit regularly:** Review audit logs of de-tokenization activities to ensure access is appropriate and within policy.
-   **Test policies:** Create and test policies in non-production environments before deploying to production.
-   **Document your policies:** Maintain clear documentation of what data is tokenized, why, and who can access original values.
-   **Monitor child table tokenization:** When using child table tokenization, ensure that the tokenization strategy for related data is consistent with your security posture.
-   **Plan for key rotation:** Establish procedures for rotating cryptographic keys while maintaining the ability to access tokenized data.

## Limitations and considerations

-   Real-time tokenization and detokenization operations consume system resources. Consider the performance impact in high-volume scenarios.
-   The security of the tokenization system depends on protecting the cryptographic keys. Ensure[Tokenization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-privacy-classic/reversible-tokenization-overview.md) keys are stored securely and access is controlled.
-   If tokenized data is used in searches, reports, or exports, ensure your use cases account for the tokenized format.
-   While tokenization is format-preserving, certain data types may have constraints on token length or character sets.
-   Tokenization only applies to real-time user data entries.
-   Once data in a form is tokenized, the ability to edit the field is disabled for all users regardless of whether sensitive data is discovered.
-   Selecting **Show sensitive data** is a prerequisite step for users with the elevated role to edit or save the form.

