---
title: Developer Sandboxes release notes
description: The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 3
---

# Developer Sandboxes release notes

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.

## Developer Sandboxes highlights for the Australia release

-   Upgrading an instance recreates sandboxes and backs up any update sets.
-   A new plugin supports clone preservation when cloning an instance with sandboxes.

See Developer Sandboxes for more information.

## New in the Australia release

-   **New granular roles for administration**

    Several new granular roles enable developers to complete administrative and configuration tasks without requiring the full admin role.

-   **Support for separate indices for AI Search**

    AI Search \(AIS\) now maintains separate indices for each sandbox environment, ensuring development activities that rely on AIS are correctly supported.

    **Note:** The AIS integration with Developer Sandboxes is supported only on non-production environments.


## UI changes

-   **Clarified sandbox initialization status**

    An error status message now appears on the instance home page when there’s an initialization error when allocating a sandbox.

-   **Developer Sandboxes home page hidden when product is inactive**

    The Developer Sandboxes home page is unavailable when Developer Sandboxes is inactive on an instance.


## Changed in this release

-   **Upgrade enhancements**

    After an upgrade, Developer Sandboxes now recreates the sandboxes on an instance and automatically backs up update sets to the base instance.

-   **Queuing for successive sandbox creation**

    To improve performance, Developer Sandboxes has implemented queuing when multiple sandboxes are created in succession.

-   **SSO support for vanity URLs**

    Instances with vanity URLs can now support Single Sign-On \(SSO\).

-   **Schema change for shared tables isolates the table**

    To ensure configuration consistency, if you make a schema change, such as adding a column, to a shared table, the table now becomes an isolated table on the sandbox that initiated the schema change.

-   **New vibe coding documentation**

    Documentation is now available that introduces vibe coding, which is a natural language approach to application development in ServiceNow, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


## Deprecated features

Data generation profiles and templates will no longer available in Developer Sandboxes as of the Brazil release. When you upgrade, the following will happen:

-   All data generation metadata and non-metadata records are automatically deleted.
-   The data generation plugin is no longer discoverable.
-   All references to data generation will be removed from sandbox templates.
-   Sandbox initialization will operate independently of data generation logic.

**Note:** You can use the Now Assist Data Kit instead of data generation profiles.

## Activation information

Contact your ServiceNow account manager to install Developer Sandboxes.

## Plugin information

-   **New plugin**

    The following plugin is new in Australia:

    Dev Sandboxes CC \(com.glide.dsb.cc\): A new plugin is available for clone preservers, which preserve settings when you clone an instance.


## Related ServiceNow applications and features

-   **ServiceNow IDE**

    Create and develop scoped applications in source code in an integrated development environment \(IDE\) on the ServiceNow AI Platform to improve collaboration across development teams and accelerate application development.

-   **ServiceNow SDK**

    The ServiceNow SDK is used in the background of the ServiceNow IDE as the application packaging service that builds applications and provides the ServiceNow Fluent APIs for developing applications in source code. Scoped applications created or converted with the ServiceNow IDE or ServiceNow SDK can be developed with either application.

-   **ServiceNow Studio**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps with ease.

-   **Workflow Studio**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

