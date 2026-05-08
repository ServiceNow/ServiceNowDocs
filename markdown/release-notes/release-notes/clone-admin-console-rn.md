---
title: Clone Admin Console release notes
description: The ServiceNow Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
---

# Clone Admin Console release notes

The ServiceNow® Clone Admin Console application copies data and metadata from one ServiceNow instance to another ServiceNow instance to easily synchronize your instances. Clone Admin Console was enhanced and updated in the Australia release.

## Clone Admin Console highlights for the Australia release

-   Access all clone functions from the Clone Admin Console menu navigation item.
-   Submit additional clone requests to a target instance with an existing scheduled clone that is at least seven days apart.

See Instance Clone for more information.

## Changed in this release

-   **Updated clone menu navigation items**

    All clone-related functions are now available under the Clone Admin Console menu navigation item.

-   **Submit a new clone even if another clone is scheduled**

    Create an additional clone request even if there’s already a future clone for that target. This feature helps with the limitation where you can't submit another clone until all existing requests have been canceled.

-   **Clone summary**

    Help prevent clone conflicts with the Clone summary, which highlights clones that are scheduled in the next 30 days that involve the same target instance.

-   **Updated authentication model**

    Clone Admin Console now uses JWT certificate-based authentication instead of username and password authentication, improving security and simplifying cross-instance authentication.


## Deprecated Features

-   Clone requests via lists and forms \(legacy\) are no longer supported. The page redirects to the new request page after 30 seconds.
-   Legacy clones no longer appear in the Clone Admin Console dashboard.

## Activation information

Clone Admin Console is a ServiceNow AI Platform feature that is active by default.

**Parent Topic:**[ServiceNow AI Platform administration release notes](now-platform-admin-rn-landing.md)

