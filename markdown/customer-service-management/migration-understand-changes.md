---
title: Understand what changes when you move to CSM Configurable Workspace
description: CSM Configurable Workspace is built on a different technical foundation than CSM Agent Workspace. Understanding the key differences helps you plan your migration and set realistic expectations before you start.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-understand-changes.html
release: zurich
topic_type: concept
last_updated: "2026-10-25"
reading_time_minutes: 3
breadcrumb: [Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Understand what changes when you move to CSM Configurable Workspace

CSM Configurable Workspace is built on a different technical foundation than CSM Agent Workspace. Understanding the key differences helps you plan your migration and set realistic expectations before you start.

CSM Configurable Workspace uses the Next Experience UI and the full UI Builder. Some configurations from CSM Agent Workspace transfer directly, some need to be adapted, and some must be rebuilt.

**Note:** CSM Agent Workspace is considered legacy and is no longer available for new activation, beginning with the Washington DC release. No new features or updates are planned for CSM Agent Workspace. Migrate to CSM Configurable Workspace as soon as possible.

## What changes for your agents

In CSM Agent Workspace, agents work in a separate browser window that can't share branding or navigation with the rest of the platform. They have limited ability to customize their view and can't access AI features such as case summaries or response recommendations.

After migration, agents work in a single interface within the Next Experience UI. They get a tabbed, multi-record view with inline Now Assist features, and you can tailor the workspace to each agent group without engineering work.

## Key differences between the workspaces

|Capability|CSM Agent Workspace|CSM Configurable Workspace|
|----------|-------------------|--------------------------|
|UI components and page variants|Uses a limited version of UI Builder. You can't create non-landing pages or page variants, or edit component properties.|Uses the full UI Builder to tailor the workspace for multiple agent groups. Provides highly customizable components for page layouts, content, data visualization, messaging, and navigation.|
|Agent experience|UI actions and modals are the primary interaction methods.|Supports contextual side panels, tabs, and additional interactive functionality.|
|Next Experience UI and branding|Can't inherit branding or theming from the Next Experience UI. Operates in a separate browser window.|Integrates with the Next Experience UI and theming. Works with Unified Navigation, so no separate browser window is required.|
|Compatibility and support|No further enhancements. App Engine Studio apps can't integrate with CSM Agent Workspace.|Receives quarterly store app updates. Included as a core CSM product feature with all CSM SKUs. App Engine Studio apps generate a configurable workspace automatically.|

For a full feature overview, see [CSM Configurable Workspace features](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-workspace-feature-overview.md).

## Compare features between the workspaces

Several capabilities that didn't exist in CSM Agent Workspace become available after migration, including global search, AI-based recommended actions, message indicators on chat tabs, and Now Assist features. Knowing what's new helps you decide which capabilities to enable for your agents and where to focus training. To see the action required for each configuration, see [Plan the CSM Agent Workspace migration](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-plan.md).

|Page or module|Feature|CSM Agent Workspace|CSM Configurable Workspace|
|--------------|-------|-------------------|--------------------------|
|Workspace landing page|List of assigned cases and tasks, with metrics|Yes|Yes|
|Workspace landing page|Configurable page layout and notifications|Limited|Yes|
|Workspace landing page|Current user and organization performance indicators|Limited|Yes|
|Chat|Message indicator on chat tabs|No|Yes|
|Case page|Global search|No|Yes|
|Case page|Contextual search with Agent Assist|Limited|AI Search|
|Case page|AI-based recommended actions|No|Yes|
|Case page|Templates|Yes|Yes|
|Case page|Response templates|No|Yes|
|Case page|Base system UX screen collection configuration for the contextual side panel, including the consumer Lookup and Verify option|Limited|Yes|
|Case page and front-line case page|Now Assist capabilities such as case summary, Customer Central chat summary, voice conversation summary, chat and email response recommendations, and case triage|No|Yes|
|OpenFrame window|Integration with third-party telephony systems so that agents can place customer calls|Yes|Yes|

**Note:** Limited means that the feature exists in CSM Agent Workspace with reduced capability. Capabilities that are new in CSM Configurable Workspace and aren't part of the core migration steps are covered in [Go live with CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/migration-go-live.md).

