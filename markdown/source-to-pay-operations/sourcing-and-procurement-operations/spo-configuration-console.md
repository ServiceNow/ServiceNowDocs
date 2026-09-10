---
title: Sourcing and Procurement Operations Configuration Console
description: The SPO Configuration Console guides administrators through configuring SPO in a structured, sequenced set of steps.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/sourcing-and-procurement-operations/spo-configuration-console.html
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-08-23"
reading_time_minutes: 5
keywords: [configuration console, SPO setup, procurement configuration, configuration wizard]
breadcrumb: [Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing and Procurement Operations Configuration Console

The SPO Configuration Console guides administrators through configuring SPO in a structured, sequenced set of steps.

Selecting **Configure** on the SPO Product Hub opens the SPO Configuration Console. The console presents configuration items in a fixed module and sub-module hierarchy in the left navigation pane. Administrators see the same structure and sequence every time they configure SPO.

The console includes two main modules:

-   **Platform** — Covers platform-wide setup including branding, localization, identity management integrations, and email configuration. Also includes operational data, groups and roles assignment, assets, knowledge management, AI skills, CMDB, AI Search, and security settings.
-   **Procurement Case Management** — Covers Employee Experience, Case Types, Assignment &amp; Routing, Playbooks, Notifications, Platform, Workspace, Properties, and Otto Skills.

\[Omitted image "spo-config-console.png"\] Alt text: Configure Sourcing and Procurement Operations Configuration Console showing configuration summary and setup status.

## Step indicators

Each configuration item in the console navigation panel carries indicators that orient administrators before they open it:

-   A **Suggested** label and icon for recommended steps, or an optional indicator for steps not required for go-live.
-   A lock icon and prerequisite list when a dependency step has not yet been marked **Configured**.
-   **New** or **Updated** labels for steps that are new or modified in the current product version.

Each module requires the **sn\_spend\_psd.admin** role to view or configure its steps.

## Setup status

The **Configuration Summary** page, the default landing page for the console, shows a **Setup status** section with the overall percentage of configuration items completed across the instance. Below the overall percentage, a separate progress gauge for each module shows how many of that module's configuration items are marked **Configured** out of the module's total. Selecting **Get Started** on a module with no completed items, or **Continue** on a module already in progress, opens that module's first available configuration item.

## Configuration activity

A **Configuration activity** section on the **Configuration Summary** page shows how configuration changes are captured. Configuration changes are recorded automatically into batched update sets, without requiring administrators to manage update sets manually.

This section provides two tabs:

-   **Configured items** — A searchable, sortable list of individual configuration changes not yet included in a completed batch. The list shows the configuration item, the module section it belongs to, who configured it, and when it was last updated. A **Go to active batch** link opens the update set currently collecting these changes.
-   **Completed batches** — The update sets already packaged from prior configuration activity.

For the procedure to package and download these update sets, see [Configure Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-spo-apps.md).

## Tracking progress on a configuration item

Administrators select **Mark as Configured** on a step to record it as complete. The status is reflected in the console navigation and in the step header, and rolls up into that module's progress gauge in **Setup status**. Administrators can return to a previously configured step and re-configure it without losing the earlier configuration.

## Learning resources

Documentation links, video guides, and community articles relevant to a configuration item are accessible inline within that step, without navigating away from the console. Each step also indicates whether ServiceNow Otto agent assistance is available for that item or whether it is a manual-only configuration step. A **How this works** link on the **Configuration Summary** page explains the console at a high level.

For the procedure to open the console and an overview of what you can do from it, see [Configure Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configure-spo-apps.md). For the configuration areas available under Procurement Case Management, see [Configuring case management in Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configuring-case-management-spo.md).

**Parent Topic:**[Configuring Sourcing and Procurement Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/sourcing-and-procurement-operations/configuring-spo.md)

**Related topics**  


[Sourcing and Procurement Operations product tile]()

[Sourcing and Procurement Operations Product Hub]()

[Install Sourcing and Procurement Operations]()

[Configure Sourcing and Procurement Operations]()

[Setting up primary data for ShoppingHub]()

[Configure punchout for third-party site purchases]()

[Configuring work prioritization]()

[Add a button in Shopping Hub]()

[Add a footer link in Shopping Hub]()

[Customize your top suppliers on Shopping Hub]()

[Configure conditions for merging purchase requisitions]()

[Service portal configuration for ShoppingHub]()

[Install ShoppingHub Mobile]()

[Advanced Work Assignment for Source-to-Pay Operations]()

[Install Universal Request for Sourcing and Procurement Operations]()

