---
title: Entitlement validation rules reference
description: Technical reference documenting entitlement validation rules, error states, and validation logic for jumbo apps and App Manager integration in product bundle installation workflows.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-administration/ia-entitlement-validation-rules.html
release: australia
topic_type: reference
last_updated: "2026-08-27"
reading_time_minutes: 2
breadcrumb: [Jumbo apps and entitlement validation, Administer, ServiceNow Otto for Setup, Get started, Administer the ServiceNow AI Platform]
---

# Entitlement validation rules reference

Technical reference documenting entitlement validation rules, error states, and validation logic for jumbo apps and App Manager integration in product bundle installation workflows.

## Validation phases

Entitlement validation occurs in three distinct phases during the apps installation workflow:

|Phase|When it occurs|What is validated|Result if validation fails|
|-----|--------------|-----------------|--------------------------|
|App selection|After the admin starts the installation workflow|For jumbo apps, Product Hub redirects the admin to App Manager. App Manager determines which apps are mandatory or optional and displays the selection experience|The selection experience remains available and displays information about missing dependencies when applicable.|
|Install submission|After the admin submits the install request|App Manager performs the required installation checks before proceeding|Installation is blocked and App Manager displays an error or dependency message|

## Mandatory app validation rules

For jumbo apps, App Manager determines which apps are mandatory and which are optional.

-   Are determined by App Manager
-   Can't be deselected
-   Remain visible in the selection experience even when required dependencies or entitlements are unavailable
-   Can prevent installation from completing if App Manager detects missing dependencies or other validation issues

## Optional app validation rules

For jumbo apps, App Manager determines which apps are optional.

-   Can be selected or cleared during the installation process
-   Are presented by App Manager based on the product configuration and instance state
-   Don't affect the selection state of mandatory apps.

## Error states and messaging

|Error state|When it occurs|User action required|
|-----------|--------------|--------------------|
|Missing dependency|A required dependency is unavailable during installation|Review the message provided by App Manager and resolve the dependency before retrying|
|Install validation failed|App Manager can't complete the install request|Review the error details and retry after addressing the reported issue|

## App Manager integration

-   Product Hub redirects jumbo app installations to App Manager
-   App Manager determines which apps are mandatory and optional
-   App Manager displays the app selection experience and any dependency-related messaging
-   App Manager performs validation checks before installation
-   If required dependencies are unavailable, App Manager can block the installation and provide guidance to the administrator.

## Implementation notes

-   Jumbo app identification: Product Hub identifies jumbo apps and redirects administrators to App Manager for installation. App Manager determines which apps are mandatory or optional based on its configuration and business logic.
-   Jumbo app installation workflow: For jumbo app installations, Product Hub redirects administrators to App Manager. App Manager provides the installation experience, including app selection, dependency messaging, and installation validation.
-   Fallback behavior: If App Manager can't provide the installation experience or validation results, the administrator receives an error message and installation can't continue until the issue is resolved.

**Parent Topic:**[Jumbo apps and entitlement validation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/ia-jumbo-apps-valid.md)

