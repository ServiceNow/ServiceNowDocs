---
title: Exploring Cryptographic Asset Compliance
description: Cryptographic Asset Compliance provides centralized visibility and control of cryptographic assets for proactive risk assessment and post-quantum cryptography \(PQC\) readiness.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/exploring-CAC.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 3
keywords: [explore, cryptographic asset discovery, cryptographic assets, post-quantum cryptography]
breadcrumb: [Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Exploring Cryptographic Asset Compliance

Cryptographic Asset Compliance provides centralized visibility and control of cryptographic assets for proactive risk assessment and post-quantum cryptography \(PQC\) readiness.

## Cryptographic Asset Compliance overview

As quantum computing advances are anticipated to threaten traditional cryptographic algorithms, organizations need comprehensive visibility into their cryptographic assets. Cryptographic Asset Compliance addresses this challenge by automatically inventorying cryptographic assets like certificates, AWS KMS keys, and Azure Key Vault keys across cloud and on-premises environments. This visibility helps you assess your PQC readiness and plan migration strategies.

## Cryptographic Asset Compliance workflow

The typical workflow when implementing Cryptographic Asset Compliance includes the following activities:

1.  Set up discovery: Set up certificate discovery in ServiceNow [Certificate Inventory and Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cert-inventory-mgmt.md) and cloud discovery in ServiceNow [Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/r-discovery.md) \(for AWS and Azure\) so cryptographic assets can be found. A scheduled job then syncs the discovered assets into Cryptographic Asset Compliance.
2.  Review inventory: Analyze discovered cryptographic assets in the inventory, including certificates and keys across all connected sources.
3.  Assess risks: Review the risk indicators identified for your assets, such as weak or quantum-vulnerable algorithms and certificate authority trust or ownership gaps. Use the AI-generated summary and recommendations to understand each asset's risk.
4.  Monitor and maintain: Use dashboards to track cryptographic asset health, PQC compliance status, and quantum vulnerable algorithms.

## Cryptographic Asset Compliance users

|User|Description|
|----|-----------|
|SecOperations Engineer|Need visibility into cryptographic asset inventory to identify keys and certificates for PQC migration planning. They monitor asset health, identify vulnerable algorithms, and prioritize remediation.|
|Compliance and Governance Manager|Require audit-ready reports of cryptographic assets and quantum risk exposure to meet regulatory requirements. They generate compliance reports, track policy adherence, monitor risk indicators, and document remediation efforts.|
|PKI Engineer|Manage certificate life cycle, configure discovery sources, define risk indicators, and monitor certificate expiration. They contribute to proper cryptographic asset governance and operational continuity.|

## Cryptographic Asset Compliance benefits

<table id="table_cad_benefits"><thead><tr><th>

Benefit

</th><th>

Method

</th><th>

Users

</th></tr></thead><tbody><tr><td>

Establish a trusted, up-to-date inventory of cryptographic assets and monitor its risk and PQC readiness by configuring asset discovery and the certificate authorities your organization trusts.

</td><td>

-   [Configuring the discovery of cryptographic assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/set-up-cryptographic-asset-discovery.md)
-   [Configure trusted certificate authorities](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/add-trusted-certificate-authorities.md)
-   [Cryptographic Asset Compliance Home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/home-dashboard-CAC.md)
-   [View and manage cryptographic assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/manage-inventory.md)
-   [View cryptographic asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/view-asset-details.md)

</td><td>

Cryptographic Asset adminsn\_itom\_cac.admin

</td></tr><tr><td>

Monitor the health of cryptographic assets, investigate risk indicators, and track PQC readiness to support remediation and compliance planning, using read access that doesn't change configuration.

</td><td>

-   [Cryptographic Asset Compliance Home page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/home-dashboard-CAC.md)
-   [View and manage cryptographic assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/manage-inventory.md)
-   [View cryptographic asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/view-asset-details.md)

</td><td>

Cryptographic Asset usersn\_itom\_cac.user

</td></tr></tbody>
</table>## What to explore next

-   [Post-quantum cryptography overview](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/pqc-overview-CAC.md)
-   [Cryptographic risk indicators](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/risk-indicators-CAC.md)
-   [About Policy as Code Engine policies](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/policies-and-risk-indicators.md)

