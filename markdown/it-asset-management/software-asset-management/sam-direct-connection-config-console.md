---
title: Direct connection integration in Configuration Console
description: The Direct connection module under the Software integrations module in the Configuration Console displays tiles for supported SaaS providers. Use these tiles to create integration profiles that connect directly to SaaS portals and pull in user subscription, activity, and usage data for license management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/sam-direct-connection-config-console.html
release: brazil
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure SAM using Configuration Console, Configuration Console for Software Asset Management, Software Asset Management installation methods, Configuring Software Asset Management, Software Asset Management, IT Asset Management, Asset Management]
---

# Direct connection integration in Configuration Console

The Direct connection module under the Software integrations module in the Configuration Console displays tiles for supported SaaS providers. Use these tiles to create integration profiles that connect directly to SaaS portals and pull in user subscription, activity, and usage data for license management.

Access to the Direct connection module requires the sam\_admin role. The module enables SAM admins to configure SaaS provider integrations, review integration status, and manage subscription and usage data for connected applications.

**Note:** When the [Software Asset Management - SaaS License Management](https://store.servicenow.com/store/app/49d8632e1be06a50a85b16db234bcbee) store application is installed, a default set of tiles such as Dropbox and DocuSign appears in the Direct connection module. Additional tiles appear based on the dependent store applications installed on your instance.

## Tile actions

Each direct connection tile displays one of the following actions based on the integration status:

-   **Get started**

    Opens the guided setup for a tile with no existing integration profile. Use this action to configure the SaaS provider for the first time.

-   **Resume**

    Continues an in-progress guided setup that was started earlier but not completed.

-   **Review**

    Opens the Software Asset Workspace list view of integration profiles created for that provider. The tile shows the count of draft or published profiles above the button.


## Ways to create a direct connection integration profile

The Configuration Console provides two entry points for creating a direct connection integration profile:

-   The **Get started** action on a provider tile, which launches the guided setup for that provider.
-   The **New integration** button, followed by selection of a provider from the **Confirm integration type** drop-down list.

Both entry points launch the Guided Setup for the selected provider, which covers prerequisites, SaaS product setup, and success goal creation. After the profile is created, the **Review** action on the tile opens the list view of all profiles created for that provider, along with their current status.

**Parent Topic:**[Configure Software Asset Management using the Configuration Console](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/software-asset-management/configure-sam-from-config-console.md)

**Related topics**  


[Integrate with SaaS applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/create-integration-profile.md)

[SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/it-asset-management/saas-license-management/sam-subscription-management.md)

