---
title: Configuring the discovery of cryptographic assets
description: Configuring the discovery of cryptographic assets involves setting up certificate and cloud discovery.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/itom-visibility/set-up-cryptographic-asset-discovery.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-07-24"
reading_time_minutes: 2
breadcrumb: [Configure, Cryptographic Asset Compliance, ITOM Visibility, IT Operations Management]
---

# Configuring the discovery of cryptographic assets

Configuring the discovery of cryptographic assets involves setting up certificate and cloud discovery.

Cryptographic Asset Compliance inventories the assets that ServiceNow [Certificate Inventory and Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cert-inventory-mgmt.md) and ServiceNow [Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/r-discovery.md) discovers rather than running discovery of cryptographic assets itself.

You must configure the discovery of cryptographic assets:

-   Certificate discovery in [Certificate Inventory and Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cert-inventory-mgmt.md) to catalog certificates \(on-premises and URL-based\). For more information, see [Visibility to TLS certificates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/run-cert-discovery.md).
-   Cloud discovery in [Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/r-discovery.md) to catalog keys from AWS KMS and Azure Key Vault. For more information, see [Discovery for cloud environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery/cloud-discovery-wizard.md).

After discovery is set up, a scheduled job syncs discovered assets into Cryptographic Asset Compliance periodically.

## Onboarding from the Home page

The Home page includes a guided onboarding that helps you configure cloud and certificate discovery. The banner is collapsible and is displayed until the discovery of all cryptographic assets is configured.

The Certificates card indicates whether certificate discovery is configured by displaying either the Setup required or Configured states.

The Keys card indicates whether cloud discovery is configured by displaying the following states.

-   Setup required: Cloud discovery is not configured for AWS KMS and Azure Key Vault.
-   Partially configured: Cloud discovery is configured for either AWS KMS or Azure Key Vault.
-   Configured: Cloud discovery is configured for both AWS KMS and Azure Key Vault.

