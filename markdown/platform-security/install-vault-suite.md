---
title: Install Vault Suite
description: Use Vault Suite to deploy ServiceNow Vault and its underlying plugins in a single step, without configuring each plugin separately.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/install-vault-suite.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [Vault Suite, install vault, vault plugins, Admin Home, product hub]
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# Install Vault Suite

Use Vault Suite to deploy ServiceNow Vault and its underlying plugins in a single step, without configuring each plugin separately.

## Before you begin

Your instance must have a ServiceNow Vault entitlement. Without an entitlement, the underlying plugins remain inactive after installation and the tool cards on the [ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-dashboard.md) appear as inactive.

Role required: admin

## About this task

Vault Suite includes ServiceNow Vault and its premium plugins, including Data Privacy, Log Export Service, Zero Trust Access, Field Encryption, and Code Signing. Installing Vault Suite activates all included plugins together.

**Note:** If ServiceNow Vault is already installed on your instance, installing Vault Suite adds the remaining plugins without affecting your existing ServiceNow Vault configuration.

You can install Vault Suite from the Application Manager or from the ServiceNow Vault tile on Admin Home. Both entry points use the same Application Manager installation process and install the same plugins. However the ServiceNow Vault tile appears on Admin Home only when your instance has a entitlement.

## Procedure

1.  Navigate to **All** &gt; **Application Manager** &gt; **Vault Suite**.

    Alternatively, go to Admin Home, select the ServiceNow Vault tile, and then select **Start new setup** to open the ServiceNow Vault product hub page.

2.  Select **Install**.

    Vault Suite begins installing the underlying plugins. Installation may take several minutes to complete.

    If you install from Admin Home, Vault Suite moves to the **Installed** tab on the product hub page when installation completes.


## Result

Vault Suite and the following premium plugins are installed on your instance:

-   Vault Console
-   Data Privacy
-   Log Export Service
-   Zero Trust Access
-   Field Encryption
-   Code Signing

## What to do next

Navigate to the [ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-dashboard.md) to confirm that the tool cards are enabled. On Vault Console 2.1 or later, if your instance doesn't already have policies or configurations for Anonymization and Log Export Service, then ServiceNow Vault can apply ready-to-use defaults to help you get started. For more information, see [Default policies and configurations in ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-default-policies-configs.md).

If you installed from Admin Home, select **Configure** on the product hub page to open the Configuration Console for ServiceNow Vault. In this release, the Configuration Console provides **Open Vault Console**, which navigates to the [ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-dashboard.md). You can also mark the product as configured to record your progress, which doesn't change any configuration.

**Note:**

To use the full range of ServiceNow Vault capabilities from the [ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-dashboard.md), elevate to the roles described in [ServiceNow Vault roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-roles.md).

