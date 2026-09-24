---
title: Create a CRM Workspace landing page
description: Create landing pages for different agents and teams by creating a page variant and adding or modifying containers and components.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/customer-service-management/config-csm-config-ws-landing-page.html
release: brazil
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Set up CRM Workspace, CRM Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Create a CRM Workspace landing page

Create landing pages for different agents and teams by creating a page variant and adding or modifying containers and components.

## Before you begin

Role required: workspace\_admin, ui\_builder\_admin, admin

## About this task

A landing page is the page that an agent sees when they open their workspace. One landing page for CRM Workspace is included with the Case Management Core plugin \(com.sn\_customerservice\). This page, the CSM Landing Page, gives agents an overview of their new, assigned and high priority cases, plus the cases assigned to their groups.

You can create a variant of this page in [UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/ui-builder-overview.md), a web user interface builder, and modify it as needed.

**Note:** It is important to create a variant of the CSM Landing Page to prevent issues with upgrades.

For example, you can use UI Builder to perform these tasks:

<table id="table_a12_gjp_ynb"><thead><tr><th>

Task

</th><th>

Description

</th></tr></thead><tbody><tr><td>

[Change the page layout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/change-layout.md)

</td><td>

The layout governs the slots that are available on a page, how the slots are positioned, and what CSS rules apply to them. For more information about layouts and layout systems, see [Work with layouts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/work-layouts.md).

</td></tr><tr><td>

[Add components to the page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/add-components.md)

</td><td>

Components are the base elements of your page. Components range from core elements like buttons and labels to more complex experience components like lists and forms. For more information, see [Work with components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/work-components.md).**Note:** You can also find information about UI Builder components on the ServiceNow developer site. For more information, see the component documentation on www.devportaldocs.service-now.com/.

</td></tr><tr><td>

[Connect data resources to the components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/connect-data.md)

</td><td>

Connect data resources to dynamically expose data from tables, records, or other elements on your page. For more information, see [Work with data resources](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/data-resources.md).

</td></tr></tbody>
</table>## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**.

2.  In the **My experiences** section, select CRM Workspace.

3.  In the Page drop-down menu, select **Landing Page**.

4.  In the Variants list, select **CSM Landing Page**.

5.  Create a landing page variant.

    1.  Select the additional actions menu next to the **CSM Landing Page** variant and then select **Duplicate variant**.

    2.  In the Create a variant pop-up window, add a **Variant name**.

    3.  Select **Create**.

    4.  If desired, specify the audience and display conditions for the page variant.

        The audience determines who can see the page. An audience is a collection of user roles. For more information, see [Understanding your audiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/add-audiences.md).

        The **Order** field determines which page is displayed. The page with the lowest order number is displayed first.

    5.  Select **Save**.

        The system displays the landing page variant you created in the Landing Page section in UI Builder. The **Audience** and **Order** settings determine which landing page is displayed for any given persona.

6.  Add or modify containers and components for the landing page variant.

    See the UI Builder documentation for details about adding or modifying containers and components.

    -   [Add components to a page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/add-components.md): Beginning with step 4, use this task to add a component to a container and to configure the component properties and event handlers. This task also contains information about adding additional containers.
    -   [Add styling to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/add-styling-to-component.md): Beginning with step 3, set CSS styles for a component to change its default appearance.
    -   [Add a modal to a component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/modals-uib.md): Beginning with step 5, add a window that appears when a user selects a component. For example, if you add a button component that deletes a record, you can add a modal that asks the user to confirm the record deletion.
7.  Select **Save** to save the changes to the page variant.

    You can see the landing page variant in the **Landing Page** section in UI Builder.


