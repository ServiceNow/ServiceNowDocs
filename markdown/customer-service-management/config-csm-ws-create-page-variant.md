---
title: Creating pages and page variants
description: You can create new pages or customize existing pages in UI Builder to display table and record information in CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Record pages and page templates, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Creating pages and page variants

You can create new pages or customize existing pages in UI Builder to display table and record information in CSM Configurable Workspace.

When you create a page in UI Builder, you have the option to create a page from scratch, create a page from a template, or you can duplicate and modify a page variant.

## UI Builder terminology

The following table describes the UI Builder terminology around workspace experiences, pages and page variants, and page templates. For more information about UI Builder terminology, see the UI Builder glossary.

<table id="table_spj_stk_1bc"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Workspace experience

</td><td>

A workspace experience in UI Builder is a collection of web pages. Users use these pages to interact with an application. A workspace experience includes experience settings, routes, page variants, and the audience and conditions required for each variant.

A workspace experience resides at a specific URL. When an admin creates a workspace experience, they define the web address for the experience and the homepage that the experience uses.

</td></tr><tr><td>

Page collection

</td><td>

A page collection is a group of pages that can be used across multiple workspace experiences within tabs or modals.

</td></tr><tr><td>

Page

</td><td>

A page is a collection of layouts, columns, and components that display information in a workspace.-   A page has a unique name.
-   A page has a unique URL. The page contains content that resides at this URL.
-   A page includes components that display data from tables and records.

</td></tr><tr><td>

Page variant

</td><td>

A page variant is a version of a page that has unique settings, including audience, conditions, and order.-   Admins can create variants of pages to target experiences for different audiences at the same URL.
-   When a user opens a page URL, the variant that they see is based on these settings.

You can create a page variant if you want to use the same page and make minor changes for a different audience. For example, you can create a landing page for customer service agents and a variant of that landing page for customer service managers.

</td></tr><tr><td>

Page template

</td><td>

A page template provides a base structure for a page that you can customize to meet your needs. Using a page template can help you create pages faster and keep pages consistent within an experience.

Page templates can include components, data resources, and a layout.

</td></tr></tbody>
</table>## Methods for creating pages and page variants

There are different ways to create pages and page variants in UI Builder.

<table id="table_jpg_nkm_w1c"><thead><tr><th>

Method

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Create a page from scratch

</td><td>

When you create a page from scratch, you start with a blank page and select layouts and components that guide a user through an experience. Components are like building blocks that you can add to the page and then customize to build the page functionality.

</td></tr><tr><td>

Create a page from a template

</td><td>

When you create a page from a template, you start with a base structure, including layouts and components. From this starting point, you can customize the page to meet your needs.When you create a page from a template:

-   The page is automatically active.
-   The page includes basic settings.
-   The first variant of the page is also created. You can add settings such as conditions and audience to the variant.

For example, when you create a page from the Front-line case page template, the page includes only basic settings. It does not include the same settings as the Front-line case page variant that is provided out of box.

</td></tr><tr><td>

Create a page variant

</td><td>

When you create a page variant, you create a variation of a page that exists at the same path.When you create a page by duplicating a variant, the new page inherits the variant settings.

By creating a page variant, you can target an experience for a specific audience and add conditions that determine when the variant is shown.

-   The audience determines who uses the page variant. For example, you can limit the audience to a specific user role.
-   The conditions determine when a page is shown. For example, you can add a condition for records from a specific table, such as the Case table.

</td></tr></tbody>
</table>For more information about customizing record pages, see Manage UI Builder pages and page variants.

**Note:** If a page is modified after page variants have been created, the changes to the page do not sync with the variants. These changes must be made manually.

## Determining which record page is used

There are several settings that determine which record page the system uses to display information in CSM Configurable Workspace.

-   **Order value**: Each record page has an order value. The system uses this order value to determine which record page is used. The active page with the lowest order value is the default record page.
-   **Conditions**: A record page can have one or more conditions that determine when it is used. For example, a record page can have a condition that specifies a table, such as the Interaction \[interaction\] table. This condition limits the use of the page to records from the Interaction table.
-   **Audience**: A record page can have a defined audience or set of user roles such as the sn\_customerservice\_agent role. The audience determine the users that have access to the page. If a record page has no assigned user roles, then every role can access it.

The system chooses a record page by evaluating the settings on the available active pages:

-   If there are no active pages with conditions or audience, the system chooses the page with the lowest order value.
-   If there is an active page with one or more conditions and those conditions are met, the system chooses that page.
-   If there are two active pages with the same conditions, the system chooses the page with the lowest order value.

For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

**Related topics**  


[bundle-platux.create-configurable-workspace-experience-uib]

[bundle-platux.create-configurable-workspace-page-uib]

