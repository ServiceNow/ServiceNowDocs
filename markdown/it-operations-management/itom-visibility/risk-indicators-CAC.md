---
title: Cryptographic risk indicators
description: Risk indicators highlight cryptographic assets that need attention so you can prioritize remediation and track compliance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/itom-visibility/risk-indicators-CAC.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-11-17"
reading_time_minutes: 1
keywords: [risk assessment, vulnerability indicators, compliance, security metrics]
breadcrumb: [Explore, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Cryptographic risk indicators

Risk indicators highlight cryptographic assets that need attention so you can prioritize remediation and track compliance.

Cryptographic Asset Compliance evaluates assets against policies and raises a risk indicator when an asset meets a risk condition. Risk indicators are based on policies, and each indicator points to a specific weakness, such as a weak algorithm or a missing owner. For more information, see [About Policy as Code Engine policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/policies-and-risk-indicators.md). For more information about risk detection criteria, see [Risk indicator definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/risk-indicator-definitions.md).

## Supported risk indicators

For certificates:

-   Weak Algorithm: Uses a deprecated or quantum-vulnerable algorithm.
-   Trusted CA Risk: Issued by an untrusted or unrecognized certificate authority. For more information, see [Configure trusted certificate authorities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/add-trusted-certificate-authorities.md).
-   No Owner: Has no assigned owner or responsible party.
-   No Environment: Is not classified by environment.
-   No Renewal: Has no defined renewal workflow.

For AWS KMS keys and Azure Key Vault keys:

-   Weak Algorithm: Uses a weak or insufficient algorithm or key size.
-   Not PQC ready: Does not use a post-quantum-safe algorithm.
-   Pending Deletion \(AWS KMS keys\): Is scheduled for deletion.
-   Expired \(Azure Key Vault keys\): Has an expiration date that has passed.
-   Key Disabled \(AWS KMS keys and Azure Key Vault keys\): Key is disabled. No other risk indicators are shown for a disabled key.
-   Expiring Soon \(Azure Key Vault keys\): Expires within 30 days.
-   No Renewal: For AWS KMS keys, is older than 365 days or has no creation date. For Azure Key Vault keys, has no expiration date.

## Risk levels

Each asset is assigned an overall risk level, calculated from its active indicators. The available risk levels are:

-   Critical: Severe vulnerabilities requiring immediate attention.
-   High: Significant weaknesses that should be addressed promptly.
-   Medium: Moderate concerns that require monitoring and planning.
-   Protected: Quantum-safe, or no active risk indicators.

