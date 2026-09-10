---
title: Pages, templates, and components
description: Pages, templates, and components work together to build the Configurable Workspace experience. Understanding how they relate helps administrators design a playbook that works for their users.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-07-14"
reading_time_minutes: 2
keywords: [playbook pages, playbook templates, playbook components, layouts]
---

# Pages, templates, and components

Pages, templates, and components work together to build the Configurable Workspace experience. Understanding how they relate helps administrators design a playbook that works for their users.

A **page** provides the layout that a user sees when they open a record — any type of record, whether it's a case, work order, or other record type. A **page template** is a predefined blueprint for creating pages, with playbook components already configured. **Components** are the individual objects placed on a page that display information or provide functionality — such as the activity stream, contextual side panel, or related items. Components are included in templates and in any record pages that are created from those templates or from scratch.

When you activate a page template in UI Builder, it creates the page structure and includes the configured components. You can then customize both the page layout and individual components to match your organizational needs. This flexibility lets you tailor the experience. Different users might see different sets of components based on their role or the record type they're working with.

When configuring record pages, administrators have three options:

-   Use a template as-is, without changes
-   Save a template and modify it as needed
-   Create a new page from scratch

## Playbook pages

A playbook page is the record page a user sees when they open a record with a playbook attached. It controls the overall layout — which components are visible, what appears in the header, and how the contextual side panel is structured. Pages are activated and configured in UI Builder.

Because different audiences interact with the same playbook in different ways, different pages can be configured for different personas. A requester on a portal or embeddable gets a simplified, guided layout. A fulfiller agent in the workspace gets a richer page with more tools, components, and actions available.

For configuration topics, see the Pages, templates, and components section in the sidebar.

## Playbook page templates

Page templates are starting points for creating record pages. Each template comes with the necessary playbook components already in place, so a template can be used as-is out of the box, or used as the basis for a customized page. The horizontal and vertical stages record pages are both predefined templates.

When it comes to setting up a record page, an administrator can apply a template exactly as it comes, save a copy and adjust its components and layout, or set the templates aside and build a page from scratch.

Just as with pages, templates can be selected and customized based on the persona accessing them — a different template can be used for a requester on a portal than for a fulfiller agent in the workspace.

## Playbook components

Components are the individual building blocks that appear within a playbook page. Each component serves a specific function in Configurable Workspace. Components come with the playbook page templates by default and are not fixed — using UI Builder, an administrator can remove any of them, rearrange them, or create a custom page layout for a playbook record page.

For the full list of playbook components and what each one does, see.

## Layouts

Pages and templates are arranged using layouts, which control how a playbook's stages and activities appear on the page. The same page can be presented in more than one way depending on the layout applied to it. The main layouts are:

-   **Horizontal layout:** stages run across the top of the page.
-   **Vertical layout:** stages run down the side of the page.

