---
title: Migrate the contextual side panel
description: The contextual side panel in CSM Configurable Workspace is built in UI Builder and isn't carried over from CSM Agent Workspace. Review what agents needed in CSM Agent Workspace and rebuild the panel to meet those needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/migration-contextual-side-panel.html
release: australia
topic_type: task
last_updated: "2026-10-25"
reading_time_minutes: 2
breadcrumb: [Migrate to CSM Configurable Workspace, Migrating to CSM Configurable Workspace, CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# Migrate the contextual side panel

The contextual side panel in CSM Configurable Workspace is built in UI Builder and isn't carried over from CSM Agent Workspace. Review what agents needed in CSM Agent Workspace and rebuild the panel to meet those needs.

## Before you begin

Role required: admin

-   Review what agents accessed in the CSM Agent Workspace side panel and identify the information they needed most often. Focus on information that would otherwise take agents out of the workspace, rather than replicating every tab.
-   Plan which tabs each record type needs. For example, the case page may need different tabs from the interaction page.
-   Decide whether the side panel should be enabled or disabled for specific types of case forms.
-   If you're using a predefined record page, create a record page variant first. You can't add tabs directly to a predefined page. For more information, see [Creating pages and page variants](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-ws-create-page-variant.md).

## About this task

The contextual side panel gives agents quick access to tools and information without leaving the record page. It can contain search results, recommended actions, attachments, templates, and tabs that you configure for your organization. The side panel agents see in CSM Configurable Workspace depends entirely on what you configure.

## Procedure

1.  Navigate to **All** &gt; **Now Experience Framework** &gt; **UI Builder**. On the **Experiences** tab, select **CSM/FSM Configurable Workspace**.

2.  Open the record page that you want to configure, such as the CSM default record page.

3.  Select the Tab Sidebar component in the editor, or locate it in the left navigation menu.

4.  Select **Add Tab** and choose how to build the tab content.

    -   Start from an empty container and build the tab from scratch using components from the component library.
    -   Use a repeater to display a list of items from a related table.
    -   Display related information for a record from other tables.
    -   Add a page collection to extend the tab using content that already exists as a page in UI Builder.
5.  Configure the tab name, the content, and any conditions that control when the tab is visible.

6.  Optional: To rearrange tabs, select a tab in the Tab Sidebar and drag it to the position you want.

7.  Select **Save**.


## What to do next

To hide specific tabs from the side panel for certain tables, use the **inlineTabExclusion** UX page property. For more information, see [Hide tabs in the contextual side panel](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/config-csm-ws-side-panel-tabs.md).

