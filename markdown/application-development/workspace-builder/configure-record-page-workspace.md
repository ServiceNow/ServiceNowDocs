---
title: Add a record page for a workspace in Workspace Builder
description: Configure a record page for a workspace in Workspace Builder. Use containers and components to guide a user through an experience. Each record page is linked to only one data table.
locale: en-US
release: australia
product: Workspace Builder
classification: workspace-builder
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Use, Workspace Builder, Builder library, Developing your application, Building applications]
---

# Add a record page for a workspace in Workspace Builder

Configure a record page for a workspace in Workspace Builder. Use containers and components to guide a user through an experience. Each record page is linked to only one data table.

## Before you begin

Role required:

-   admin or Guided Application Creator for ServiceNow Studio.
-   sn\_app\_eng\_studio.user or delegated\_developer for AES. For more information, see [Delegate developers using AES](../concept/aes-app-dev-workflow.md).

## About this task

Components are the building blocks of your page. Add components to your page to build or customize your workspace experience. For example, add a button component to your page that lets users submit requests.

A container is a type of component that can contain other components. Containers have layout properties applied to them. Change the page layout and visual styling to make the record page a unique experience.

**Note:** Starting with workspaces built after the AES Workspace UI Template v22.0.3 release, you can work with record pages in Workspace Builder. For older workspaces, you must edit the record pages in UI Builder.

If you don't see the record page for a table you configured for the workspace, see [this Knowledge article](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1571345) for more information.

## Procedure

1.  Navigate to Workspace Builder.

    For details on how to open Workspace Builder in ServiceNow Studio or AES, see [Accessing Workspace Builder](../../workspace-builder/concept/accessing-workspace-builder-aes-crs.md).

2.  Create a record page.

    AES automatically generates record pages for the tables that you selected when you created the workspace.

    1.  In the Workspace Builder header, from the **Record pages** menu, select **+ Create new**.

        ![Workspace tab open with Record pages menu expanded showing the create new option.](../image/wb-create-record-page2.png)

    2.  On the form, fill in the fields.

<table id="table_slr_sxs_l5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Brief name that identifies the purpose of the record page.

</td></tr><tr><td>

Table

</td><td>

Table that the record page is linked to and updates.The following rules apply:

-   If you're using a table that you or someone at your organization created, the table must contain at least one new field or column. Otherwise, the form view and the record for the table can't be created.
-   You can link each table to only one record page.
You can select from two sections: Tables that are already available in your app, and all tables outside the app scope.

</td></tr></tbody>
</table>    3.  Select **Create**.

    The page appears in the preview panel. You can select the page from the **Record pages** menu.

3.  Edit the record details for the record page.

    1.  In the navigation panel, select **Record details**.

        ![Record page details](../image/wb-record-page-details-purple.png)

    2.  In the **Form details** section of the configuration panel, select **Edit form** and fill in the fields.

        ![Configuration panel with form details section highlighted.](../image/wb-create-record-page4.png)

<table id="table_jjk_wbt_l5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Form details

</td><td>

Select the **Edit form** link to edit the form in a Table Builder tab inside AES.**Note:** After you leave the record page in the Table Builder tab, a dialog prompts you to **Reload this page**.

For more information on editing forms for a record page, see [Forms in Table Builder](../../../administer/form-builder/concept/form-view-configuration.md).

</td></tr><tr><td>

Activity stream

</td><td>

Option to enable the Activity stream for the record page. The Activity stream enables your workspace users to communicate with requesters and make internal notes about the work done on a record. For more information on the Activity stream, see [Activity streams](https://www.servicenow.com/docs/access?context=c_activity-streams&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

</td></tr></tbody>
</table>4.  Configure the related information in the Related information section of the configuration panel for the record page.

    Related information includes tables that are related to the record, which appear as tabs, such as Child Incidents. For more information on configuring related information, see [Related lists](https://www.servicenow.com/docs/access?context=c_RelatedLists&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

    **Note:** You can't create a table for the related information in a record page. The table must exist in ServiceNow AI Platform.

    1.  If no related lists exist yet, add a new related list by selecting **+ Add tabs** in the **Releated information** section.

        ![Configuration panel with related information section highlighted](../image/wb-create-record-page5.png)

        If related lists exist for the record page, select the **Manage related information** link in the configuration panel.

    2.  In the form that appears in a new tab within AES, move the related list that you want to appear as a tab from the **Available** panel to the **Selected** panel.

    3.  Use the arrow buttons to move the selected lists into the order you want them to appear.

    4.  Select **Save** and return to the Workspace Builder tab within AES.

    5.  View the changes that you made by selecting **Reload this page** in the dialog box that appears.

    Each related information component has an information icon \(![Information icon](../image/icon-information.png)\) that, when selected, displays its related table.

5.  Provide fulfillers with visibility into cross-business workflows and the actionable tasks used to complete these workflows by specifying the playbook.

    For more information on playbooks, see [About Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-ui&version=australia&pubname=australia-build-workflows&ft:locale=en-US).

    **Note:** You must have the Playbook Experience plugin installed.If you used a template to create the app, you can't add a playbook to the record page. For details on how to add a playbook for workspaces created from templates, see [this knowledgebase article](https://support.servicenow.com/kb?id=kb_article_view&sys_kb_id=13fd98de1bfd6510a4de35df034bcbce).

    1.  In the Playbook section of the configuration panel, select **Add a playbook**.

    2.  On the form, fill in the fields.

<table id="table_ebw_ddk_55b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Tab name

</td><td>

Label for the record tab that contains the playbook.

</td></tr><tr><td>

Playbook experience

</td><td>

Existing playbook to add to the record.**Note:** You can choose only from the playbooks that are available for the table.

</td></tr></tbody>
</table>    3.  Select **Add**.

    4.  Update the playbook by selecting the settings icon \(![Icon to edit playbook settings](../image/wb-settings-icon-2.png)\), making the change, and then selecting **Update**.

        **Note:** If you want to make additional changes to the playbook, you must open and edit the playbook in Playbooks.

    5.  Delete a playbook from the workspace by selecting its delete icon \(![Icon to delete a playbook from a workspace](../image/wb-delete-icon-2.png)\) and selecting **Delete** on the confirmation dialog.

6.  Configure the contextual side panel for the record page, which contains the icons for the tools that appear on the right side of the page.

    The contextual side panel contains icons that enable agents to research and resolve issues using various ServiceNow AI Platform tools. If your organization created any custom right tab components in UI Builder, you can add them as well..

    **Note:** If you used a template to create the app, you can't add a contextual side panel to the record page.

    1.  In the navigation panel for the record page, select **Contextual side panel**.

        ![Contextual side panel for a record page](../image/wb-contextual-side-panel-purple.png)

    2.  In the **Context side panel settings**, select the toggle switch for each component and ribbon component that you want to appear on the record page.

        For example, you can include Agent assist and attachments for the record. Attachments and templates are enabled by default, though you can disable them by deselecting their toggle options.

        To see the ribbon components, set the **Ribbon** component toggle to on.

        ![Ribbon component selected in settings](../image/wb-create-record-page6.png)

        To add pre-existing custom components, edit the workspace in UI Builder.

<table id="table_hbg_x3t_s5b"><thead><tr><th>

Tool

</th><th>

Type

</th><th>

Description

</th><th>

More information

</th></tr></thead><tbody><tr><td>

Active SLA

</td><td>

Ribbon component

</td><td>

Display active Service License Agreements \(SLAs\) for the case, including time remaining, the SLA state, and any breaches.

</td><td>

[SLA ribbon](https://www.servicenow.com/docs/access?context=csm-agent-workspace-ribbon&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

</td></tr><tr><td>

Attachment

</td><td>

Component

</td><td>

Add attachments to the record, such as images and PDFs.

</td><td>

[Attachments](https://www.servicenow.com/docs/access?context=attachments&version=australia&pubname=australia-integrate-applications&ft:locale=en-US)

</td></tr><tr><td>

Configuration Management Database \(CMDB\) Timeline

</td><td>

Ribbon component

</td><td>

Display a chronological summary of case activities, including state changes and interactions between the agent and the requester \(usually the customer\). The ribbon also displays how much time that the fulfiller and requester spent on the case.

</td><td>

[Timeline ribbon component](https://www.servicenow.com/docs/access?context=csm-agent-workspace-ribbon&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

</td></tr><tr><td>

Customer 360

</td><td>

Ribbon component

</td><td>

Display customer information, such as the contact or consumer name, email address, and phone numbers.

</td><td>

[Customer 360 ribbon component](https://www.servicenow.com/docs/access?context=csm-agent-workspace-ribbon&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

</td></tr><tr><td>

Ribbon

</td><td>

Component

</td><td>

Display the contextual side panel ribbon, which contains tools to help agents resolve issues.Ribbon components can have additional components added to them.

</td><td>

[Viewing ribbon information in the contextual side panel](https://www.servicenow.com/docs/access?context=csm-playbooks-viewing-ribbon-info&version=australia&pubname=australia-customer-service-management&ft:locale=en-US)

</td></tr></tbody>
</table>        The selected tools appear in the record page preview canvas.

    3.  In the configuration panel, drag the components to rearrange them.

    4.  Complete any additional configuration for components by selecting the settings icon \(![Settings icon for contextual side panel components](../image/wb-settings-icon-black.png)\).

        For example, Customer 360 requires that you specify additional settings before the component works on the record page.

    Workspace Builder automatically saves the changes to the contextual side panel.

7.  Complete any additional changes and configurations.

<table id="choicetable_f3l_vjr_dvb"><tbody><tr><td id="d246683e925">

**Update the name of the record page**

</td><td>

**Note:** You can't change the table that a record page is linked to after you create the page. To change the table for the record page, you should create a new, separate record page.

 1.  From the Record pages menu, select the page that you want to edit.

A preview of the record page appears.

2.  In the navigation panel, select **Settings**.
3.  In the Record page settings configuration panel that appears, enter the new page name.
4.  Select **Save**.


</td></tr><tr><td id="d246683e960">

**Preview the record page in a new browser tab**

</td><td>

Select **Preview** in the Workspace Builder header.The record page appears in the workspace. If no data exists for the table, AES displays a page where you can add data to the table.

</td></tr><tr><td id="d246683e981">

**Delete a record page**

</td><td>

1.  From the Record pages list, select the page.
2.  In the navigation panel, select **Settings**.
3.  At the bottom of the configuration panel, select **Delete record page**.
4.  On the confirmation dialog, select **Delete**.


</td></tr></tbody>
</table>
