---
title: Playbook pages
description: Use playbook pages in CSM Configurable Workspace so that your agents can view the stages and activities in a playbook, work on activities, and have quick access to in-context information.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# Playbook pages

Use playbook pages in CSM Configurable Workspace so that your agents can view the stages and activities in a playbook, work on activities, and have quick access to in-context information.

## Overview of templates, pages, and page variants

Pages provide the base structure for how the system displays record information in CSM Configurable Workspace. You can create and customize pages with [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US), a web user interface builder.

A page template is a pre-defined page configuration. When you create a page in UI Builder, you can select a page template as a starting point. You can also create a page from scratch or by copying another page and then customizing the page to meet your needs.

A page variant is a version of a page that includes unique settings such as the audience, conditions, and page order. For more information about templates, pages, and page variants, see [Creating pages and page variants](config-csm-ws-create-page-variant.md#section_bt3_stk_1bc).

Pages and page variants can also include playbooks, which are created in Workflow Studio. A playbook provides step-by-step guidance for resolving a specific type of case. The workflows that are associated with a specific type of case and the activities that need to be completed to resolve cases of this type are detailed in the playbook.

## Playbook pages

The Playbooks for Customer Service Management plugin provides the following playbook pages:

-   [Case playbook: horizontal stages](csm-playbook-horizontal-stages.md) page
-   [Case playbook: vertical stages](csm-playbook-vertical-stages.md) page

Additional CSM playbook applications provide playbook pages that you can activate and use with case types in CSM Configurable Workspace.

|Application|Page variant|Description|
|-----------|------------|-----------|
|Case Playbook for Complaints v5.0|Complaint case process page|Includes a horizontal stage picker that provides an end-to-end view of the complaint process.|
|Case Playbook for Onboarding v5.0|Onboarding case process page|This playbook page includes a horizontal stage picker at the top of the record that provides an end-to-end view of the onboarding process.|
|Case Playbook for Product Support v4.0|Product Support process page|This playbook page includes a horizontal stage picker at the top of the record that provides an end-to-end view of the product support process.|

For more information, see [Playbook plugins](setting-up-csm-playbooks.md#section_qgq_ylk_llb).

**Note:** By default, playbook pages are read-only. To use a playbook page, [activate the page](../task/activate-process-based-page.md) and set the page order.

## Benefits of using playbook pages

Resolving customer issues or requests often involves the execution of tasks across multiple users, departments, and systems. Different users are responsible for different tasks within the overall resolution process. Using playbooks provides the following benefits:

-   An experience that is tailored to customer service agents and other users.
-   Visibility into the overall resolution process, the current stage in the process, and the activities that need to be completed within that stage.
-   Access to in-context information.

## Configuring playbook pages

The following table includes configuration tasks for playbook pages.

<table id="table_sth_yrb_dxb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Activate a playbook page or page variant](../task/activate-process-based-page.md)

</td><td>

Activate a playbook page or page variant and set the page order.**Note:** Some playbook pages and page variants are not active by default.

</td></tr><tr><td>

[Customize the page header for a playbook page](../task/customize-process-form-header.md)

</td><td>

Configure the page header for a playbook page. The page header includes a primary value and several secondary values. These fields can provide case, account, and contact information at a glance.

</td></tr><tr><td>

[Customize UI actions for a playbook page](../task/customize-process-ui-actions-bar.md)

</td><td>

Configure the UI actions to display in the action bar for a playbook page.

</td></tr><tr><td>

[Customize content in the left side panel for a playbook page](../task/customize-content-left-side-panel.md)

</td><td>

Add custom components in the side panel. By default, this panel includes the Customer 360, Timeline, and Active SLA components.

</td></tr><tr><td>

[Customize tabs in the contextual side panel for a playbook page](../task/customize-process-tabs-in-side-panel.md)

</td><td>

Add or remove the tabs from the contextual side panel. Agents can use these tabs to perform tasks such as adding attachments and viewing recommendations.

</td></tr><tr><td>

[Customize the dynamic related records for a playbook page](../task/customize-dynamic-related-records.md)

</td><td>

Configure the Dynamic Related Records feature to display the related records in the contextual side panel.

</td></tr><tr><td>

[Configure the app route to use an existing subpage](../task/configure-app-route-for-subpage.md)

</td><td>

Create an app route to make an existing page a part of the page collection.

</td></tr><tr><td>

[Configure an optional activity for a playbook](../task/configure-optional-activity-for-a-case-type-playbook.md)

</td><td>

Configure an optional activity in  Workflow Studio at various stages in a playbook so that agents and fulfillers can insert an activity when they are using the playbook.

</td></tr><tr><td>

[Set up a record generator for case type](../task/setup-record-generator-for-case-type.md)

</td><td>

Create a record for a case type as the first step in a playbook by using a playbook record generator.

</td></tr><tr><td>

[Set up email templates in Configurable Workspace](https://www.servicenow.com/docs/access?context=configure-email-templates&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US)

</td><td>

Configure new email templates to enable agents to create emails for common issues.

</td></tr></tbody>
</table>## Using playbook pages

Playbooks enable your agents to view and complete their tasks more efficiently.

<table id="table_l2b_p5g_2xb"><thead><tr><th>

User task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Create a record using a playbook](../task/csm-playbook-create-record.md)

</td><td>

If a playbook is configured to use the  feature, an agent can create a record by using a playbook activity. Creating a record opens the playbook and initiates the first activity, which is to guide an agent through the record creation process.After saving the case, an agent moves to the next activity in the current stage or to the first activity in the next stage.

</td></tr><tr><td>

[Resolve a case using a playbook](csm-playbooks-using.md)

</td><td>

Opening a case takes the agent to the first open assigned activity. An agent can do the following actions while working on the activities in a playbook:

-   View the entire playbook process in the [horizontal stage picker](csm-playbook-templates.md#section_uyk_sp3_cxb).
-   View the activities for each stage in the stacked [playbook activity view](csm-playbook-layout.md#section_oq5_3yw_5pb).
-   [Use the activity stream in the contextual side panel](csm-playbooks-using-activity-stream.md)
-   [Filter activity cards](../task/csm-playbook-filter-activities.md).
-   Select an activity and perform the work required in the main work area.
-   View and update the case details by using the **View Details** button.
-   View the persistent contextual information in the left side panel, such as the account and contact.
-   View the related list tabs in the [Dynamic related records](csm-contextual-related-records.md) component in the contextual side panel.
-   Access information in the contextual side panel, including the activity stream, form ribbon, Agent Assist, Dynamic related records, attachments, and templates.
-   Create tasks, compose email, and add worknotes.
-   Open reference fields in subtabs under the session tab.

</td></tr><tr><td>

[Add an activity to a playbook](https://www.servicenow.com/docs/access?context=playbook-add-optional-activity&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US)

</td><td>

Add optional activities to a playbook stage as needed.

</td></tr><tr><td>

[Summarize case details](case-summarization-in-process-page.md)

</td><td>

Use the Now Assist for CSM case summarization skill to summarize the case details and display this information on the case record.

</td></tr><tr><td>

[Compose an email from an email template](../task/compose-email-from-email-template.md)

</td><td>

Quickly compose emails for common issues by selecting an email template in the Compose Email page instead of manually drafting an email.

</td></tr></tbody>
</table>**Note:** For tasks that an agent completes outside of a playbook, the system automatically updates the playbook activities.

