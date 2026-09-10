---
title: Clone Admin Console release notes
description: The ServiceNow Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release. The ServiceNow Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release. The ServiceNow Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Clone Admin Console release notes

The ServiceNow® Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release.

## About Clone Admin Console

-   Access all clone functions from the Clone Admin Console menu navigation item.
-   Monitor clone activity across multiple connected instances from a single console view.
-   Get answers to clone questions directly in the console with AI-assisted Now Assist capability.
-   Plan clone activities with estimated completion time indicators.

See [Instance Clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md) for more information.

## Activation and other requirements

-   **Activation information**

    Clone Admin Console is a ServiceNow AI Platform feature that is active by default.


**Parent Topic:**[ServiceNow AI Platform administration release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/now-platform-admin-rn-landing.md)

## July 2026

The ServiceNow® Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release.

### What's changed

-   **[Updated authentication model](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/configure-target-instance.md)**

    Clone Admin Console now uses JWT certificate-based authentication instead of username and password authentication, improving security and simplifying cross-instance authentication.


## Australia

The ServiceNow® Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release.

### What's new

-   **[Instance Overview Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)**

    The Instance Overview page now displays last-cloned timestamps for each instance, enabling you to quickly identify stale environments and prioritize update activities.

-   **[Multi-Instance View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)**

    View clone activity across connected instances from a single console. Opt in from **Configuration** &gt; **Multi-Instance View** to begin monitoring multiple instances simultaneously.

    Both the source and target instances must be on Australia Patch 2 or a subsequent release to use **Multi-Instance View**.

-   **[Clone FAQ Agent \(via Now Assist\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)**

    Get answers to clone questions directly in the console, powered by curated ServiceNow clone documentation. This AI-assisted capability streamlines the learning experience for new users.

-   **Now Assist license requirement**

    Requires a Now Assist license. If Now Assist is installed after the Clone Admin Console, reinstall the console from the Store to enable the skill.

-   **[Help Page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)**

    The static FAQ section on the Homepage has been replaced with a dedicated Help page. Links to curated clone help articles are now consolidated into the new dedicated Help page for a streamlined user experience and details about the Now Assist AI skill.

-   **[Clone Request Estimated Completion](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)**

    The Clone Request page now displays an estimated completion time beneath the selected Date/Time. A relative time indicator \(for example, "in 2 hours" or "in 2 weeks"\) helps you plan activities accordingly.


-   **[OAuth 2.0 authentication for clone targets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/clone-oauth-authentication.md)**

    Authenticate clone requests to target instances using OAuth 2.0 without requiring local admin credentials.

    Both the source and target instances must be on Australia Patch 5 or a subsequent release to use OAuth target authentication.


### What's changed

-   **[Updated clone menu navigation items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)**

    All clone-related functions are now available under the Clone Admin Console menu navigation item.

-   **[Submit a new clone even if another clone is scheduled](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md)**

    Create an additional clone request even if there’s already a future clone for that target. This feature removes the previous limitation where any new clone requests were not allowed until all existing requests were canceled. You can now submit new clone requests if more than five days apart from existing ones.

-   **[Clone summary](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_StartAClone.md)**

    Help prevent clone conflicts with the **Clone summary**, which highlights clones that are scheduled in the next 30 days that involve the same target instance.

-   **[Configuration tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)**

    All clone-related settings are now grouped under a single **Configuration** tab for improved organization and discoverability.

-   **[Clone Home Renamed to Clone Activity](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/system-clone-landing.md)**

    The **Clone Home** menu item has been renamed to **Clone Activity** to be more descriptive of the page's purpose and improve navigation clarity.

-   **Clone profile script updates**

    Fixed an issue where setting a script in the clone\_cleanup\_script table to active=false or active=true did not apply consistently across all clone profiles the script was listed on. Changes now propagate correctly.

    Both the source and target instances must be on Australia Patch 5 or a subsequent release to use cleanup script status.


### What's deprecated or removed

-   **Static FAQ Content**

    Static FAQ content has been removed from the landing page and consolidated into the new dedicated Help page for a streamlined user experience.

-   **Clone requests via lists and forms \(legacy\)**

    Clone requests via lists and forms \(legacy\) are no longer supported. The page redirects to the new request page after 30 seconds.


