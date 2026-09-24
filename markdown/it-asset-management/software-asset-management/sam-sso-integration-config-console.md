---
title: SSO integration in Configuration Console
description: The SSO \(Single Sign-On\) module under the Software integrations module in the Configuration Console displays a tile for each supported SSO provider. Use these tiles to create SSO integration profiles that capture managed applications and their usage data for software asset tracking.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/sam-sso-integration-config-console.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 2
breadcrumb: [Configure SAM using Configuration Console, Configuration Console for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# SSO integration in Configuration Console

The SSO \(Single Sign-On\) module under the Software integrations module in the Configuration Console displays a tile for each supported SSO provider. Use these tiles to create SSO integration profiles that capture managed applications and their usage data for software asset tracking.

Access to the SSO module requires the sam\_admin and sn\_ia\_config.ia\_user roles. The module enables SAM admins to configure SSO provider integrations, review integration status, and track software usage data for connected SSO applications.

The following SSO providers are supported:

-   **Microsoft Entra ID**

    Pulls SSO applications, users, groups, and group memberships from your Microsoft Entra ID tenant through the Microsoft Entra ID Spoke.

    **Note:** The tile appears when the [Software Asset Management - SaaS License Management](https://store.servicenow.com/store/app/49d8632e1be06a50a85b16db234bcbee) and [Microsoft Entra ID Spoke](https://store.servicenow.com/store/app/8e29af6e1be06a50a85b16db234bcb8a) store applications are installed.

-   **Okta**

    Pulls SSO applications, users, and groups from your Okta organization through the Okta Spoke.

    **Note:** The tile appears when the [Software Asset Management - SaaS License Management](https://store.servicenow.com/store/app/49d8632e1be06a50a85b16db234bcbee) and [Okta Spoke](https://store.servicenow.com/store/app/05e9a3a21b246a50a85b16db234bcb25) store applications are installed.


## Tile actions

Each SSO tile displays one of the following actions based on the integration status:

-   **Get started**

    Opens the Guided Setup for a tile with no existing integration profile. Use this action to configure the SSO provider for the first time.

-   **Resume**

    Continues an in-progress guided setup that was started but not completed.

-   **Review**

    Opens the Software Asset Workspace list view of integration profiles created for that provider.


## Ways to create an SSO integration profile

The Configuration Console provides two entry points for creating an SSO integration profile:

-   The **Get started** action on a provider tile, which launches the guided setup for that provider.
-   The **New integration** button, followed by selection of a provider from the **Confirm integration type** drop-down list.

Both entry points open the **Create New SSO Integration Profile** form in the Software Asset Workspace. Enter the details required for the selected provider and submit the form to create the profile. The **Review** action on the tile then opens the list view of all profiles created for that provider, along with their current status.

**Parent Topic:**[Configure Software Asset Management using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-sam-from-config-console.md)

**Related topics**  


[Integrate with SSO providers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/saas-sso-integration.md)

[Integrating with Microsoft Entra ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/integrate-with-azure-ad.md)

[Integrating with Okta](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/integrate-okta.md)

[Integrate with SaaS applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/create-integration-profile.md)

