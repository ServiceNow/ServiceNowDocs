---
title: CSM Configurable Workspace record pages
description: A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. This includes records such as cases, incidents, and tasks.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2025-06-09"
reading_time_minutes: 4
breadcrumb: [Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configuring Customer Service Management, Customer Service Management]
---

# CSM Configurable Workspace record pages

A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. This includes records such as cases, incidents, and tasks.

## Record page overview

Record pages include elements such as layouts, containers, and components to display record information. Some record pages, including the **CSM default record page** and **CSM Interaction record page**, leverage additional logic using presets, controllers, and extension points. Pages with preset and controller logic benefit from reusability because they automatically inherit styling, events, and data binding. This reusability makes simplifies configuration and makes the pages upgrade friendly.

Several record pages are included with CSM Configurable Workspace. You can use these record pages as is or you can customize them to suit your needs. For more information about customizing record pages, see [Manage UI Builder pages and page variants](https://www.servicenow.com/docs/access?context=work-pages&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US).

Each record page has an order value. The system uses the pages with the lowest order values as the [default record pages](csm-config-workspace-record-pages.md#section_j34_kwm_2vb). When the system displays information in CSM Configurable Workspace, such as interaction and case records, it uses the elements in the default pages to determine the page appearance.

## Available record pages

Several record pages are included with CSM Configurable Workspace.

<table id="table_hmm_t21_lzb"><thead><tr><th>

Page

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[CSM default record page](csm-default-record-page.md)

</td><td>

This page builds on the Record default page and includes specific features for case management.

**Note:** Use this page to display generative AI elements and functionality available with Now Assist for Customer Service Management \(CSM\).

</td></tr><tr><td>

[CSM Interaction record page](csm-interaction-record-page.md)

</td><td>

This page builds on the interaction record page and includes CSM-specific features for interaction management.

**Note:** Use this page to display generative AI elements and functionality available with Now Assist for Customer Service Management \(CSM\).

</td></tr><tr><td>

[Front-line case page](csm-front-line-case-page.md)

</td><td>

This page is designed for front-line agents. It provides a simplified case view that enables agents to quickly gather context, categorize cases, and provide prompt responses to customers.

</td></tr><tr><td>

Record default

</td><td>

This page provides the basic structure for a record page, including record information, a communication interface, and suggestions for issue resolution. This page is also known as the standard record page.

**Note:** The Record default page is no longer supported with patches and fixes.

</td></tr><tr><td>

Interaction record page

</td><td>

This page provides the basic structure for an interaction record, including interaction information and related search results.

**Note:** The Interaction record page is no longer supported with patches and fixes.

</td></tr></tbody>
</table>## Record page elements

Record pages are made up of different elements that determine how record information is displayed in CSM Configurable Workspace.

<table id="table_iyv_lzx_hzb"><thead><tr><th>

Element

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Layouts

</td><td>

The metadata that determines how components are positioned on a page and what CSS rules apply. Layouts enable you to create useful and visually appealing pages.

</td></tr><tr><td>

Containers

</td><td>

Hold one or more components on a page.

</td></tr><tr><td>

Components

</td><td>

Components are the building blocks that you use to create pages. End users, such as agents, use components to view and interact with data. Commonly used components include Heading, Image, List, Form, and Button.For more information about components and component configuration, see the [ServiceNow® Developer site](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?availability[]=Draft&availability[]=In+Progress&availability[]=Available&categories[]=Dev-Design+System&releases[]=utah&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

</td></tr><tr><td>

[Presets](https://www.servicenow.com/docs/access?context=presets&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

</td><td>

A preset is a set of instructions that define configuration values for a specific component. A preset also specifies how a component connects to a controller. Using presets can simplify component configuration and enable you to avoid manual data binding.

</td></tr><tr><td>

[Controllers](https://www.servicenow.com/docs/access?context=controllers&version=xanadu&pubname=xanadu-application-development&ft:locale=en-US)

</td><td>

A controller combines the complex business logic, including data brokers, state parameters, scripting, and event management, into a single entity. Presets use the data in a controller to auto-configure a component.

</td></tr><tr><td>

Extension points

</td><td>

An extension point enables subpages, such as viewports and page collections, to inherit controllers from the parent page. Extension points also improve the ability to upgrade.

</td></tr></tbody>
</table>## Default record pages

Each record page has an order number and the page with the lowest order number is the default page. When the system displays a record in CSM Configurable Workspace, it uses this default page to display the record information.

New Z-boot customers see the following pages by default:

-   CSM default record page
-   CSM Interaction record page

Upgrade customers retain their custom record pages. However, the following pages are no longer supported with patches and fixes:

-   Record default
-   Interaction record page

For more information about setting the default record pages, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

