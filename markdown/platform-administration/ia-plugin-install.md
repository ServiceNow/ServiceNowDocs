---
title: Individual plugin installation from Product Hub
description: Individual plugin installation enables you to discover, review, and install standalone plugins directly from Product Hub without requiring a bundled apps package. This capability supports flexible deployment scenarios, early adoption, and validation of plugins before committing to full product bundles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ia-plugin-install.html
release: australia
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 3
breadcrumb: [Administer, ServiceNow Otto for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Individual plugin installation from Product Hub

Individual plugin installation enables you to discover, review, and install standalone plugins directly from Product Hub without requiring a bundled apps package. This capability supports flexible deployment scenarios, early adoption, and validation of plugins before committing to full product bundles.

Product Hub traditionally expose product bundles, providing guided installations of complete product packages with mandatory and optional apps. Individual plugin installation extends this capability by allowing admins to install specific standalone plugins without committing to an entire bundle. This approach enables business units \(BUs\) such as ITAM to adopt plugins incrementally, validate functionality before broader deployment, and maintain granular control over their instance's capabilities.

Individual plugins are surfaced alongside bundled products in Product Hub. Each plugin displays its name, description, current status, and required dependencies. The installation process leverages the same guided framework used for bundled installs, including entitlement validation, dependency checking, installation progress tracking, and dynamic item count display. Individual plugin installation workflows mirror the product bundle installation experience, ensuring consistency across product bundle installation scenarios.

## Key benefits

Individual plugin installation provides the following benefits:

-   Flexible deployment: Admins can activate only the capabilities they need, avoiding unnecessary components and reducing instance bloat from unwanted functionality.
-   Early adoption: Business units can validate new plugins in controlled environments before deciding on broader deployment or full product adoption.
-   Incremental rollout: Organizations can phase plugin adoption over time, aligning deployments with business priorities and readiness schedules rather than bundled all-or-nothing approaches.
-   Faster time to value: Admins bypass the overhead of evaluating and installing entire product bundles when they only need specific capabilities.
-   Simplified licensing: Plugin-level licensing constraints are evaluated independently, allowing admins to proceed with available plugins and defer others pending license acquisition.
-   Clear dependency visibility: The install flow displays all required dependencies, helping admins understand what will be activated alongside their selected plugin.

## Use cases

Individual plugin installation is useful in the following scenarios:

-   Selective capability adoption: An organization needs a specific plugin's functionality but does not want the additional apps that would come with a full product bundle. Individual plugin installation lets them activate exactly what they need.
-   Pilot deployments: A business unit tests a plugin in a sandbox or development instance before deciding whether to roll it out to production. If validation is successful, they proceed with installation in production; if not, they can defer or abandon the plugin without affecting other deployments.
-   Phased rollout: A large enterprise rolls out multiple plugins over time according to organizational readiness. Using individual plugin installation, different teams can adopt plugins on their own schedule without waiting for bundled product releases.
-   Licensing optimization: An organization has licenses for some plugins but not others. They install available plugins immediately and defer others until additional licensing is procured, avoiding all-or-nothing delays.
-   Feature experimentation: IT teams evaluate whether a plugin's capabilities align with business requirements before committing to broader rollout, minimizing waste and maximizing ROI on technology investments.

## Considerations

Consider the following when using individual plugin installation:

-   Dependencies are mandatory: When a plugin has required dependencies, all of them must be installed as part of the transaction. You can't selectively skip dependencies even if you don't intend to use them. Dependencies are identified during installation planning and validated before execution begins.
-   Entitlements are authoritative: Plugin availability is controlled by active licensing and can't be overridden within Product Hub. If a plugin or dependency lacks appropriate licensing, installation is blocked until licensing is obtained.
-   Plugins are registered by business units: Not all plugins are automatically eligible for individual installation through Product Hub. Plugins must be explicitly registered in the Product Hub registry by their owning business unit. Contact your implementation team if a plugin you need is not visible in the hub.
-   Individual plugin installs don't include bundle customization: Individual plugin installation follows a streamlined path with pre-defined mandatory apps and dependencies. If you need fine-grained control over optional components, consider the bundled product installation flow instead.
-   Installation status reflects App Manager state: The plugin's installation status in Product Hub is synchronized with App Manager. If a plugin is set to inactive or is uninstalled outside of Product Hub \(for example, via direct App Manager operations\), the status in Product Hub updates to reflect the current state.

-   **[Install an individual plugin from Product Hub](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-install-individual-plugin.md)**  
Use Product Hub to discover, review, and install an individual standalone plugin without requiring a full product bundle installation.

**Parent Topic:**[Administer ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-administer.md)

