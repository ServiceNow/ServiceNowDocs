---
title: Developer Sandboxes release notes
description: The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
---

# Developer Sandboxes release notes

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Developer Sandboxes was enhanced and updated in the Australia release.

## Developer Sandboxes highlights for the Australia release

-   Upgrading an instance recreates sandboxes and backs up any update sets.
-   Cloning automatically recreates sandboxes on an instance.
-   A new plugin supports clone preservation when cloning an instance with sandboxes.

See [Developer Sandboxes](https://www.servicenow.com/docs/access?context=sandboxes-landing&version=australia&pubname=australia-application-development&ft:locale=en-US) for more information.

## New in the Australia release

-   **[New granular roles for administration](https://www.servicenow.com/docs/access?context=dsb-installed-with&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Several new granular roles enable developers to complete administrative and configuration tasks without requiring the full admin role.

-   **[Support for separate indices for AI Search](https://www.servicenow.com/docs/access?context=exploring-sandboxes&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    AI Search \(AIS\) now maintains separate indices for each sandbox environment, ensuring development activities that rely on AIS are correctly supported.

    **Note:** The AIS integration with Developer Sandboxes is supported only on non-production environments.


## UI changes

-   **[Clarified sandbox initialization status](https://www.servicenow.com/docs/access?context=allocating-sandboxes&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    An error status message now appears on the instance home page when there’s an initialization error when allocating a sandbox.

-   **[Developer Sandboxes home page hidden when product is inactive](https://www.servicenow.com/docs/access?context=dev-sbx-entitlements&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    The Developer Sandboxes home page is unavailable when Developer Sandboxes is inactive on an instance.


## Changed in this release

-   **[Upgrade enhancements](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    After an upgrade, Developer Sandboxes now recreates the sandboxes on an instance and automatically backs up update sets to the base instance.

-   **[Cloning enhancements](https://www.servicenow.com/docs/access?context=dev-sbx-clone-upgrade-info&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    After a clone, sandboxes on an instance are automatically re-created with the same name, but without the previous work.

-   **[Queuing for successive sandbox creation](https://www.servicenow.com/docs/access?context=allocating-sandboxes&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    To improve performance, Developer Sandboxes has implemented queuing when multiple sandboxes are created in succession.

-   **[SSO support for vanity URLs](https://www.servicenow.com/docs/access?context=dev-sbx-general-guidelines&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Instances with vanity URLs can now support Single Sign-On \(SSO\).

-   **[Schema change for shared tables isolates the table](https://www.servicenow.com/docs/access?context=dsb-installed-with&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    To ensure configuration consistency, if you make a schema change, such as adding a column, to a shared table, the table now becomes an isolated table on the sandbox that initiated the schema change.

-   **[New vibe coding documentation](https://www.servicenow.com/docs/access?context=vibe-coding-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Documentation is now available that introduces vibe coding, which is a natural language approach to application development in ServiceNow, including how to get started, when to use it, and how it fits within the broader suite of AI-powered development tools.


## Activation information

Contact your ServiceNow account manager to install Developer Sandboxes.

## Plugin information

-   **[New plugin](https://www.servicenow.com/docs/access?context=dev-sbx-installing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    The following plugin is new in Australia:

    Dev Sandboxes CC \(com.glide.dsb.cc\): A new plugin is available for clone preservers, which preserve settings when you clone an instance.


## Related ServiceNow applications and features

-   **[ServiceNow IDE](https://www.servicenow.com/docs/access?context=servicenow-ide-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    Create and develop scoped applications in source code in an integrated development environment \(IDE\) on the ServiceNow AI Platform to improve collaboration across development teams and accelerate application development.

-   **[ServiceNow SDK](https://www.servicenow.com/docs/access?context=servicenow-sdk-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    The ServiceNow SDK is used in the background of the ServiceNow IDE as the application packaging service that builds applications and provides the ServiceNow Fluent APIs for developing applications in source code. Scoped applications created or converted with the ServiceNow IDE or ServiceNow SDK can be developed with either application.

-   **[ServiceNow Studio](https://www.servicenow.com/docs/access?context=servicenow-studio-landing&version=australia&pubname=australia-application-development&ft:locale=en-US)**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps with ease.

-   **[Workflow Studio](https://www.servicenow.com/docs/access?context=workflow-studio&version=australia&pubname=australia-build-workflows&ft:locale=en-US)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience.


**Parent Topic:**[App development and low-code release notes](build-automate-rn-landing.md)

