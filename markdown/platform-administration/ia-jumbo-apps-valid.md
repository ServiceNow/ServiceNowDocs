---
title: Jumbo apps and entitlement validation
description: Jumbo apps are large application bundles that support mandatory and optional app selection during installation. Entitlement validation confirms that admins have appropriate licensing for mandatory apps before installation proceeds, while optional apps display licensing status inline to inform installation decisions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ia-jumbo-apps-valid.html
release: australia
topic_type: concept
last_updated: "2026-08-27"
reading_time_minutes: 2
breadcrumb: [Administer, ServiceNow Otto for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Jumbo apps and entitlement validation

Jumbo apps are large application bundles that support mandatory and optional app selection during installation. Entitlement validation confirms that admins have appropriate licensing for mandatory apps before installation proceeds, while optional apps display licensing status inline to inform installation decisions.

Jumbo apps are large product bundles that bundle multiple applications together. Unlike standard apps or smaller product packages, jumbo apps support granular control over which components are installed by offering mandatory and optional app selections. Product Hub workflow leverages entitlement validation to confirm licensing requirements are met before allowing installations to proceed.

Entitlement validation operates at two levels: mandatory app validation and optional app validation. This layered approach prevents invalid installations caused by missing licenses while giving you the flexibility to defer optional components when licenses aren't available.

## Jumbo apps vs standard products

Jumbo apps follow a different installation workflow than standard products:

-   Standard products: Use the app selection modal within Product Hub, where admins select mandatory and optional apps directly.
-   Jumbo apps: Redirect admins to App Manager, where they configure version, choose optional features, and complete installation.

**Note:** For jumbo apps, when an admin selects Install from Product Hub, they are navigated to App Manager to complete the installation experience.

## Mandatory vs optional app designation

Business Units \(BUs\) register jumbo apps by populating specific fields on the Product Hub resource table:

-   Mandatory apps: Identified through the product resource configuration. These apps are essential for core functionality and can't be deselected by admins.

    **Note:** Licensing for mandatory apps is a hard requirement — installations can't proceed without valid entitlements.

-   Optional apps: Also defined in product resource configuration. These apps add supplementary capabilities and can be selected or deselected by admins during installation. Licensing for optional apps is informational — admins can defer installation if licenses are unavailable.
-   Jumbo app identification: The system distinguishes jumbo apps from regular apps through a product type flag or resource classification. This classification enables the mandatory/optional app selection modal and triggers enhanced entitlement validation workflows.

## Entitlement validation rules

Entitlement validation follows these rules:

-   Mandatory apps require active licensing: Every mandatory app in a jumbo bundle must have a valid, active entitlement. Expired, inactive, or missing licenses block installation and prevent the modal from displaying.
-   Entitlement checks validate against mandatory apps only before modal display: Pre-modal validation only checks mandatory apps. Optional app licensing is evaluated after the modal displays, allowing admins to see the full picture before deciding which components to install.
-   Optional app licensing is non-blocking: If an optional app lacks valid entitlements, it displays as disabled within the modal with an inline message. Admins can proceed with installation of available apps.
-   App Manager is the source of truth: All entitlement queries delegate to App Manager APIs. Product Hub doesn't cache or override App Manager licensing rules. If App Manager reports an app as unlicensed, it is treated as unlicensed regardless of other factors.
-   Installation fails if App Manager validation fails: Even if pre-modal and modal-level validation passes, if App Manager rejects the install request during submission \(for example, due to a changed licensing state or validation rule\), the installation is blocked with an error message.

-   **[Entitlement validation rules reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-entitlement-validation-rules.md)**  
Technical reference documenting entitlement validation rules, error states, and validation logic for jumbo apps and App Manager integration in product bundle installation workflows.

**Parent Topic:**[Administer ServiceNow Otto for Setup](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-administer.md)

