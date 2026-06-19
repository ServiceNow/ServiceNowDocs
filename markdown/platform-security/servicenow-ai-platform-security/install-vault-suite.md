---
title: Install Vault Suite
description: Use Vault Suite to deploy ServiceNow Vault and its underlying plugins in a single step, without configuring each plugin separately.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/servicenow-ai-platform-security/install-vault-suite.html
release: australia
product: ServiceNow AI Platform Security
classification: servicenow-ai-platform-security
topic_type: task
last_updated: "2026-05-26"
reading_time_minutes: 1
keywords: [Vault Suite, install vault, vault plugins]
breadcrumb: [Configuring ServiceNow Vault, ServiceNow Vault]
---

# Install Vault Suite

Use Vault Suite to deploy ServiceNow Vault and its underlying plugins in a single step, without configuring each plugin separately.

## Before you begin

Your instance must have a ServiceNow Vault entitlement. Without an entitlement, the underlying plugins remain inactive after installation and the tool cards on the [ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/vault-dashboard.md) appear as inactive.

Role required: admin

## About this task

Vault Suite includes ServiceNow Vault and its premium plugins, including Data Privacy, Log Export Service, Zero Trust Access, Field Encryption, and Code Signing. Installing Vault Suite activates all included plugins together.

**Note:** If ServiceNow Vault is already installed on your instance, installing Vault Suite adds the remaining plugins without affecting your existing ServiceNow Vault configuration.

## Procedure

1.  Navigate to **All** &gt; **Application Manager** &gt; **Vault Suite**.

2.  Select **Install**.

    Vault Suite begins installing the underlying plugins. Installation may take several minutes to complete.


## Result

Vault Suite and the following premium plugins are installed on your instance:

-   Vault Console
-   Data Privacy
-   Log Export Service
-   Zero Trust Access
-   Field Encryption
-   Code Signing

## What to do next

Navigate to the [ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/vault-dashboard.md) to confirm that the tool cards are enabled. On Vault Console 2.1 or later, if your instance doesn't already have policies or configurations for Anonymization and Log Export Service, then ServiceNow Vault can apply ready-to-use defaults to help you get started. For more information, see [Default policies and configurations in ServiceNow Vault](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/servicenow-ai-platform-security/vault-default-policies-configs.md).

