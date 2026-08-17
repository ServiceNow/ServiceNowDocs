---
title: View cryptographic asset details
description: View detailed information about an individual cryptographic asset, including its risk indicators, cryptographic properties, AI-generated insights, and dependencies.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/view-asset-details.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2026-07-25"
reading_time_minutes: 1
breadcrumb: [Monitor, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# View cryptographic asset details

View detailed information about an individual cryptographic asset, including its risk indicators, cryptographic properties, AI-generated insights, and dependencies.

## Before you begin

-   The discovery of cryptographic assets is set up. For more information, see [Configuring the discovery of cryptographic assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/set-up-cryptographic-asset-discovery.md).
-   Role required: Cryptographic Asset admin \(sn\_itom\_cac.admin\) or Cryptographic Asset user \(sn\_itom\_cac.user\)

## Procedure

1.  Navigate to **All** &gt; **Cryptographic Asset Compliance**.

2.  In the main navigation, select the Inventory icon \[Omitted image "inventory-icon.png"\] Alt text:.

3.  Select the asset name.

4.  Select the **Details** tab and review the following information.

    |Metric|Description|
    |------|-----------|
    |PQC compliant|Whether the asset uses post-quantum-safe algorithms.|
    |Risk indicators|The active risk indicators detected for the asset, such as a weak algorithm or trusted CA risk.|
    |AI Insights|An AI-generated analysis of the asset's risk. For more information, see [AI insights and dependency details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/ai-insights-and-dependency-details.md).|
    |Details|Key attributes of the asset, such as validity dates, owner, team, and environment.|
    |Cryptographic summary|The cryptographic properties of the asset. The displayed fields vary by asset type. For more details, see [Cryptographic summary fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/cryptographic-summary-fields.md).|
    |Lifecycle metrics|The creation, expiry, and last attested date of a certificate. This field is displayed only if the cryptographic asset is a certificate.|

5.  Review where the asset is used by selecting the **Dependency graph** tab.

    For more information, see [AI insights and dependency details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/ai-insights-and-dependency-details.md).


