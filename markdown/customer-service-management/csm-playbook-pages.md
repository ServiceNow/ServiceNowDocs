---
title: Configure templates and pages
description: Use playbook pages in CRM Workspace so that your agents can view the stages and activities in a playbook, work on activities, and have quick access to in-context information.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-playbook-pages.html
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Workspace, Playbooks in Customer Service Management, Agent tools, Organize agent workspaces, Configure, Customer Service Management]
---

# Configure templates and pages

Use playbook pages in CRM Workspace so that your agents can view the stages and activities in a playbook, work on activities, and have quick access to in-context information.

## Pages, page templates, and page variants

Pages provide the base structure for how record information is displayed in CRM Workspace. Pages are created and customized in [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/ui-builder-overview.md), a web user interface builder. Pages and page variants can also include playbooks, which are created in Workflow Studio and provide step-by-step guidance for resolving a specific type of case.

A page template is a pre-defined page configuration. When a page is created in UI Builder, a page template can be selected as a starting point. A page can also be created from scratch or by copying and then customizing an existing page.

A page variant is a version of a page that includes unique settings such as the audience, conditions, and page order. For more information about templates, pages, and page variants, see [Creating pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/config-csm-ws-create-page-variant.md).

## CSM page templates

The following page templates are available with the Playbooks for Customer Service Management application \[com.sn\_csm\_playbook\]. For more information, see [Playbook plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setting-up-csm-playbooks.md).

|Page template|Description|
|-------------|-----------|
|[Case playbook: horizontal stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-horizontal-stages.md)|Includes a horizontal stage picker that displays across the top of the UI and shows persistent information in the left panel.|
|[Case playbook: vertical stages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-vertical-stages.md)|Includes a vertical stage picker that displays in the left panel. This stage picker can track overall progress on the UI in a vertical view.|

Considerations for using these page templates include the number of stages that appear in the picker and the length of the stage names. For example, longer stage names in the horizontal playbook can be truncated.

**Note:** By default, the playbook page templates aren’t active. To activate a page template, see [Activate a playbook page or page variant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-process-based-page.md).

Additional CSM playbook applications provide playbook pages that you can activate and use with case types in CRM Workspace.

|Application|Page variant|Description|
|-----------|------------|-----------|
|Case Playbook for Complaints v5.0|Complaint case process page|Includes a horizontal stage picker that provides an end-to-end view of the complaint process.|
|Case Playbook for Onboarding v5.0|Onboarding case process page|This playbook page includes a horizontal stage picker at the top of the record that provides an end-to-end view of the onboarding process.|
|Case Playbook for Product Support v4.0|Product Support process page|This playbook page includes a horizontal stage picker at the top of the record that provides an end-to-end view of the product support process.|

For more information, see [Playbook plugins](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setting-up-csm-playbooks.md).

**Note:** By default, playbook pages are read-only. To use a playbook page, [activate the page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-process-based-page.md) and set the page order.

## Configuring playbook pages

The following table includes task information for activating and customizing a playbook page. Most customization is done in UI Builder and can happen during setup or after the page is in use.

<table id="table_sth_yrb_dxb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Activate a playbook page or page variant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/activate-process-based-page.md)

</td><td>

Activate a playbook page or page variant and set the page order.**Note:** Some playbook pages and page variants are not active by default.

</td></tr><tr><td>

[Customize the page header for a playbook page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-process-form-header.md)

</td><td>

Configure the page header for a playbook page. The page header includes a primary value and several secondary values. These fields can provide case, account, and contact information at a glance.

</td></tr><tr><td>

[Customize UI actions for a playbook page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-process-ui-actions-bar.md)

</td><td>

Configure the UI actions to display in the action bar for a playbook page.

</td></tr><tr><td>

[Customize content in the left side panel for a playbook page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-content-left-side-panel.md)

</td><td>

Add custom components in the side panel. By default, this panel includes the Customer 360, Timeline, and Active SLA components.

</td></tr><tr><td>

[Customize tabs in the contextual side panel for a playbook page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-process-tabs-in-side-panel.md)

</td><td>

Add or remove the tabs from the contextual side panel. Agents can use these tabs to perform tasks such as adding attachments and viewing recommendations.

</td></tr><tr><td>

[Customize the dynamic related records for a playbook page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/customize-dynamic-related-records.md)

</td><td>

Configure the Dynamic Related Records feature to display the related records in the contextual side panel.

</td></tr><tr><td>

[Configure the app route to use an existing subpage](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-app-route-for-subpage.md)

</td><td>

Create an app route to make an existing page a part of the page collection.

</td></tr><tr><td>

[Configure an optional activity for a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/configure-optional-activity-for-a-case-type-playbook.md)

</td><td>

Configure an optional activity in  Workflow Studio at various stages in a playbook so that agents and fulfillers can insert an activity when they are using the playbook.

</td></tr><tr><td>

[Set up a record generator for case type](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/setup-record-generator-for-case-type.md)

</td><td>

Create a record for a case type as the first step in a playbook by using a playbook record generator.

</td></tr><tr><td>

[Configure an email template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/configure-email-templates.md)

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

[Create a record using a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-create-record.md)

</td><td>

If a playbook is configured to use the playbook record generator feature, an agent can create a record by using a playbook activity. Creating a record opens the playbook and initiates the first activity, which is to guide an agent through the record creation process.After saving the case, an agent moves to the next activity in the current stage or to the first activity in the next stage.

</td></tr><tr><td>

[Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-workspace.md)

</td><td>

Opening a case takes the agent to the first open assigned activity. An agent can do the following actions while working on the activities in a playbook:

-   View the entire playbook process in the Horizontal stage picker. [Case playbook: horizontal stages record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-horizontal-stages.md)
-   View the activities for each stage in the stacked [Select a playbook activity view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/playbook-select-activity-view.md).
-   [Use the activity stream in the contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbooks-using-activity-stream.md)
-   [Filter activity cards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-playbook-filter-activities.md).
-   Select an activity and perform the work required in the main work area.
-   View and update the case details by using the **View Details** button.
-   View the persistent contextual information in the left side panel, such as the account and contact.
-   View the related list tabs in the [Dynamic related records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/csm-contextual-related-records.md) component in the contextual side panel.
-   Access information in the contextual side panel, including the activity stream, form ribbon, Agent Assist, Dynamic related records, attachments, and templates.
-   Create tasks, compose email, and add worknotes.
-   Open reference fields in subtabs under the session tab.

</td></tr><tr><td>

[Add an activity to a playbook](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/playbook-add-optional-activity.md)

</td><td>

Add optional activities to a playbook stage as needed.

</td></tr><tr><td>

[Summarize case details](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/case-summarization-in-process-page.md)

</td><td>

Use the ServiceNow Otto for CSM case summarization skill to summarize the case details and display this information on the case record.

</td></tr><tr><td>

[Compose an email from an email template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/customer-service-management/compose-email-from-email-template.md)

</td><td>

Quickly compose emails for common issues by selecting an email template in the Compose Email page instead of manually drafting an email.

</td></tr></tbody>
</table>**Note:** For tasks that an agent completes outside of a playbook, the system automatically updates the playbook activities.

