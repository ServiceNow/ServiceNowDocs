---
title: Developer Sandboxes release notes
description: The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Delegated developers can write and merge code and configuration changes without the risk of getting their changes overwritten on the instance mid-development. Developer Sandboxes is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-12-08"
reading_time_minutes: 3
---

# Developer Sandboxes release notes

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Delegated developers can write and merge code and configuration changes without the risk of getting their changes overwritten on the instance mid-development. Developer Sandboxes is a new application in the Zurich release.

## Developer Sandboxes highlights for the Zurich release

-   Enable your administrators and delegated developers to request, access, and manage the isolated development environments on top of the same underlying development instance.
-   Provide developer isolation and parallelism for customer development environments and instances.
-   View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when it was last accessed, and when the sandbox was allocated.

See [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/sandboxes-landing.md) for more information.

**Important:** [Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/sandboxes-landing.md) is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## Developer Sandboxes features

-   **[Exploring Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/exploring-sandboxes.md)**

    View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when the sandbox was last accessed, and when the sandbox was allocated.

-   **[Using sandbox templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/create-sandbox-template.md)**

    Enable your delegated developers to reuse the data so that they can test their changes without manually inputting the data every time.

-   **[Create a Data Generation Profile](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/create-data-generation-profile.md)**

    Enable your customers to generate the data for testing within the context of developer sandboxes, but also independently of sandboxes.

    **Note:** Developer Sandboxes can't copy all the instance data. Data generation profiles enable a statistical sampling of data from selected tables with curated mappings to populate the sandbox with the data needed for building an application.

-   **[Allocate a sandbox](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/allocating-sandboxes.md)**

    Allocate the sandboxes that were created to your development teams.

-   **[Retire Developer Sandboxes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/retire-sandboxes.md)**

    Retire outdated sandboxes to make room for the new sandboxes in your instance.

-   **[Automatically backed up update sets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/dev-sbx-clone-upgrade-info.md)**

    If you install Developer Sandboxes on an instance after Zurich Patch 5, update sets are automatically backed up when the instance is upgraded.


## Changed in this release

-   **[Upgrade enhancements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/dev-sbx-clone-upgrade-info.md)**

    Automatic backups for upgrades are now working correctly. This issue is related to PRB2017438.


## Deprecated features

Data generation profiles and templates will no longer available in Developer Sandboxes as of the Brazil release. When you upgrade, the following will happen:

-   All data generation metadata and non-metadata records are automatically deleted.
-   The data generation plugin is no longer discoverable.
-   All references to data generation will be removed from sandbox templates.
-   Sandbox initialization will operate independently of data generation logic.

**Note:** You can use the Now Assist Data Kit instead of data generation profiles.

## Activation information

Contact your ServiceNow account manager to install Developer Sandboxes.

## Related ServiceNow applications and features

-   **[ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-ide-landing.md)**

    Create and develop scoped applications in source code in an integrated development environment \(IDE\) on the ServiceNow AI Platform to improve collaboration across development teams and accelerate application development.

-   **[ServiceNow SDK](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-sdk-landing.md)**

    The ServiceNow SDK is used in the background of the ServiceNow IDE as the application packaging service that builds applications and provides the ServiceNow Fluent APIs for developing applications in source code. Scoped applications created or converted with the ServiceNow IDE or ServiceNow SDK can be developed with either application.

-   **[ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/servicenow-studio-landing.md)**

    ServiceNow Studio provides a unified experience for all ServiceNow development activities, enabling admins and developers to extend base system solutions and create custom apps with ease.

-   **[Workflow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/build-workflows/workflow-studio.md)**

    Integrate workflow authoring, configuring, and monitoring into a single-page experience.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

