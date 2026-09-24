---
title: Clone Admin Console release notes
description: The ServiceNow Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances.Clone Admin Console was enhanced and updated in the Brazil release.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/release-notes/clone-admin-console-rn-static.html
release: brazil
topic_type: topic
last_updated: "2026-09-10"
reading_time_minutes: 4
keywords: [Clone Admin Console, Instance Clone, OAuth, Multi-Instance View, Now Assist, authentication, Clone Admin Console, Instance Clone, OAuth, Multi-Instance View, Now Assist, authentication]
breadcrumb: [ServiceNow AI Platform administration release notes, Features and changes by product, Release notes for upgrading from Australia, Learn about the Brazil release, Brazil release notes]
---

# Clone Admin Console release notes

The ServiceNow® Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances.

## About Clone Admin Console

-   Copies data and metadata from a source instance to a target instance to keep sub-production environments synchronized with production.
-   Provides a single console to configure, request, and monitor clones across your environment.
-   Supports OAuth 2.0 authentication for clone targets, removing the need for local admin credentials on every clone request.
-   Consolidates clone activity across multiple linked instances through Multi-Instance View.
-   Offers AI-assisted answers to clone questions in the console through the Clone FAQ Agent, powered by Now Assist.

See [Instance Clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/system-clone-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Clone Admin Console is a ServiceNow AI Platform feature that is active by default. No additional plugin activation is required to use core clone functionality.

-   **Additional requirements**
    -   The `clone_admin` role is required to request, cancel, or schedule clones.
    -   OAuth-based clone target authentication requires Australia Patch 5 or later on both the source and target instances. The `oauth_admin` role is required on the target instance during initial OAuth setup only. See [OAuth 2.0 authentication for clone targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/clone-oauth-authentication.md).
    -   A Now Assist license is required to use the Clone FAQ Agent. If Now Assist is installed after the Clone Admin Console, reinstall the console from the Store to enable the skill.
    -   Both the source and target instances must be on Australia Patch 5 or later to use Multi-Instance View.

## Accessibility and localization

-   **Accessibility information**
    -   The Clone Admin Console user interface follows ServiceNow platform accessibility standards.
    -   Clone status indicators, tables, and forms in the Clone Admin Console are navigable using standard keyboard and screen reader support provided by the platform.
-   **Localization information**

    Clone Admin Console follows the language settings configured on your instance. Clone Admin Console labels, messages, and Help content reflect the language preferences set for each user.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/release-notes/now-platform-admin-rn-landing.md)

## Brazil Early Availability

Clone Admin Console was enhanced and updated in the Brazil release.

### What's new

-   **[OAuth 2.0 authentication for clone targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/clone-oauth-authentication.md)**

    Authenticate clone requests to target instances using OAuth 2.0 without requiring local admin credentials. One-time target instance registration enables automatic token generation and expiration for each clone request, improving security and simplifying cross-instance authentication.

    Both the source and target instances must be on Australia Patch 5 or a subsequent release to use OAuth target authentication.

-   **[Multi-Instance View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/clone-multi-instance-view.md)**

    View clone activity across connected instances from a single console. Opt in from **Configuration** &gt; **Multi-Instance View** to begin monitoring multiple instances simultaneously.

    Both the source and target instances must be on Australia Patch 2 or a subsequent release to use **Multi-Instance View**.

-   **Instance Overview**

    The Instance Overview tab now displays last-cloned timestamps for each instance, enabling you to quickly identify stale environments and prioritize update activities.

-   **Clone FAQ Agent \(via Now Assist\)**

    Get answers to clone questions directly in the console, powered by curated ServiceNow clone documentation. This AI-assisted capability streamlines the learning experience for new users. Requires a Now Assist license. If Now Assist is installed after the Clone Admin Console, reinstall the console from the Store to enable the skill.

-   **Help page**

    The static FAQ section on the Homepage has been replaced with a dedicated Help page. Links to curated clone help articles are now consolidated into the new dedicated Help page for a streamlined user experience and details about the Now Assist AI skill.

-   **Clone request estimated completion**

    The Clone Request page now displays an estimated completion time beneath the selected Date/Time. A relative time indicator \(for example, "in 2 hours" or "in 2 weeks"\) helps you plan activities accordingly.


### What's changed

-   **Updated clone menu navigation items**

    All clone-related functions are now available under the Clone Admin Console menu navigation item.

-   **[Configuration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/clone-configurations-tab.md)**

    All clone-related settings are now grouped under a single **Configuration** tab for improved organization and discoverability.

-   **Clone Home renamed to Clone Activity**

    The **Clone Home** menu item has been renamed to **Clone Activity** to be more descriptive of the page's purpose and improve navigation clarity.

-   **Submit a new clone even if another clone is scheduled**

    Create an additional clone request even if there's already a future clone for that target. This feature removes the previous limitation where any new clone requests were not allowed until all existing requests were canceled. You can now submit new clone requests if more than five days apart from existing ones.

-   **Clone summary**

    Help prevent clone conflicts with the **Clone summary**, which highlights clones that are scheduled in the next 30 days that involve the same target instance.

-   **Updated authentication model**

    Clone Admin Console now uses JWT certificate-based authentication instead of username and password authentication, improving security and simplifying cross-instance authentication. See [Register an instance for cloning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/configure-target-instance.md).

-   **Clone profile script updates**

    Fixed an issue where setting a script in the clone\_cleanup\_script table to active=false or active=true did not apply consistently across all clone profiles the script was listed on. Changes now propagate correctly.

    Both the source and target instances must be on Australia Patch 5 or subsequent release to use cleanup script status.

-   **Clone profile duplication**

    Fixed an issue where duplicating a clone profile pulled in all existing scripts, preservers, and exclusions from the original profile. Duplicating a profile now correctly creates a new profile containing only the intended scripts, preservers, and exclusions from the source.

-   **Static FAQ content removed**

    Static FAQ content has been removed from the landing page and consolidated into the new dedicated Help page for a streamlined user experience.

-   **Clone requests via lists and forms \(legacy\) deprecated**

    Clone requests via lists and forms \(legacy\) are no longer supported. The page redirects to the new request page after 30 seconds.


