---
title: Mandatory and optional app selection modal
description: The app selection modal enables platform admins to view, select, and install product bundles with clear separation of mandatory and optional apps. The modal validates licensing, prevents modification of required apps, and integrates with App Manager APIs to verify transparent and guided installations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ia-mandatory-optional-select-modal.html
release: australia
topic_type: concept
last_updated: "2026-08-26"
reading_time_minutes: 3
breadcrumb: [Administer, ServiceNow Otto for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Mandatory and optional app selection modal

The app selection modal enables platform admins to view, select, and install product bundles with clear separation of mandatory and optional apps. The modal validates licensing, prevents modification of required apps, and integrates with App Manager APIs to verify transparent and guided installations.

When installing product bundles, platform admins need visibility into what will be installed and control over optional components. The app selection modal addresses this need by presenting a guided experience that separates mandatory apps from optional apps, validates licensing constraints, and enables informed selection decisions.

The modal integrates directly with App Manager APIs, ensuring that all app metadata, availability, and licensing rules remain current and authoritative. This approach eliminates manual app management and reduces the risk of invalid installations caused by missing required apps or licensing conflicts.

## Key benefits

The app selection modal provides the following benefits:

-   Transparent installation visibility: Admins see exactly which apps are mandatory, which are optional, and why certain apps may be unavailable due to licensing constraints.
-   Installation safety: Mandatory apps are pre-selected and locked, preventing accidental deselection of required components and eliminating installation failures caused by missing dependencies.
-   User control over optional components: Admins can customize installations by selecting or deselecting optional apps that match their organizational needs, reducing bloat and unnecessary features.
-   Clear licensing guidance: The modal displays messaging for unlicensed optional apps, enabling admins to make purchasing decisions or defer component installation until licenses are available.
-   Dynamic item count: The modal displays a real-time count of selected items that updates as admins select or deselect optional apps, providing clear visibility into the total installation scope.
-   Reduced installation errors: App Manager API integration ensures that app metadata, validation rules, and install requests align with current system state, preventing silent failures.

## Use cases

The app selection modal is useful in the following scenarios:

-   Standard product bundle installation: A platform admin installing a new product bundle wants to understand the base components \(mandatory\) before committing to optional add-ons. The modal provides clear visibility, enabling an informed decision about which optional apps to include in the initial installation.
-   Licensing-constrained installations: An organization has licenses for some but not all components in a bundle. The admin uses the modal to identify which optional apps require additional purchasing, defer installation of those apps, and proceed with available components.
-   Multi-team deployments: A large enterprise deploys the same product bundle across multiple business units with varying requirements. The modal allows each unit's administrator to customize the installation by selecting region-specific or team-specific optional apps without affecting the base functionality.
-   Phased adoption: An organization plans to roll out additional functionality over time. The admin installs the mandatory core apps immediately and deselects optional apps, deferring their installation to a later phase when users are ready to adopt them.

As of Brazil release, the mandatory and optional app selection capability is available for Business Units \(BUs\) to configure.

## Considerations

Consider the following when using the app selection modal:

-   Mandatory apps are non-negotiable: Apps marked as mandatory by App Manager can't be deselected. These represent core dependencies required for the product to function correctly. If licensing or dependency issues prevent a mandatory app from being available, the entire installation is blocked with a clear error message.
-   Licensing rules are authoritative: App availability and licensing constraints are controlled by App Manager and can't be overridden within the modal. If an app is marked as unlicensed or unavailable, it can't be selected regardless of admin preference.
-   Selection state is not saved between sessions: Optional app selections apply only to the current installation attempt. If an admin closes the modal without completing the install, their selections aren't retained for future sessions.
-   App dependencies are opaque to the modal: The modal presents which apps are mandatory versus optional but does not display dependency graphs or explain why specific apps are required. Admins who need to understand app relationships should consult App Manager documentation or contact their implementation team.
-   Item count updates dynamically: As admins select and deselect optional apps, the install button updates to show the current count of selected items. This count includes mandatory apps plus selected optional apps.
-   Install button availability: The install button is disabled if zero apps are selected for installation \(that is, if no mandatory apps are available and no optional apps are selected\). This prevents silent failures caused by empty install requests.

-   **[Select apps during product installation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-select-app-prod-install.md)**  
Use the app selection modal to review mandatory and optional apps, customize your installation by selecting optional components, and complete the product installation through product hub installation flow.

**Parent Topic:**[Administer ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-administer.md)

