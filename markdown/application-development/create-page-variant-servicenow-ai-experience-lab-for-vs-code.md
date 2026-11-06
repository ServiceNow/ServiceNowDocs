---
title: Create a page variant
description: Add a page variant to a route using the ServiceNow Lux Lab for VS Code extension.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/create-page-variant-servicenow-ai-experience-lab-for-vs-code.html
release: australia
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 4
breadcrumb: [Use, ServiceNow Lux Lab for VS Code extension, Building pro-code applications, Developing your application, Classic app development, Building applications]
---

# Create a page variant

Add a page variant to a route using the ServiceNow Lux Lab for VS Code extension.

## About this task

A route belongs to an experience, and an experience can contain multiple routes. A route maps a URL to a page. A page variant lets you add one or more additional pages under an existing route without changing its base page. Use this when you want several variations of a page to share the same URL.

When a user navigates to the route, the extension evaluates the route's variants in ascending order by their order value. For each page variant, it checks whether the user has one of the roles required to view it. The user sees the first variant whose role requirement they meet. If the user does not meet the role requirement for any page variant, they see the route's base page instead.

Projects that use folders and file names from the previous collection page structure still build. You can keep the existing names.

The following procedure describes how to complete this task manually. You can also complete the task using agentic development tools, such as Claude Code.

## Before you begin

Role required: none

You must have an existing route before you create a page variant for it. For information about creating a page, see [Create a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/create-page-servicenow-ai-experience-lab-for-vs-code.md).

The ServiceNow Lux Lab for VS Code extension requires the following:

<table id="table_imf_rfb_dkc"><thead><tr><th>

Application

</th><th>

Version

</th><th>

Resources for more information

</th></tr></thead><tbody><tr><td>

Visual Studio Code

</td><td>

1.97 or later

</td><td>

[Visual Studio Code updates](https://code.visualstudio.com/updates/v1_132)

</td></tr><tr><td>

Node.js

</td><td>

24 or later

</td><td>

[Node.js](https://nodejs.org/en/download)

</td></tr><tr><td>

pnpm

</td><td>

10 or later

</td><td>

[pnpm](https://pnpm.io/installation)

</td></tr><tr><td>

ServiceNow SDK

</td><td>

4.14 or later

</td><td>

[ServiceNow SDK](https://www.npmjs.com/package/@servicenow/sdk)

</td></tr><tr><td>

ServiceNow instance

</td><td>

-   Australia Patch 5 or later
-   Zurich Patch 12 or later

</td><td>

[Prepare your upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/release-notes/rn-prepare-landing-page.md)

</td></tr></tbody>
</table>## Procedure

1.  In the ServiceNow Lux Lab for VS Code extension, create an experience or open an existing experience.

    For information about creating an experience, see [Create a new experience](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/create-a-new-experience-servicenow-ai-experience-lab-for-vs-code.md).

2.  Start the page variant flow.

    If you already have the page folder for the route open in the file explorer, starting there skips the experience and route selections. Otherwise, use the command palette, which walks you through selecting the experience and route.

    -   Using the command palette.
        1.  Access the command palette by pressing Ctrl+Shift+P on Windows or Command+Shift+P on macOS, or by navigating to **View** &gt; **Command Palette**.
        2.  Select **Lux: Create Page Variant**.
        3.  If your project contains more than one experience, select the experience that contains the route.
        4.  Select the route that you want to add the variant to. Routes are listed alphabetically.
    -   Using the file explorer.

        1.  In the explorer panel, select and hold \(or right-click\) one of the following:
            -   An existing page variant folder for a route.
            -   An individual folder for a page variant within it \(for example, `_variants/admin`\).
        2.  Select **Lux: Create Page Variant**. Selecting and holding \(or right-clicking\) any other item in the explorer opens the same guided flow as the command palette, starting with the experience and route selections.
        **Note:** Selecting and holding \(or right-clicking\) a page variant's page.js file directly does not show this option.

3.  Enter a name for the page variant and press Enter.

    The name cannot be empty and must contain at least one character usable in a folder name. The name cannot duplicate an existing page variant name on that route. Matching is case-insensitive.

4.  Enter an order for the page variant, or accept the suggested value, and press Enter.

    The extension suggests an order based on the highest order already used on that route, plus 10 \(or 10 if the route has no variants yet\). If you enter a value that duplicates an existing order or reaches the route's base page order, the extension shows a non-blocking warning but still accepts the value.

5.  Select whether to restrict the page variant by role.

    Select **No additional role restriction** so that any user who can reach the route can open the page variant. Select **Restrict by role** to open a searchable, check box list of roles from the connected instance. Search for and check one or more roles, then select **OK**. A user sees the page variant only if they have at least one of the selected roles.


## Result

The extension creates the page variant under the selected route and opens the new page file automatically. Page variants are stored in a \_variants folder within the route's page folder, with each variant in its own subfolder \(for example, `home/_variants/admin/page.js`\). The route's original `page.js` file remains unchanged as the base page. This procedure only changes local files; the variant isn't visible on your instance until you deploy your changes.

## What to do next

-   [Preview a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/preview-page-servicenow-ai-experience-lab-for-vs-code.md)
-   [Add a page to the navigation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/add-page-to-navigation-servicenow-ai-experience-lab-for-vs-code.md)
-   [Deploy changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/deploy-changes-servicenow-ai-experience-lab-for-vs-code.md)

