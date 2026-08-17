---
title: Add a page to the navigation
description: Add pages to the navigation to make them accessible from other pages, such as a home page.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-08-06"
reading_time_minutes: 1
---

# Add a page to the navigation

Add pages to the navigation to make them accessible from other pages, such as a home page.

## About this task

Some pages are added to the navigation by default when you create them. For pages that aren't added automatically added to the navigation, use the following procedure to make them display and accessible via other pages.

The following procedure describes how to complete this task manually. You can also complete the task using agentic development tools, such as Claude Code.

## Before you begin

Role required: none

The ServiceNow® AI Experience Lab for VS Code extension requires the following:

<table id="table_imf_rfb_dkc"><thead><tr><th>

Application

</th><th>

Version

</th><th>

Resources for more information

</th></tr></thead><tbody><tr><td>

Visual Studio Code

</td><td>

1.97 later

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

4.10 or later

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

1.  Select the ServiceNow \[Omitted image "servicenow-youmoji-icon.png"\] icon in the side panel to open the ServiceNow® AI Experience Lab for VS Code extension.

2.  Open a net new or extension experience.

3.  If your project doesn't already have an application.js file, at the experience folder root \(not under `src/extensions/`\), add an application.js file.

    **Tip:** Use the nav helper API from `@servicenow/aiux/aiux-components-nav` rather than adjusting the `navLayoutContext` by hand.

4.  Double-click \(or use the keyboard shortcut\) to open the `application.js` file in explorer.

5.  Add the following lines of code to the application.js file with the page name and target path that you want to add.

    **Note:** To add pages to L2, include an `l2Nav: [{icon, title, action}]` array on the L1 page you pass to `addNavItem`. The page accepts \{icon, title, action, l2Nav?, l3Nav?\}.

    |Action|Code to add in application.js|
    |------|-----------------------------|
    |Add pages to L1 sidebar|`addNavItem(item, {source?})`|
    |Set \(replace\) the L3 tab array on any L1 or L2 page by path|`setL3Nav(targetPath, l3Nav)`|
    |Append tabs to an L1 or L2 page, keeping any tabs already present|`appendL3Nav(targetPath, l3Nav)`|

6.  Save the file.

7.  In the **Script Runner** panel, select **Build**.

8.  Verify that the added page appears at the expected navigation level using the **Quick Preview** panel or by deploying to your instance.

    For more information, see the following resources:

    -   [Preview a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/preview-page-servicenow-ai-experience-lab-for-vs-code.md)
    -   [Deploy changes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/deploy-changes-servicenow-ai-experience-lab-for-vs-code.md)

