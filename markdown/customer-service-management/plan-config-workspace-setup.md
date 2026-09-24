---
title: Plan your CRM Workspace configuration
description: Planning your CRM Workspace configuration includes defining your key goals, personas, and requirements. This planning ensures that your configuration directly supports your business objectives and delivers the right experience to each user group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/plan-config-workspace-setup.html
release: brazil
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
breadcrumb: [Set up CRM Workspace, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Plan your CRM Workspace configuration

Planning your CRM Workspace configuration includes defining your key goals, personas, and requirements. This planning ensures that your configuration directly supports your business objectives and delivers the right experience to each user group.

## Define goals and KPIs

Key performance indicators \(KPIs\) are performance measurements of business services or activities. These measurements, taken at regular intervals, result in a series of indicator scores over time.

As part of your planning, clearly define the key performance indicators \(KPIs\) that you are optimizing for. Your KPIs should directly inform the workspace design and configuration decisions. Some KPIs to consider could include improving first contact resolution rates, reducing average handle time, and increasing CSAT scores.

As you set up your workspace components such as lists, landing pages, and contextual side panel, ensure that each element aligns with your identified goals. For instance:

-   KPI goal: Reduce the average resolution time for high-priority cases.
-   Workspace design: Incorporate a gauge visualization on the landing page to display the percentage of cases that met service level agreements \(SLAs\) over the past seven days.

## Define personas

Define the personas who will be using the workspace. In a workspace, audiences can be defined to accomplish certain goals, and different versions of pages can be presented for different personas.

For instance, customer service agents and case managers both use the workspace but have different priorities. You can create separate landing page variants for each persona:

-   Agent landing page: Displays assigned cases and individual performance metrics.
-   Manager landing page: Displays team-level analytics and the team's cases.

With this approach, you can make sure that each persona sees the most relevant information for their role.

## Gather configuration requirements

Review the baseline experience and identify what needs configuration to meet your goals. Multiple customization options are available when setting up features for your CRM Workspace.

The following tape provides the key decisions that for the most common workspace features.

<table id="table_ipn_qvz_jjc"><thead><tr><th>

Feature

</th><th>

Decision

</th><th>

Leading practices/Consideration

</th></tr></thead><tbody><tr><td>

Branding and theming

</td><td>

Do you want your workspace to match your brand?

</td><td>

A theme sets the visual style of a workspace experience and provides a consistent look and feel across all pages.-   Choose colors suited for an effective agent experience and in line with your overall branding strategy.
-   Adhere to logo size and acceptable format guidelines.

For more information see:

-   [View the brand and theme setting in your workspace experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/workspace-view-theme-setting.md)
-   [Working with themes in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/next-experience-theming.md)

</td></tr><tr><td>

Landing page

</td><td>

Do you want to update the headers, containers, or widgets on the landing page?

</td><td>

&lt;add intro&gt;.-   The information on the landing page should be relevant to the logged-in user.
-   Consider the key metrics and condensed data views that the user needs to see regularly.

</td></tr><tr><td>

Tab settings: New record menu

</td><td>

Are new record menus needed for other tables, such as Contact or Case? \(The + button that enables an agent to create a new record.\)

</td><td>

-   Use Interaction as an entry point for case creation. Capture initial triage information separately and provide for first time-resolutions that don’t need a subsequent task \(such as a case, incident, or request\) to be created.
-   User must have create access to the table\(s\) for the button to appear on their records menu in the workspace.
-   Include only those tables that are most frequently used by agents, such as Case and Interaction.

</td></tr><tr><td>

Service catalogs

</td><td>

-   Will agents use service catalogs to create requests on behalf of customers?
-   Which service catalogs need to be added to the service portal to enable this?

</td><td>

-   Consider the holistic agent experience, including case, incident, and request management, to define an effective process.
-   Encourage self-service by customers. Agents creating requests on behalf of users should be for exceptional scenarios.

</td></tr><tr><td>

Lists

</td><td>

-   Are new list categories and lists required?
-   Do existing list categories and lists need to be removed?
-   Are access controls needed for lists for specific roles or groups?
-   Disable the New button on the List view?
-   Are UI notifications required when a record is updated?

</td><td>

Configure list categories, filtered lists, and tailor lists to show specific items by user role in a configurable workspace.-   The order of list categories and lists should make sense to the logged-in users.
-   Remove unwanted lists and list categories to avoid information overload.
-   If UI notifications are required for record updates, define the recipients and the trigger conditions.

</td></tr><tr><td>

Form headers

</td><td>

For each form:-   Is a header required?
-   If yes, which fields should be included in the header?

</td><td>

-   Form headers are optional.
-   Headers provide information that agents can see at a glance.
-   Review the existing headers in the baseline workspace experience and update as needed.

</td></tr><tr><td>

UI actions

</td><td>

For each form:-   Are updates required to existing actions?
-   What additional actions do agents need?

</td><td>

-   Focus on actions used by agents.
-   Leverage actions provided in the baseline workspace experience.
-   If custom actions are needed, use correct scripting meant for workspace.

</td></tr><tr><td>

Ribbon

</td><td>

Do you need to add or change the ribbon widgets displayed for Case records? If yes, specify the following information:-   Data table
-   Widget
-   Width
-   Attributes
-   Placement

</td><td>

In the in the baseline workspace experience, the ribbon includes three widgets: Customer 360, SLA, and Timeline.-   To choose suitable widgets, identify the data frequently required by agents to be more effective and productive.
-   The total ribbon width is 12 units. Divide the width between the widgets based on volume of information they contain.

Train your agents on the ribbon widgets to drive its usage.

</td></tr><tr><td>

Ribbon widgets

</td><td>

Customer 360:-   Provide primary user tables to be displayed \(for example, Contact or Consumer\).
-   Provide primary user fields to be displayed \(for example, Name or Phone\).
-   Provide secondary fields to be displayed.

Timeline: Specify which task states denote that the task is awaiting customer response.

</td><td>

-   Customer 360: Fill out secondary fields so that the widget isn't empty when primary user details are missing.
-   Timeline: Educate agents that not updating task states correctly will impact calculations in this widget.
-   SLA: Train agents to interpret colors for SLAs that are approaching breach limits.

</td></tr><tr><td>

Contextual side panel

</td><td>

For each record page:-   What will the agents need to access quickly?
-   Which tables or related records are involved?
-   Should it be enabled or disabled for specific types of case forms?

</td><td>

Display frequently referenced information that might often take the agent out of the workspace

</td></tr><tr><td>

Form layout

</td><td>

The overall structure of the record page displayed in the workspace, including the arrangement of tabs, sections, and components.-   Which tabs and sections are needed on the form?
-   Should sections be collapsible or mandatory?

</td><td>

-   Group related fields logically to improve agent understanding.
-   Keep important fields higher on the page for visibility.
-   When possible, reuse baseline layouts to ensure consistency.

</td></tr><tr><td>

Form templates

</td><td>

Which form templates do you need? Form templates can pre-populate fields, provide conditions that need to be met, user and group access, and other requirements.

</td><td>

-   Identify the fields most used by agents and use form templates to automate manual input.
-   Identify tables with standard fields that can be pre-populated \(For example, Order or Major Case\).

</td></tr><tr><td>

Lookup and verify

</td><td>

-   Do you want to use the Lookup and verify feature? If yes, for which customers \(for example, Contact or Consumer\).
-   Is caller verification done prior?

</td><td>

Consider using automated authentication methods for enabling the **Verify** check box in the Lookup and verify feature.

</td></tr><tr><td>

Search sources: AI Search in Recommended Actions

</td><td>

-   Configure the Recommended Actions component to include AI Search.
-   Map search sources with guidance inputs for accurate results.

</td><td>

AI Search for Recommended Actions displays relevant search results as cards in the contextual side panel.Recommended Actions is the default for the Front-line case record page and Chat interaction record page. This default provides access to AI Search and Genius results and single-click attach capability.

</td></tr><tr><td>

Search sources: Genius results

</td><td>

Do you want to enable Genius results? If yes, configure the Recommended Actions component to include Genius results.

</td><td>

Genius results provide AI-driven, contextually relevant answers and actions.

</td></tr><tr><td>

Customer Central

</td><td>

-   Specify information to be displayed in ‘Customer Information’: reports, lists, records.
-   Any updates required to ‘Customer Activity’ tab?

</td><td>

-   Pick critical customer information that agents will need quick access to
-   To keep the view refreshed with accurate information, configure the number of days to display data for

</td></tr><tr><td>

Major case management

</td><td>

-   Do you want Major Case Management to be accessible from the workspace?
-   Any updates required to lists, filters, fields, process and access-control for it?

</td><td>

-   Ensure major case managers do not need to use both, classic UI and workspace, spoiling their overall user experience
-   Use manager-specific lists and form layout to avoid displaying excessive information more relevant for agents.

</td></tr></tbody>
</table>## Remaining configuration considerations

<table id="table_k4w_gmk_jgc"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Search

</td><td>

Define search sources that your agents can query in a configurable workspace. Agents can use these keywords to search for specific records or knowledge articles.-   [Configuring search in Next Experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-user-interface/using-search-next-experience.md)
-   [AI search in Recommended Actions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/customer-service-management/ra-csm-ai-search.md)

</td></tr><tr><td>

Configurable Workspace notifications

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
</table>