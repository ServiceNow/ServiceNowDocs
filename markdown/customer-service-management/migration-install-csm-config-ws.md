---
title: Install CSM Configurable Workspace
description: Before you migrate, install the Customer Service plugin \(com.sn\_customerservice\) on your instance. Installing this plugin gives you access to CSM Configurable Workspace.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/migration-install-csm-config-ws.html
release: zurich
topic_type: task
last_updated: "2026-10-25"
reading_time_minutes: 2
breadcrumb: [Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Install CSM Configurable Workspace

Before you migrate, install the Customer Service plugin \(com.sn\_customerservice\) on your instance. Installing this plugin gives you access to CSM Configurable Workspace.

## Before you begin

Role required: admin

-   Confirm that valid CSM licenses and user roles are in place.
-   Set up your foundational data and access management. For more information, see [Set up your environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/set-up-your-environment.md).
-   Enable your communication channels. For more information, see [Enable communication channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/enable-comm-channels.md).
-   Confirm that your instance is on the Washington DC release or later.
-   If cases should be assigned to agents or groups automatically, configure Advanced Work Assignment \(AWA\) before agents start working in CSM Configurable Workspace. For more information, see [AWA for CSM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/awa-csm-overview.md).
-   If domain separation and delegated admin are enabled, make sure that the administrative user is in the global domain during installation. Otherwise, the following error appears: `Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>`.
-   Recommended: Familiarize yourself with [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder-overview.md).

## About this task

You don't need to deactivate CSM Agent Workspace before you install CSM Configurable Workspace. Both workspaces can coexist on the same instance, so you can pilot the new workspace with a smaller agent group before switching everyone over.

## Procedure

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.

2.  Search for `com.sn_customerservice`.

    You can search for the plugin by its name or ID. If you can't find the plugin, you might have to request it from ServiceNow.

3.  Select **Install**.

    The following plugins are installed automatically:

    -   CSM and FSM Configurable Workspace Foundation \(com.snc.uib.cwf\_workspace\)
    -   CSM Configurable Workspace \(com.snc.uib.csm\_agent\_workspace\)
    -   CSM Configurable Workspace Lookup and Verify \(com.snc.uib.lookup\_verify\)
    -   CSM Configurable Workspace Special Handling Notes \(com.snc.uib.special\_handling\_notes\)
    **Note:** Additional plugins are required for phone integration.

    A message appears when the installation is complete.

4.  Open **CSM/FSM Configurable Workspace** from the **Workspaces** menu or the **All** menu.

    You can also navigate directly to `https://<instance>/now/cwf/agent`.


## What to do next

If you're setting up CSM Configurable Workspace for the first time without an existing CSM Agent Workspace deployment, use the guided setup instead. For more information, see [Set up CSM Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-config-workspace-set-up.md).

