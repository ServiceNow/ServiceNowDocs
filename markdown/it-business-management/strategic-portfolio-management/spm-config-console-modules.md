---
title: Modules in Setup Hub \(SPM\)
description: Module-by-module listing of the setup items that Setup Hub \(SPM\) surfaces, with cross-references to the per-application configuration topic each item launches.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-business-management/strategic-portfolio-management/spm-config-console-modules.html
release: zurich
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: reference
last_updated: "2026-05-25"
reading_time_minutes: 7
keywords: [Now Assist Setup, Strategic Portfolio Management, SPM, configuration console, setup modules, common setup, financials, fiscal calendar, demand management, project management, resource management, strategic planning, portfolio planning, enterprise-wide deployment, performance analytics, business units, departments, cost types, project templates, partitions]
audience: administrator
breadcrumb: [Setup Hub \(SPM\), Strategic Portfolio Management]
---

# Modules in Setup Hub \(SPM\)

Module-by-module listing of the setup items that Setup Hub \(SPM\) surfaces, with cross-references to the per-application configuration topic each item launches.

The console groups setup items into the modules listed in this topic. The modules that a system administrator sees depend on the Strategic Portfolio Management \(SPM\) applications licensed for the instance. The order of modules shown here matches the order in which the console displays them.

## Common setup

Items shared across SPM applications, including organization structure data and analytics activation.

|Module|Configuration item|Description|
|------|------------------|-----------|
|Define organization structure|Set up business units|Define the top level of your organization structure with business units. SPM tables reference business units to filter and segment data automatically, drive hierarchy-based workflows and approvals, generate aligned reports, and simplify access control.|
|Define organization structure|Set up departments|Define organizational subdivisions within your business units. SPM tables reference departments alongside business units to filter data, drive workflows, generate aligned reports, and simplify access control.|
|Reporting setup|Activate performance analytics jobs|Activate the Performance Analytics scheduled job that powers Project Portfolio Management \(PPM\) dashboards and indicators.|

## Demand Management

Items that configure demand management user roles, intake channels, and the demand form. Sub-modules group related items under the **Demand Management** module.

|Module|Configuration item|Description|
|------|------------------|-----------|
|Setup user roles|Users|Manage users that have access to Demand Management. For more information, see [Demand Management users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/explore-demand-workspace.md).|
|Setup user roles|Groups|Manage groups that have access to Demand Management. For more information, see [Demand Management users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/explore-demand-workspace.md).|
|Configure demand intake channels|Service Catalog|Configure catalog items that let users submit demands through the Service Catalog. Catalog items are preconfigured for all users; edit them in Catalog Builder. For more information, see .|
|Configure demand intake channels|Demand form|Customize the demand form used by demand users. Use Form Builder to add or remove fields and adjust the layout. For more information, see [Forms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/form-field-information-for-dw.md).|
|Demand management|Configure demand playbooks|Review the default demand playbooks for demand managers and demand users. Customize them in Workflow Studio to define stages, activities, approval flows, and state transitions. For more information, see [Playbooks in Next Experience for Demand Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-planning/playbooks-in-demand-workspace.md).|
|Demand Management|Advanced settings|Access advanced Demand Management settings, including assessment metric categories used to evaluate demands. For more information, see [View an assessment metric category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/demand-management/t_CreateAnAssessmentCategory.md).|

## Project Management

Items that configure project management, including user roles, project types, templates, schedules, and advanced settings. Sub-modules group related items under the **Project Management** module.

|Module|Configuration item|Description|
|------|------------------|-----------|
|Setup user roles|Users|Manage users that have access to project management. For more information, see [Project Management user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-management/exploring-project-management.md).|
|Setup user roles|Groups|Manage groups that have access to project management. For more information, see [Project Management user roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-management/exploring-project-management.md).|
|Setup project types|Setup dynamic categories|Define dynamic categories and attributes in the Default SPM Dynamic Namespace to add custom fields, such as Boolean, Date, or Integer, to projects and other planning items.|
|Setup project types|Setup form views|Customize the project form used by project managers and project users. Use Form Builder to add or remove fields and adjust the layout. For more information, see []().|
|Setup project types|Project types|Define project types to apply distinct workflows, approval flows, and field requirements to different categories of projects. Assign project types to specific projects, portfolios, or departments.|
|Project Management|Configure Project Playbooks|Review the default project playbooks \(Project default and Stage gate default\) and customize them in Workflow Studio to match your project management methodology. For more information, see [Use Playbooks in Project Workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/use-playbooks-pw.md).|
|Project Management|Setup project templates|Create reusable project templates as starting points for new projects to ensure consistency and reduce setup time. For more information, see [Project templates](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-management/c_ProjectTemplates.md).|
|Project Management|Setup status report templates|Define status report templates that project managers use to communicate project progress. For more information, see[Status reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-workspace/create-a-status-report-in-project-workspace.md).|
|Project Management|Setup project schedules|Define working days and hours used to estimate project timelines. The default Project Management Schedule applies to all projects and does not include holidays; create custom schedules to add holidays or different working calendars. For more information, see [Project Schedules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-management/t_UseAProjectSchedule.md).|
|Project Management|Advanced settings|Access advanced project management settings such as budgets, forecasts, widgets, diagnostics, planning attributes, time sheet policies, and risk value matrixes. For more information, see [Project Diagnostics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/project-management/project-diagnostics-overview.md).|

## Resource Management

Items that configure resource management through the **Resource Management** guided setup wizard.

|Module|Configuration item|Description|
|------|------------------|-----------|
|Resource Management|Resource Management guided setup|Launch the Resource Management guided setup to configure resource planning and allocation. The wizard walks through resource pools, capacity planning, skill definitions, and allocation settings.|

## Financials

Items related to system currency, fiscal calendar setup, and cost type definitions. The **Financials** module surfaces items directly and through the **Setup fiscal calendar** sub-module.

|Module|Configuration item|Description|
|------|------------------|-----------|
|Financials|Configure system currency|Set the default system currency by updating the `glide.system.locale` system property. A blank Value field defaults to USD.|
|Setup fiscal calendar|Generate fiscal calendar|Generate the fiscal calendar that defines fiscal periods for fund requests and allocations. The calendar type drives funding frequency, such as monthly or quarterly, and can't change after funds have been allocated to a period.|
|Setup fiscal calendar|Review fiscal periods|Review the years, quarters, and months created by your fiscal calendar. Each period shows start and end dates, parent period relationships, and type. Select **Validate Periods** to confirm the configuration.|
|Financials|Review/Setup Cost type definitions|Review default cost types and create custom cost types to match your organization's financial tracking. Retain or replace the Labor cost types to keep resource management working.|

## Strategic Planning and Portfolio Planning

Items that configure Strategic Planning and Portfolio Planning capabilities, including the guided setup wizard and demand playbooks.

|Module|Configuration item|Description|
|------|------------------|-----------|
|Strategic and Portfolio Planning|Set up Strategic Planning or Portfolio Planning|Launch the Strategic Planning or Portfolio Planning guided setup to configure planning capabilities in your SPM environment. The wizard walks you through integrations, alignment settings, portfolio structures, and planning settings, and you can run it multiple times as your configuration needs evolve.|

## Enterprise-Wide Deployment

Items that govern multi-partition deployment of Strategic Portfolio Management \(SPM\).

|Module|Configuration item|Description|
|------|------------------|-----------|
|Partitions|Set up partitions|Define data visibility boundaries for teams on the same instance. Create a partition for each function such as team, business unit, or department that requires separate access to project, demand, program, or portfolio records. For more information, see [Create and configure a partition](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-business-management/strategic-portfolio-management/create-partition-ewd.md).|

