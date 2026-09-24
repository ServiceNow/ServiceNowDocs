---
title: Default policies and configurations in ServiceNow Vault
description: ServiceNow Vault has a set of ready-to-use policies and configurations for selected tools to help you get started quickly.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-security/vault-default-policies-configs.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
keywords: [vault default policies configurations anonymization log export service]
breadcrumb: [ServiceNow Vault console dashboard, ServiceNow Vault]
---

# Default policies and configurations in ServiceNow Vault

ServiceNow Vault has a set of ready-to-use policies and configurations for selected tools to help you get started quickly.

**Note:** Default policies and configurations are available only on instances with a ServiceNow Vault subscription.

Defaults help new users get started by providing a baseline of ready-to-use settings. The following tools support default policies and configurations:

-   [Anonymization](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/data-privacy-classic/dps-data-anonymization.md)
-   [Log Export Service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/les-landing-page.md)
-   [Zero Trust Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/ca-homepage.md)

## How defaults are applied

Default behavior differs by tool:

-   **Anonymization**

    Default real-time protection policies are added to your instance when you have the Data Privacy plugin and the Vault Console store app installed. These defaults are applied in addition to any existing real-time protection policies. Select **Activate** on the tool card on the [tools page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-tools.md) to apply them.

-   **Log Export Service**

    Default configurations are applied only when no existing Log Export Service configurations exist on your instance. If existing configurations are present, the existing setup applies and no defaults are created. Select **Activate** on the tool card to apply defaults, or **Go to Log Export Service** if configurations already exist.

-   **[Zero Trust Access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/ca-homepage.md)**

    Default step-up authentication policies are created automatically when all of the following conditions are met:

    -   A ServiceNow Vault subscription is present on the instance.
    -   Both Vault Console and the Zero Trust - Continuous Authentication plugin \(`com.snc.zero_trust_continuous_authentication`\) are installed.
    -   No existing Zero Trust Access policies are present. If any policy already exists, the default policies aren't created.
    The default policies protect the following Vault configuration tables: Cryptographic Module \[sys\_kmf\_crypto\_module\], Encrypted Field Configuration \[sys\_platform\_encryption\_configuration\], and Module Access Policy \[sys\_kmf\_crypto\_caller\_policy\].

    When a user tries to access one of these tables, the policy requires re-authentication via MFA \(multi-factor authentication\) for local logins, or redirects SSO users to their identity provider. Maint users are excluded from policy evaluation.

    To review the default policies, select **View default policies** on the Zero Trust Access tool card.

    **Note:** A user with the ca\_admin role can deactivate or reactivate a default policy. To do so, navigate to **All** &gt; **Continuous Authentication** &gt; **Policies**, select the policy name to open its record, and then select **Deactivate** or **Activate**.


## View default policies and configurations

Select **View default policies** or **View default configurations** on the tool card to review defaults. Selecting a policy or configuration name opens its management page.

## Log Export Service version requirement

Default Log Export Service configurations require Log Export Service version 3.5.0 and later. On earlier versions, the **Activate** option isn't available and the tool card shows **Go to Log Export Service** instead.

**Parent Topic:**[ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-dashboard.md)

**Related topics**  


[Vault tools and metrics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-tools.md)

[ServiceNow Vault console dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/vault-dashboard.md)

