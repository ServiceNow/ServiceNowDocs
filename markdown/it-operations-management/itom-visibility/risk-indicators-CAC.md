---
title: Cryptographic risk indicators
description: Risk indicators highlight cryptographic assets that need attention so you can prioritize remediation and track compliance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/risk-indicators-CAC.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [risk assessment, vulnerability indicators, compliance, security metrics]
breadcrumb: [Explore, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Cryptographic risk indicators

Risk indicators highlight cryptographic assets that need attention so you can prioritize remediation and track compliance.

Cryptographic Asset Compliance evaluates assets against policies and raises a risk indicator when an asset meets a risk condition. Risk indicators are based on policies, and each indicator points to a specific weakness, such as a weak algorithm or a missing owner. For more information, see [About Policy as Code Engine policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/policies-and-risk-indicators.md). For more information about risk detection criteria, see [Risk indicator definitions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/risk-indicator-definitions.md).

## Supported risk indicators

For certificates:

-   Weak algorithm: Uses a deprecated or quantum-vulnerable algorithm.
-   Trusted CA risk: Issued by an untrusted or unrecognized certificate authority. For more information, see [Configure trusted certificate authorities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/add-trusted-certificate-authorities.md).
-   No owner: Has no assigned owner or responsible party.
-   No environment: Is not classified by environment.
-   No renewal process: Has no defined renewal workflow.

For AWS KMS keys and Azure Key Vault keys:

-   Weak algorithm: Uses a weak or insufficient algorithm or key size.
-   Not PQC ready: Does not use a post-quantum-safe algorithm.
-   Not rotated \(AWS KMS keys\): Has not been rotated within the recommended period.
-   Pending deletion \(AWS KMS keys\): Is scheduled for deletion.
-   Expired \(Azure Key Vault keys\): Is expired or lacks a proper expiration date.

## Risk levels

Each asset is assigned an overall risk level, calculated from its active indicators. The available risk levels are:

-   Critical: Severe vulnerabilities requiring immediate attention.
-   High: Significant weaknesses that should be addressed promptly.
-   Medium: Moderate concerns that require monitoring and planning.
-   Protected: Quantum-safe, or no active risk indicators.

