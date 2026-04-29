---
title: CSM Configurable Workspace record pages and page templates
description: Use record pages to display information in CSM Configurable Workspace. Use page templates to create record pages.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [CSM Configurable Workspace, Organize agent workspaces, Configure, Customer Service Management]
---

# CSM Configurable Workspace record pages and page templates

Use record pages to display information in CSM Configurable Workspace. Use page templates to create record pages.

## Record pages

A record page provides the base structure for how a record is displayed in CSM Configurable Workspace. This includes records such as cases, incidents, and tasks.

Record pages include elements such as layouts, containers, and components to display record information. Some record pages leverage additional logic using presets, controllers, and extension points.

Several [record pages](csm-config-workspace-record-pages.md) are included with CSM Configurable Workspace. You can use these record pages as is or you can customize them to suit your needs.

## Record templates

A page template is a blueprint or a model of a record page that displays information in CSM Configurable Workspace. You can use page templates to create new pages or page variants in UI Builder.

Page templates can include components, data resources, extension points, and a layout. When you create a page or a page variant from a page template, you start from a base structure that you can customize to meet your needs.

The Customer Service application includes several [page templates](csm-config-workspace-page-templates.md) that you can use to create pages.

## Workspace record page interoperability

Enable agents to use record pages between CSM Configurable Workspace and ITSM Service Operations Workspace \(SOW\). The following ITSM pages are interoperable across CSM:

-   Incident page
-   Change page

These ITSM pages are inactive by default. Users with the system administrator role can enable these pages as needed:

1.  Navigate to the UX Cross-experience routes list \(sys\_ux\_interoperable\_route\_list.do\).
2.  Select **SOW Incident and change Page use**.
3.  Enable the page for editing and select the **Active** check box.
4.  Select **Update** to save the changes.

