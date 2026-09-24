---
title: Set up CRM Workspace
description: Set up and configure CRM Workspace for your agents so they can engage with customers, answer questions, create cases, and resolve issues.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/csm-config-workspace-set-up.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 12
breadcrumb: [CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Set up CRM Workspace

Set up and configure CRM Workspace for your agents so they can engage with customers, answer questions, create cases, and resolve issues.

The CRM Workspace setup and configuration topics include information about the workspace's core capabilities, configuration options, and details for tailoring the experience to meet your specific business requirements.

## Prerequisite information

Before setting up and configuring CRM Workspace, complete the following setup tasks:

-   [Set up your environment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/set-up-your-environment.md): Set up your foundation data and access management, including customer data, product data, and user roles.
-   [Enable your communication channels](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/enable-comm-channels.md): Set up your communication channels, such as chat, email, and phone, so customers can contact you through their preferred methods.
-   [Set up case routing and work assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/case-routing-and-asign.md): If cases should be automatically assigned to agents or groups, set up Advanced Work Assignment \(AWA\). You can use this application to route cases to the appropriate agents.
-   [Familiarize yourself with UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder-overview.md): This tool is a web user interface builder that you use to create or customize pages for workspace experiences.
-   Ensure that you have valid CSM licenses and user roles in place.

## Activating CRM Workspace

Activating the Case Management Core plugin \(com.sn\_customerservice\) provides the CRM Workspace functionality. To activate this plugin:

1.  Navigate to **All** &gt; **System Applications** &gt; **All Available Applications** &gt; **All**.
2.  Search for the plugin by name \(Case Management Core\) or plugin ID \(com.sn\_customerservice\).
3.  Select the plugin card and then select **Install** to begin the installation process.

    The system displays a message when the installation is complete. For more information about the components installed with the Customer Service plugin, see [Find components installed with an application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/find-components.md).


**Note:** When domain separation and delegated admin are enabled in an instance, the administrative user must be in the global domain. Otherwise, the following error appears:

`Application installation is unavailable because another operation is running: Plugin Activation for <plugin name>.`

## Accessing CRM Workspace

Navigate to the CRM Workspace in one of the following ways:

-   Navigate to **All** &gt; **Workspace Experience** &gt; **Workspaces** and then select CRM Workspace.
-   Select **Workspaces** and then select CRM Workspace.
-   Select **Favorites** and then select CRM Workspace \(after creating a favorite by selecting the star next to the workspace name in the workspace header\).

## Configuration tasks

This section describes how you can configure the baseline CRM Workspace to meet your unique needs.

1.  Configure branding and theming.

    Themes enable you to tailor the visual workspace experience for your users. Use the [Theme Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/configuring-next-experience-with-theme-builder.md) application to create themes that reflect your company's brand.

    You can configure and publish multiple themes and designate a default theme. Agents can choose their preferred theme from the available options.

    The following video demonstrates how you can create and manage your themes using Theme Builder.\[Omitted video\] Description: Use Theme Builder to create and manage themes such as colors and branding for a configurable workspace

2.  Configure the landing page.

    The landing page is the initial view that an agent sees when they open their workspace. You can modify the baseline landing page as needed to enhance usability for your agents.

    For more information, see [Create a CRM Workspace landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-landing-page.md).

3.  [Configure the new record action](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-new-record-action.md).

    The new record action \(the **+** button on the tab\) enables agents to quickly create records.

    **Note:** The action to create an interaction record is available by default.

4.  [Configure service catalogs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-service-catalog.md).

    Service catalogs enable agents to submit requests on behalf of customers directly from within CRM Workspace.

5.  [Configure lists](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-lists.md).

    List categories and lists enable agents and managers to quickly find records. You can modify the baseline workspace list categories and lists to better suit the needs of your agents or you can create your own.

6.  Configure record pages.

    A record page provides the base structure for displaying records in CRM Workspace. Record pages include containers, components, and layouts to display record information. Several record pages are available in the baseline implementation. You can use these pages as is or customize as needed,

    For more information, see the following topics:

    -   [Creating pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-ws-create-page-variant.md)
    -   [Record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-config-workspace-record-pages.md)
7.  [Configure form headers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-form-header.md).

    Form headers in CRM Workspace provide a quick glance of case, account, or contact information. You can configure the primary and secondary values that appear in the form header.

8.  [Configure UI actions on forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-form-action.md).

    Form actions enable users to perform common tasks directly from the form. Custom form actions can be configured as needed. For example, use form actions to update record fields, navigate to related records, or trigger other operations.

9.  [Configure the form ribbon and components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-ribbon.md).

    The form ribbon displays information that provides agents with a quick overview of the case details. For example, the form ribbon can include summary information about the contact or consumer, the case timeline, and SLA details.

10. [Configure the form layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-form-layout.md).

    You can configure the layout of a record form as needed. For example, you can add or remove fields that appear on the form, determine field visibility, or add new sections to the form.

11. [Configure tabs in the contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-ws-side-panel-tabs2.md).

    The contextual side panel includes different tools that agents can use to research and resolve customer issues. You can add, rearrange, or hide tabs as well as set default values. You can also [hide tabs in the contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-ws-side-panel-tabs.md).

12. Configure [Customer Central](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/customer-central-configuration.md).

    Customer Central provides agents with all of the information about a customer in one central place. This information is provided in two views:

    -   **Customer Information**: Displays key information about the customer and a view of all recent customer touch points with the service organization.
    -   **Customer History**: Displays all the recent customer touch points with the service organization in the form of an activity feed.

## Set up CRM Workspace using guided setup

You can set up CRM Workspace by using the Customer Service Management Guided Setup. To use the guided setup:

1.  Navigate to **Customer Service** &gt; **Administration** &gt; **Guided Setup**.
2.  Select **Get Started** on the Welcome page.
3.  Scroll through the list of guided setup categories until you reach the CRM Workspace category.
4.  Select **Get Started** in the CRM Workspace category.

    The CRM Workspace category includes one task for the Configurable Workspace Guided Setup.

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

A theme sets the visual style of a configurable workspace experience and provides a consistent look and feel across all pages.-   [View the brand and theme setting in your workspace experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/workspace-view-theme-setting.md)
-   [Working with themes in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/next-experience-theming.md)

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

Configure the way forms appear for your agents or workers in a configurable workspace. You can also configure the fields that appear on the form to be different depending on the record type and user roles. For more information, see [Administering forms for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/administer-forms-configurable-workspace.md).

</td></tr><tr><td>

Additional Forms Configuration

</td><td>

Configure templates that agents can use to pre-populate fields and UI actions to make a configurable workspace more interactive. For more information, see [Administering forms for Configurable Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/administer-forms-configurable-workspace.md).

</td></tr><tr><td>

Search

</td><td>

Define search sources that your agents can query in a configurable workspace. Agents can use these keywords to search for specific records or knowledge articles.-   [Configuring search in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/using-search-next-experience.md)
-   [AI search in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/ra-csm-ai-search.md)

</td></tr><tr><td>

Configurable Workspace Notifications

</td><td>

Determine the conditions when notifications display in a configurable workspace, such as when a record updates or a record assigns to a user.

</td></tr><tr><td>

Advanced Work Assignment \(AWA\)

</td><td>

Set up [Advanced Work Assignment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/awa-application-landing-page.md) to automatically route tasks and interactions to the right agents.

</td></tr><tr><td>

Configurable Workspace Agent Chat

</td><td>

Configure Agent Chat to enable live agents to chat with customers and manage various conversation features for agents and end users. For more information, see [Setting up Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-configure-agent-chat.md).

</td></tr><tr><td>

Playbook

</td><td>

Playbooks display business process workflows in a simple task-oriented view. These step-by-step procedures guide users through workflows that address commonly encountered situations. For more information, see [Building Playbooks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/build-workflows/building-a-process.md).

</td></tr></tbody>
</table>## Configuring workspace pages in UI Builder

You can use UI Builder to configure the pages and components that display information in CRM Workspace including the following:

-   [Landing pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-landing-page.md)
-   [Record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/csm-config-workspace-record-pages.md)
-   [Customer Central – Customer Information tab](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/cust-central-configure-info-tab.md)

For more information, see the [Manage UI Builder pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/work-pages.md) topic in the [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/create-custom-experience.md) documentation.

## Set up communication channels and routing

Enable agents to chat with customers or to receive and place customer calls. You can also set up routing that automatically directs chats to the appropriate agents. For more information, see [Setting up Agent Chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/conversational-interfaces/ac-configure-agent-chat.md).

## Set up additional CRM Workspace components

Complete these tasks to set up the components that are specific to CRM Workspace.

|Task|Description|
|----|-----------|
|[Create or modify a landing page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-landing-page.md)|The landing page is an agent's initial view of the workspace. The CSM Landing Page is included with the Customer Service plugin. You can modify this landing page or you can create and modify a page variant in UI Builder.|
|[Set up a ribbon configuration in CRM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-ribbon.md)|The form ribbon includes components that display information about a record. You can add the Customer 360, Timeline, and SLA components to the Case form ribbon. You can also configure attributes for the Customer 360 and Timeline components.|
|[Set up a form header in CRM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-form-header.md)|Configure form headers that provide a quick summary of case, account, or contact information.|
|[Set up a highlighted value in a form header in CRM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-highlight-value.md)|Configure fields that appear as highlighted values in form headers in CRM Workspace.|
|[Set up a form action in CRM Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-config-ws-form-action.md)|Create form actions that link to UI actions so that you can use the UI actions in CRM Workspace.|
|[Display the form ribbon and form header secondary values in the Contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-display-header-in-sidebar.md)|Configure the form ribbon and the secondary values that appear in a form header to display in the Contextual side panel in CRM Workspace.|
|[Display field values as interaction record tab titles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-display-values-as-tab-titles.md)|Display field values, such as contact or consumer names, as titles on interaction record tabs in CRM Workspace.|
|[Hide tabs in the contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/config-csm-ws-side-panel-tabs.md)|Use the **inlineTabExclusion** UX page property to prevent tabs from appearing in the configurable side panel in CRM Workspace.|
|Configure service catalogs for CSM workspaces|Customer service agents use service catalogs to fulfill catalog item requests. You can configure the Service Workspace Portal to use the catalogs that contain the desired items.|

**Related topics**  


[Activate Customer Service Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/t_ActivateCustomerService.md)

