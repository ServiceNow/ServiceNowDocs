---
title: Default policies and configurations in ServiceNow Vault
description: ServiceNow Vault has a set of ready-to-use policies and configurations for selected tools to help you get started quickly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/vault-default-policies-configs.html
release: australia
topic_type: concept
last_updated: "2026-05-26"
reading_time_minutes: 1
keywords: [vault default policies configurations anonymization log export service]
breadcrumb: [ServiceNow Vault console dashboard, ServiceNow Vault]
---

# Default policies and configurations in ServiceNow Vault

ServiceNow Vault has a set of ready-to-use policies and configurations for selected tools to help you get started quickly.

**Note:** Default policies and configurations are available only on instances with a ServiceNow Vault subscription.

Defaults help new users get started by providing a baseline of ready-to-use settings. The following tools support default policies and configurations:

-   [Anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/data-privacy-classic/dps-data-anonymization.md)
-   [Log Export Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/les-landing-page.md)

## How defaults are applied

Default behavior differs by tool:

-   **Anonymization**

    Default real-time protection policies are added to your instance when you have the Data Privacy plugin and the Vault Console store app installed. These defaults are applied in addition to any existing real-time protection policies. Select **Activate** on the tool card on the [tools page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/vault-tools.md) to apply them.

-   **Log Export Service**

    Default configurations are applied only when no existing Log Export Service configurations exist on your instance. If existing configurations are present, the existing setup applies and no defaults are created. Select **Activate** on the tool card to apply defaults, or **Go to Log Export Service** if configurations already exist.


## View default policies and configurations

Select **View default policies** or **View default configurations** on the tool card to review defaults. Selecting a policy or configuration name opens its management page.

## Log Export Service version requirement

Default Log Export Service configurations require Log Export Service version 3.5.0 and later. On earlier versions, the **Activate** option isn't available and the tool card shows **Go to Log Export Service** instead.

**Parent Topic:**[ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/vault-dashboard.md)

**Related topics**  


[Vault tools and metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/vault-tools.md)

[ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/vault-dashboard.md)

