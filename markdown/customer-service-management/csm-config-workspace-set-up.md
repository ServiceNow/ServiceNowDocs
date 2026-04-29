---
title: Set up CSM Configurable Workspace
description: Set up CSM Configurable Workspace for your agents so they can engage with customers, answer questions, create cases, and resolve issues.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up CSM Configurable Workspace

Set up CSM Configurable Workspace for your agents so they can engage with customers, answer questions, create cases, and resolve issues.

Complete the following tasks to set up CSM Configurable Workspace:

1.  Activate the Customer Service plugin \(com.sn\_customerservice\).
2.  Set up CSM Configurable Workspace using guided setup.
3.  Set up communication channels and routing.
4.  Set up additional components specific to CSM Configurable Workspace.

## Activate the plugin

Activating the Customer Service plugin \(com.sn\_customerservice\) provides the CSM Configurable Workspace functionality. For more information, see the following topics:

-   [Activate Customer Service Management](../task/t_ActivateCustomerService.md)
-   [Plugins activated with Customer Service Management](../reference/plugins-activated-with-csm.md)

## Set up CSM Configurable Workspace using guided setup

You can set up CSM Configurable Workspace by using the Customer Service Management Guided Setup. To use the guided setup:

1.  Navigate to **Customer Service** &gt; **Administration** &gt; **Guided Setup**.
2.  Select **Get Started** on the Welcome page.
3.  Scroll through the list of guided setup categories until you reach the CSM Configurable Workspace category.
4.  Select **Get Started** in the CSM Configurable Workspace category.

    The CSM Configurable Workspace category includes one task for the Configurable Workspace Guided Setup.

5.  Select **Configure** to go to the Configurable Workspace Guided Setup.
6.  Select **Get Started**.

The Configurable Workspace Guided Setup includes a sequence of workspace configuration tasks.

<table id="table_k4w_gmk_jgc"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Branding and theming

</td><td>

A theme sets the visual style of a configurable workspace experience and provides a consistent look and feel across all pages.-   [View the brand and theme setting in your workspace experience](https://www.servicenow.com/docs/access?context=workspace-view-theme-setting&version=australia&pubname=australia-application-development&ft:locale=en-US)
-   [Working with themes in Next Experience](https://www.servicenow.com/docs/access?context=next-experience-theming&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)

</td></tr><tr><td>

Tab Settings

</td><td>

Configure the following in the Tab Settings category:-   Configure a New Record menu by adding a table that agents can select to create new records in a configurable workspace.
-   Select a Service Catalog for your agents to use with a configurable workspace.

</td></tr><tr><td>

Lists

</td><td>

Configure list categories, filtered lists, and tailor lists to show specific items by user role in a configurable workspace.-   Create list categories
-   Create filtered lists

</td></tr><tr><td>

Forms

</td><td>

Configure the way forms appear for your agents or workers in a configurable workspace. You can also configure the fields that appear on the form to be different depending on the record type and user roles. For more information, see [Administering forms for Configurable Workspace](https://www.servicenow.com/docs/access?context=administer-forms-configurable-workspace&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Additional Forms Configuration

</td><td>

Configure templates that agents can use to pre-populate fields and UI actions to make a configurable workspace more interactive. For more information, see [Administering forms for Configurable Workspace](https://www.servicenow.com/docs/access?context=administer-forms-configurable-workspace&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Search

</td><td>

Define search sources that your agents can query in a configurable workspace. Agents can use these keywords to search for specific records or knowledge articles.-   [Configuring search in Next Experience](https://www.servicenow.com/docs/access?context=using-search-next-experience&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US)
-   [AI search in Recommended Actions](ra-csm-ai-search.md)

</td></tr><tr><td>

Configurable Workspace Notifications

</td><td>

Determine the conditions when notifications display in a configurable workspace, such as when a record updates or a record assigns to a user.

</td></tr><tr><td>

Advanced Work Assignment \(AWA\)

</td><td>

Set up [Advanced Work Assignment](https://www.servicenow.com/docs/access?context=awa-application-landing-page&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US) to automatically route tasks and interactions to the right agents.

</td></tr><tr><td>

Configurable Workspace Agent Chat

</td><td>

Configure Agent Chat to enable live agents to chat with customers and manage various conversation features for agents and end users. For more information, see [Setting up Agent Chat](https://www.servicenow.com/docs/access?context=ac-configure-agent-chat&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

</td></tr><tr><td>

Playbook

</td><td>

Playbooks display business process workflows in a simple task-oriented view. These step-by-step procedures guide users through workflows that address commonly encountered situations. For more information, see [Building Playbooks](https://www.servicenow.com/docs/access?context=building-a-process&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

</td></tr></tbody>
</table>## Configuring workspace pages in UI Builder

You can use UI Builder to configure the pages and components that display information in CSM Configurable Workspace including the following:

-   [Landing pages](../task/config-csm-config-ws-landing-page.md)
-   [Record pages](csm-config-workspace-record-pages.md)
-   [Customer Central – Customer Information tab](../task/cust-central-configure-info-tab.md)

For more information, see the [Manage UI Builder pages and page variants](https://www.servicenow.com/docs/access?context=work-pages&version=australia&pubname=australia-application-development&ft:locale=en-US) topic in the [UI Builder](https://www.servicenow.com/docs/access?context=create-custom-experience&version=australia&pubname=australia-application-development&ft:locale=en-US) documentation.

## Set up communication channels and routing

Enable agents to chat with customers or to receive and place customer calls. You can also set up routing that automatically directs chats to the appropriate agents. For more information, see [Setting up Agent Chat](https://www.servicenow.com/docs/access?context=ac-configure-agent-chat&version=australia&pubname=australia-conversational-interfaces&ft:locale=en-US).

## Set up additional CSM Configurable Workspace components

Complete these tasks to set up the components that are specific to CSM Configurable Workspace.

|Task|Description|
|----|-----------|
|[Create or modify a landing page](../task/config-csm-config-ws-landing-page.md)|The landing page is an agent's initial view of the workspace. The **CSM Landing Page** is included with the Customer Service plugin. You can modify this landing page or you can create and modify a page variant in UI Builder.|
|[Set up a ribbon configuration in CSM Configurable Workspace](../task/config-csm-config-ws-ribbon.md)|The form ribbon includes components that display information about a record. You can add the Customer 360, Timeline, and SLA components to the Case form ribbon. You can also configure attributes for the Customer 360 and Timeline components.|
|[Set up a form header in CSM Configurable Workspace](../task/config-csm-config-ws-form-header.md)|Configure form headers that provide a quick summary of case, account, or contact information.|
|[Set up a highlighted value in a form header in CSM Configurable Workspace](../task/config-csm-config-ws-highlight-value.md)|Configure fields that appear as highlighted values in form headers in CSM Configurable Workspace.|
|[Set up a form action in CSM Configurable Workspace](../task/config-csm-config-ws-form-action.md)|Create form actions that link to UI actions so that you can use the UI actions in CSM Configurable Workspace.|
|[Display the form ribbon and form header secondary values in the Contextual side panel](../task/config-csm-display-header-in-sidebar.md)|Configure the form ribbon and the secondary values that appear in a form header to display in the Contextual side panel in CSM Configurable Workspace.|
|[Display field values as interaction record tab titles](../task/config-csm-display-values-as-tab-titles.md)|Display field values, such as contact or consumer names, as titles on interaction record tabs in CSM Configurable Workspace.|
|[Enable the Create Case UI action for case type selection](../task/config-csm-config-ws-ui-action.md)|Enable the **Create Case** UI action for case type selection for one or more selected tables.|
|[Configure tabs in the contextual side panel](../task/config-csm-ws-side-panel-tabs.md)|Use the **inlineTabExclusion** UX page property to prevent tabs from appearing in the configurable side panel in CSM Configurable Workspace.|
|Configure service catalogs for CSM workspaces|Customer service agents use service catalogs to fulfill catalog item requests. You can configure the Service Workspace Portal to use the catalogs that contain the desired items.|

