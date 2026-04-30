---
title: Creating pages and page variants
description: You can create new pages or customize existing pages in UI Builder to display table and record information in CSM Configurable Workspace.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-08-25"
reading_time_minutes: 4
breadcrumb: [CSM Configurable Workspace record pages, Set up CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Creating pages and page variants

You can create new pages or customize existing pages in UI Builder to display table and record information in CSM Configurable Workspace.

When you create a page in UI Builder, you have the option to create a page from scratch, create a page from a template, or you can duplicate and modify a page variant.

## UI Builder terminology

The following table describes the UI Builder terminology around workspace experiences, pages and page variants, and page templates. For more information about UI Builder terminology, see the [UI Builder glossary](https://www.servicenow.com/docs/access?context=ui-builder-glossary&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

<table id="table_spj_stk_1bc"><thead><tr><th>

Term

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Workspace experience](https://www.servicenow.com/docs/access?context=ui-builder-workspace-settings&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

</td><td>

A workspace experience in UI Builder is a collection of web pages. Users use these pages to interact with an application. A workspace experience includes experience settings, routes, page variants, and the audience and conditions required for each variant.

A workspace experience resides at a specific URL. When an admin creates a workspace experience, they define the web address for the experience and the homepage that the experience uses.

</td></tr><tr><td>

[Page collection](https://www.servicenow.com/docs/access?context=page-collections&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

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

[Create a page from scratch](https://www.servicenow.com/docs/access?context=create-page&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

</td><td>

When you create a page from scratch, you start with a blank page and select layouts and components that guide a user through an experience. Components are like building blocks that you can add to the page and then customize to build the page functionality.

</td></tr><tr><td>

[Create a page from a template](https://www.servicenow.com/docs/access?context=reuse-page-definitions&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

</td><td>

When you create a page from a template, you start with a base structure, including layouts and components. From this starting point, you can customize the page to meet your needs.When you create a page from a template:

-   The page is automatically active.
-   The page includes basic settings.
-   The first variant of the page is also created. You can add settings such as conditions and audience to the variant.

For example, when you create a page from the Front-line case page template, the page includes only basic settings. It does not include the same settings as the Front-line case page variant that is provided out of box.

</td></tr><tr><td>

[Create a page variant](https://www.servicenow.com/docs/access?context=create-variant&version=zurich&pubname=zurich-application-development&ft:locale=en-US)

</td><td>

When you create a page variant, you create a variation of a page that exists at the same path.When you create a page by duplicating a variant, the new page inherits the variant settings.

By creating a page variant, you can target an experience for a specific audience and add conditions that determine when the variant is shown.

-   The audience determines who uses the page variant. For example, you can limit the audience to a specific user role.
-   The conditions determine when a page is shown. For example, you can add a condition for records from a specific table, such as the Case table.

</td></tr></tbody>
</table>For more information about customizing record pages, see [Manage UI Builder pages and page variants](https://www.servicenow.com/docs/access?context=work-pages&version=zurich&pubname=zurich-application-development&ft:locale=en-US).

**Note:** If a page is modified after page variants have been created, the changes to the page do not sync with the variants. These changes must be made manually.

## Determining which page to use

Each record page has an order number. CSM Configurable Workspace uses the active record page with the lowest order number as the default page. When the system displays a record in CSM Configurable Workspace, it uses this default page to display the record information.

Additionally, the system looks at the page settings in this order:

1.  Conditions \(i.e., table\)
2.  Audience \(the user roles that have access to the page\)

If a page variant has no assigned user roles, then every role can access it.

For more information, see [Set record page order](../task/config-csm-ws-set-record-page-order.md).

