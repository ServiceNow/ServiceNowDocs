---
title: Developer Sandboxes release notes
description: The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Delegated developers can write and merge code and configuration changes without the risk of getting their changes overwritten on the instance mid-development. Developer Sandboxes is a new application in the Zurich release.The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Delegated developers can write and merge code and configuration changes without the risk of getting their changes overwritten on the instance mid-development. Developer Sandboxes is a new application in the Zurich release.The ServiceNow Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Delegated developers can write and merge code and configuration changes without the risk of getting their changes overwritten on the instance mid-development. Developer Sandboxes is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: topic
last_updated: "2026-07-20"
reading_time_minutes: 2
---

# Developer Sandboxes release notes

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Delegated developers can write and merge code and configuration changes without the risk of getting their changes overwritten on the instance mid-development. Developer Sandboxes is a new application in the Zurich release.

## About Developer Sandboxes

-   Support for Build Agent in sandboxes.
-   Enable your administrators and delegated developers to request, access, and manage the isolated development environments on top of the same underlying development instance.
-   Provide developer isolation and parallelism for customer development environments and instances.
-   View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when it was last accessed, and when the sandbox was allocated.

See  for more information.

## Activation and other requirements

**Important:**  is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

-   **Activation information**

    Contact your ServiceNow account manager to install Developer Sandboxes.


**Parent Topic:**[App development and low-code release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/release-notes/build-automate-rn-landing.md)

## June 2026

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Delegated developers can write and merge code and configuration changes without the risk of getting their changes overwritten on the instance mid-development. Developer Sandboxes is a new application in the Zurich release.

### What's changed

-   **Upgrade enhancements**

    Automatic backups for upgrades are now working correctly. This issue is related to PRB2017438.


## Zurich

The ServiceNow® Developer Sandboxes application enables your administrators and delegated developers to request, access, and manage the individual sandboxes on top of the same underlying development instance. Delegated developers can write and merge code and configuration changes without the risk of getting their changes overwritten on the instance mid-development. Developer Sandboxes is a new application in the Zurich release.

### What's new

-   ****

    View the total, available, and allocated sandboxes in your instance by using the Sandbox Management home dashboard. The dashboard also displays information about each sandbox, including the status, data utilization, owner, when the sandbox was last accessed, and when the sandbox was allocated.

-   ****

    Enable your delegated developers to reuse the data so that they can test their changes without manually inputting the data every time.

-   ****

    Enable your customers to generate the data for testing within the context of developer sandboxes, but also independently of sandboxes.

    **Note:** Developer Sandboxes can't copy all the instance data. Data generation profiles enable a statistical sampling of data from selected tables with curated mappings to populate the sandbox with the data needed for building an application.

-   ****

    Allocate the sandboxes that were created to your development teams.

-   ****

    Retire outdated sandboxes to make room for the new sandboxes in your instance.

-   **Automatically backed up update sets**

    If you install Developer Sandboxes on an instance after Zurich Patch 5, update sets are automatically backed up when the instance is upgraded.


### What's deprecated or removed

-   All data generation metadata and non-metadata records are automatically deleted.
-   The data generation plugin is no longer discoverable.
-   All references to data generation will be removed from sandbox templates.
-   Sandbox initialization will operate independently of data generation logic.

