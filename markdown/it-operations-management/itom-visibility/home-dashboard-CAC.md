---
title: Cryptographic Asset Compliance Home page
description: The Cryptographic Asset Compliance Home page provides centralized visibility into cryptographic asset health, risk indicators, key metrics, and actionable insights for proactive compliance management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/home-dashboard-CAC.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [home dashboard, metrics, overview, risk indicators]
breadcrumb: [Monitor, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Cryptographic Asset Compliance Home page

The Cryptographic Asset Compliance Home page provides centralized visibility into cryptographic asset health, risk indicators, key metrics, and actionable insights for proactive compliance management.

The Home page presents information to help you assess your post-quantum cryptography \(PQC\) readiness and plan migration strategies.

## Key Metrics

-   Cryptographic assets: The total number of inventoried assets.
-   PQC compliant: Assets that use post-quantum-safe algorithms.
-   At critical risk: Assets that need immediate attention.
-   Asset Type: A breakdown of assets by type \(Certificate, AWS KMS Key, and Azure Key Vault Key\), with colors indicating the risk level: Protected, Medium, High, or Critical.

## Recent risk indicators

Recent risk indicator cards summarize current risk conditions such as assets using weak or outdated algorithms or assets with no assigned owners. Each indicator provides an actionable recommendation.

## Compliance status

The compliance status is the percentage of PQC compliance for each supported regulation: NIST FIPS 204/ML-DSA, NIST FIPS 203/ML-KEM, and ISO/IEC 27001 Annex A 8.24. The available compliance statuses are: Not compliant, Partially compliant, and Compliant.

## Quantum-vulnerable algorithms

Quantum-vulnerable algorithms are ranked by the number of affected assets, with guidance to plan replacement by 2035 per NIST IR 8547. You can select the number of assets to view a filtered list of the assets on the **Inventory** page. For more information, see [View and manage cryptographic assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/manage-inventory.md).

## Cryptographic asset breakdown

Per-asset-type counts with key risk indicators.

-   Certificates: The total, at critical risk, weak algorithm, and trusted CA risk assets.
-   AWK KMS Keys: The total, weak algorithms, and pending deletion assets.
-   Azure Key Vault Keys: The total, critical risk, weak algorithm, and expired assets.

