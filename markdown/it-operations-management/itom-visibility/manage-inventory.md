---
title: View and manage cryptographic assets
description: View details of cryptographic assets and filter the data to focus on specific assets, analyze risk indicators, and export details from the Inventory page.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/manage-inventory.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: task
last_updated: "2024-12-19"
reading_time_minutes: 1
keywords: [inventory, asset management, certificates, filtering, cryptographic assets]
breadcrumb: [Monitor, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# View and manage cryptographic assets

View details of cryptographic assets and filter the data to focus on specific assets, analyze risk indicators, and export details from the Inventory page.

## Before you begin

-   Discovery of cryptographic assets must have been set up. For more information, see [Configuring the discovery of cryptographic assets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/set-up-cryptographic-asset-discovery.md).
-   Role required: Cryptographic Asset admin \(sn\_itom\_cac.admin\) or Cryptographic Asset user \(sn\_itom\_cac.user\)

## Procedure

1.  Navigate to **All** &gt; **Cryptographic Asset Compliance**.

2.  In the main navigation, select the Inventory icon \[Omitted image "inventory-icon.png"\] Alt text:.

3.  Review the assets' key metrics.

    |Metric|Description|
    |------|-----------|
    |Cryptographic assets|Total number of discovered cryptographic assets.|
    |PQC compliant|Total number of PQC-compliant and quantum-safe assets.|
    |Not compliant|Total number of cryptographic assets that aren't PQC-compliant.|
    |Critical risk|Total number of cryptographic assets requiring immediate attention.|

4.  View the assets related to the metric by selecting the metric.

5.  Focus on specific assets by applying filters in the **Quick filters** section.

    |Filter|Description|
    |------|-----------|
    |Asset Type|Filter by asset type: Certificate, AWS KMS Key, Azure Key Vault Key.|
    |Risk level|Filter by risk severity: Protected, Medium, High, and Critical.|
    |Risk indicators|Filter by specific risk conditions, such as outdated algorithm and non-compliant.|
    |Algorithm|Filter by cryptographic algorithm, such as RSA-2048 or ECDSA P-384.|
    |PQC compliant|Filter by whether the assets are PQC compliant.|

6.  Apply complex filters using a condition builder by selecting **Filter**.

7.  Sort the list of assets by a specific category in an ascending or descending order by selecting **Sort by**.

8.  Group the list of assets by a specific category by selecting **Group by**.

9.  Export data for external analysis or reporting.

    1.  Select **Export**.

    2.  Select the export format in the **File Type** field.

        The available options are Excel, CSV, JSON, or PDF.

    3.  Select whether you want to download or email the file in the **Delivery Type** field.

    4.  If you selected the email delivery type, in the **Email** field, enter the email address you want to send the email to.

    5.  Select **Export**.

10. View more details about the asset by selecting an asset name.

    For more information, see [View cryptographic asset details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/itom-visibility/view-asset-details.md).


