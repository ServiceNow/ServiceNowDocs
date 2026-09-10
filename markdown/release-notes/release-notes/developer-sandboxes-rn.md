---
title: Developer Sandboxes release notes
description: The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: topic
last_updated: "2026-07-20"
reading_time_minutes: 3
---

# Developer Sandboxes release notes

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.

## About Developer Sandboxes

-   Support for Build Agent in sandboxes.
-   Upgrading an instance recreates sandboxes and backs up any update sets.
-   A new plugin supports clone preservation when cloning an instance with sandboxes.

See  for more information.

## Activation and other requirements

-   **Activation information**

    Contact your ServiceNow account manager to install Developer Sandboxes.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/build-automate-rn-landing.md)

## June 2026

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.

### What's changed

-   **Upgrade enhancements**

    Automatic backups for upgrades are now working correctly. This issue is related to PRB2017438.


## April 2026

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.

### What's changed

-   **Schema change for shared tables isolates the table**

    To ensure configuration consistency, if you make a schema change, such as adding a column, to a shared table, the table now becomes an isolated table on the sandbox that initiated the schema change.


## Australia Early Availability

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.

### What's changed

-   **Upgrade enhancements**

    After an upgrade, Developer Sandboxes now recreates the sandboxes on an instance and automatically backs up update sets to the base instance.

-   **Queuing for successive sandbox creation**

    To improve performance, Developer Sandboxes has implemented queuing when multiple sandboxes are created in succession.

-   **SSO support for vanity URLs**

    Instances with vanity URLs can now support Single Sign-On \(SSO\).

-   **New vibe coding documentation**

    Documentation is now available that introduces vibe coding, which is a natural language approach to application development in ServiceNow, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


## Australia

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.

### What's new

-   **New granular roles for administration**

    Several new granular roles enable developers to complete administrative and configuration tasks without requiring the full admin role.

-   **Support for separate indices for AI Search**

    AI Search \(AIS\) now maintains separate indices for each sandbox environment, ensuring development activities that rely on AIS are correctly supported.

    **Note:** The AIS integration with Developer Sandboxes is supported only on non-production environments.


### What's changed

-   **Clarified sandbox initialization status**

    An error status message now appears on the instance home page when there’s an initialization error when allocating a sandbox.

-   **Developer Sandboxes home page hidden when product is inactive**

    The Developer Sandboxes home page is unavailable when Developer Sandboxes is inactive on an instance.


### What's deprecated or removed

-   All data generation metadata and non-metadata records are automatically deleted.
-   The data generation plugin is no longer discoverable.
-   All references to data generation will be removed from sandbox templates.
-   Sandbox initialization will operate independently of data generation logic.

### Plugin information

-   **New plugins**

    The following plugin is new in Australia:

    Dev Sandboxes CC \(com.glide.dsb.cc\): A new plugin is available for clone preservers, which preserve settings when you clone an instance.


