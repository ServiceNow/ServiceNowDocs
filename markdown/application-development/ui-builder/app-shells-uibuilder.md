---
title: Define UI experiences using app shells
description: Understand what app shells are, what app shells are available for UI Builder, and why you would pick one over another.
locale: en-US
release: australia
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure how users interact with your applications in UI Builder, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Define UI experiences using app shells

Understand what app shells are, what app shells are available for UI Builder, and why you would pick one over another.

## App shells

An app shell is the wrapper of the contents of an experience page. An app shell includes functionality similar to a web page. For example, an app shell can show things in a header or footer of your experience, such as a logo for your company, user preferences, a search icon, configuration icon, user menu, and so on.

An app shell is required for UI Builder.

The app shell defines whether your experience has a workspace or portal design. A workspace is a graphical user interface that puts multiple tools on one page for handling requests from users. A portal is a page where users can add requests, such as order items, track their tickets, and so on.

You choose which app shell to apply to your experience when you create an experience in the ServiceNow® platform. For more information on how to create an experience, see [Configure how users interact with your applications in UI Builder](work-experiences.md).

You can choose from various app shells when creating an experience.

![List of the app shells available when creating a new experience.](../image/app-shells-available.png)

|App shell|Description|Example|
|---------|-----------|-------|
|Breadcrumb app shell|The breadcrumb app shell includes a header, breadcrumb style navigation, and a primary navigation bar for a workspace experience. Use the breadcrumb app shell for focused workflows and wizard flows that don't require multi-tasking.| |
|Header app shell|The header app shell includes a header and user menu for a workspace experience. Use the header app shell for experiences that require minimal navigation and few actionable items in the header.| |
|Portal app shell|The portal app shell includes the header and footer for a portal experience. The portal app shell record is a reference implementation of how the menu, utilities, logo, and login are configured for a portal experience.|![Experience created with portal app shell.](../image/app-shell-portal.png)|
|UXR Base Experience app shell|The UXR Base Experience shell creates an experience with the Next Experience banner. The UXR Base Experience shell provides base functionality support for experiences that are configured within a parent app, including experience configuration, context binding, routing, screen loading, and caching. The UXR Base Experience shell has no visual or experience-specific components. The UXR Base Experience shell can also be used for experiences that have no shell customization. For example, Identity Center directly uses UXR Base Experience Shell as its app shell.| |
|Workspace app shell|The workspace app shell includes the headers and footers for a workspace experience. Use the workspace app shell to provide tools that users need to find, research, and resolve issues. To manage the visual style of experiences created with this app shell, see Configuring Next Experience with Theme Builder.| |

**Parent Topic:**[Configure how users interact with your applications in UI Builder](work-experiences.md)

