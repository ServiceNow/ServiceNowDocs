---
title: CSM Configurable Workspace overview
description: CSM Configurable Workspace is a ServiceNow workspace specifically designed for customer service agents. This workspace is designed to improve user efficiency and facilitate resolutions and can be configured using UI Builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/customer-service-management/csm-config-workspace-overview.html
release: zurich
product: Customer Service Management
classification: customer-service-management
topic_type: concept
last_updated: "2025-11-26"
reading_time_minutes: 3
breadcrumb: [CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace overview

CSM Configurable Workspace is a ServiceNow workspace specifically designed for customer service agents. This workspace is designed to improve user efficiency and facilitate resolutions and can be configured using UI Builder.

The [configurable workspace UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/learn-about-agent-workspace.md) provides a suite of tools in a single focused work area. It displays the lists and forms that agents are used to working in within the Core UI. It also includes features that enable agents to be more efficient, manage multiple cases, and quickly orient themselves to the current task.

## CSM Configurable Workspace and UI Builder

ServiceNow configurable workspaces use content pages to display list, table, and record information. These pages contain layouts and components that provide building blocks for creating user interfaces.

Some [record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-config-workspace-record-pages.md) are provided with the CSM Configurable Workspace application, such as the [CSM default record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-default-record-page.md) and the [CSM Interaction record page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-interaction-record-page.md).

You can customize these content pages and create content pages for workspaces using [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder/ui-builder-overview.md), a web user interface builder. With UI Builder, you can:

-   Create pages and page variants, tailoring workspace pages for multiple user roles.
-   Configure page layouts, containers, and components, drawing from the library of reusable Next Experience components.
-   Customize components for page layouts, content, data visualization, messaging, and navigation.

For more information about working with content pages and components, see the following topics:

-   [CSM Configurable Workspace record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-config-workspace-record-pages.md)
-   [Creating pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/config-csm-ws-create-page-variant.md)
-   [Work with components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/application-development/ui-builder/work-components.md).
-   [Next Experience Components documentation](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

## Viewing information in CSM Configurable Workspace

Agents can view information in different ways in CSM Configurable Workspace including landing pages and dashboards, list pages, and record pages.

|Information|Description|
|-----------|-----------|
|[Landing pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-workspace-landing-pages.md)|Landing pages provide agents with a starting point to get into their work. These pages can include filtered lists such as assigned cases and case tasks, key performance indicators \(KPIs\), and other metrics. Agents can quickly scan the information presented on a landing page and prioritize cases and case tasks, access records, and track their performance.|
|[Dashboards](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-ws-landing-page-dashboard.md)|Dashboards provide an overview of information such as filtered lists, reports, and performance analytics. Dashboards are flexible and easily customizable so agents can display the information they need.|
|[List pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/lists-configurable-workspace.md)|A list displays records from a database table. CSM Configurable Workspace uses list pages to display list information such as cases and case tasks. These pages are designed to help agents navigate, filter, and manage records.|
|[Record pages](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/customer-service-management/csm-config-workspace-record-pages.md)|A record displays the information from one record in a database table. CSM Configurable Workspace uses record pages to provide the base structure for how that information is displayed. Record pages include elements such as layouts, containers, and components to display record information.|

## Configurable workspace tutorials

The following tutorials describe the different parts of a workspace and give you an overview of how a workspace works.

-   [Workspace tutorial for agents starting with a record](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/workspace-tutorial-for-agents.md)
-   [Workspace tutorial for agents starting with a chat](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/platform-user-interface/configure-user-experiences/workspace-tutorial-agents-chat.md)

