---
title: CSM Configurable Workspace record pages
description: A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. This includes records such as cases, tasks, and interactions.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace record pages

A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. This includes records such as cases, tasks, and interactions.

## Record page overview

Record pages include elements such as layouts, containers, and components to display record information. Some record pages leverage additional logic using presets, controllers, and extension points. Pages with preset and controller logic benefit from reusability because they automatically inherit styling, events, and data binding. This reusability makes simplifies configuration and makes the pages upgrade friendly.

Several record pages are included with CSM Configurable Workspace. You can use these record pages as is or you can customize them to suit your needs. For more information about customizing record pages, see [Manage UI Builder pages and page variants](https://www.servicenow.com/docs/access?context=work-pages&version=australia&pubname=australia-application-development&ft:locale=en-US).

## Record pages available with CSM Configurable Workspace

Several record pages are included with CSM Configurable Workspace.

<table id="table_hmm_t21_lzb"><thead><tr><th>

Page

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[CSM default record page](csm-default-record-page.md)

</td><td>

This page provides the basic structure for case management, including record information, chat and phone features, and suggestions for resolving issues.**Note:** Use this page to display generative AI elements and functionality available with [Now Assist for Customer Service Management \(CSM\)](now-assist-csm.md).

</td></tr><tr><td>

[Front-line case page](csm-front-line-case-page.md)

</td><td>

This page is designed for front-line agents. It provides a simplified case view that enables agents to quickly gather context, categorize cases, and provide prompt responses to customers.

</td></tr><tr><td>

[CSM Interaction record page](csm-interaction-record-page.md)

</td><td>

This page includes CSM-specific features for interaction management, including interaction information and related search results, and enables agents to accept and respond to live chats, calls, email, and SMS messages.**Note:** Use this page to display generative AI elements and functionality available with [Now Assist for Customer Service Management \(CSM\)](now-assist-csm.md).

</td></tr><tr><td>

[Email interaction record page](csm-email-interaction-record-page.md)

</td><td>

This page enables agents to manage email conversations with customers using interaction records.

</td></tr><tr><td>

[CSM voice interaction record page](csm-native-voice-record-page.md)

</td><td>

This page provides a component that customers can use for integration with Contact Center as a Service \(CCaaS\) providers and an interface that agents can use to handle customer phone calls.

</td></tr><tr><td>

[CSM centered chat interaction record page](csm-centered-chat-interaction-page.md)

</td><td>

This page provides a chat component in the center of the workspace that agents can use to handle customer chat conversations.

</td></tr><tr><td>

Record default

</td><td>

This page provides the basic structure for a record page, including record information, a communication interface, and suggestions for issue resolution. This page is also known as the standard record page.

**Note:** The Record default page is no longer supported with patches and fixes.

</td></tr><tr><td>

Interaction record page

</td><td>

This page provides the basic structure for an interaction record, including interaction information and related search results.**Note:** The Interaction record page is no longer supported with patches and fixes.

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

A container holds one or more components on a page. Think of a container as an area of the page where you add information, images, or functionality \(your components\).

</td></tr><tr><td>

Components

</td><td>

Components are the building blocks that you use to create pages. End users, such as agents, use components to view and interact with data. Commonly used components include Heading, Image, List, Form, and Button.For more information about components and component configuration, see the [ServiceNow® Developer site](https://developer.servicenow.com/dev.do#!/reference/next-experience/components?availability[]=Draft&availability[]=In+Progress&availability[]=Available&categories[]=Dev-Design+System&releases[]=utah&query=&order_by=nameAsc&limit=120&offset=0&categories[]=uib_component&categories[]=uib_macroponent-component&categories[]=uib_facades).

</td></tr><tr><td>

[Presets](https://www.servicenow.com/docs/access?context=presets&version=australia&pubname=australia-application-development&ft:locale=en-US)

</td><td>

A preset is a set of instructions that define configuration values for a specific component. A preset also specifies how a component connects to a controller. Using presets can simplify component configuration and enable you to avoid manual data binding.

</td></tr><tr><td>

[Controllers](https://www.servicenow.com/docs/access?context=controllers&version=australia&pubname=australia-application-development&ft:locale=en-US)

</td><td>

A controller combines the complex business logic, including data brokers, state parameters, scripting, and event management, into a single entity. Presets use the data in a controller to auto-configure a component.

</td></tr><tr><td>

Extension points

</td><td>

An extension point enables subpages, such as viewports and page collections, to inherit controllers from the parent page. Extension points also improve the ability to upgrade.

</td></tr></tbody>
</table>## Determining which record page is used

Record pages include several settings that the system uses to determine which record page to use when displaying information in CSM Configurable Workspace.

-   **Active**: A record page can be active or inactive. The system evaluates active pages when determining which page to use.
-   **Order**: A record page has an order value. The system uses this order value when determining which page to use. The page with the lowest order value is the default record page.
-   **Conditions**: A record page can have one or more conditions that determine when it is used. For example, a record page can have a condition that specifies a table, such as the Interaction \[interaction\] table. This condition limits the use of the page to records from the Interaction table.
-   **Audience**: A record page can have a specified audience. This audience determines who can see the page. If no audience is specified, all users can see the page.

The system chooses a record page by evaluating the conditions, order values, and audience on the available active pages.

-   If there are no active pages with conditions or audience, the system chooses the page with the lowest order value.
-   If there is an active page with one or more conditions and those conditions are met, the system chooses that page.
-   If there are two active pages with the same conditions, the system chooses the page with the lowest order value.
-   If an audience is specified, only those users can see the record page.

## Default record pages

Each record page has an order value and the page with the lowest order number is the default record page.

New zBoot customers see the following pages by default:

-   CSM default record page
-   CSM Interaction record page

Upgrade customers retain their custom record pages. However, the following pages are no longer supported with patches and fixes:

-   Record default
-   Interaction record page

For more information about setting the default record pages, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

**Note:** Starting with the Australia release, the admin role includes all roles. With this change, the admin role can see the following pages:

-   Front-line case page
-   CSM centered chat interaction record page

