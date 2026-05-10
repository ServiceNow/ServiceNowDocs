---
title: Microsites
description: Rich Content Editor enables content managers and admins to create HTML-based content for the Employee Center Pro topic and portal pages using a visual drag-and-drop interface.
locale: en-US
release: australia
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Creating employee communications, Authoring and managing employee communications, Employee Center Pro, Unified Employee Experience, Employee Service Management]
---

# Microsites

Rich Content Editor enables content managers and admins to create HTML-based content for the Employee Center Pro topic and portal pages using a visual drag-and-drop interface.

You can create a layout, add components \(such as containers, images, videos, and links\), and adjust the settings of the components with little or no HTML or CSS \(cascading style sheets\) knowledge. The Rich Content Editor allows non-technical users to build sections of pages without the help of IT or technical users.

The Rich Content Editor provides a library of components and a canvas area, where you use drag-and-drop method to create your content. The components can be edited individually and you can preview what you're creating on a desktop, tablet, or mobile device before you make your content available to your audience.

## Overview of building microsites

The Rich Content Editor makes it possible to build HTML content with little or no HTML or CSS \(cascading style sheets\) knowledge, using the following process:

1.  Create the Rich Content type record: [Create rich content](../task/ec-content-library-portal-rich-content.md)
2.  Create the page layout.
    -   Modules are predefined content layouts comprised of header, paragraph text, and images. See [Add predefined content layouts with the Rich Content Editor](../task/add-modules-rich-content-editor.md)
    -   Columns are containers that enable you to define a custom layout. See [Add columns with the Rich Content Editor](../task/ec-rich-content-canvas.md)
3.  Add components such as images, videos, text boxes, and buttons.
4.  Change the canvas size to create content for tablet and mobile.

    **Note:** For best results when creating content for all three platforms, first create your content for desktop, then tablet and mobile.

5.  \(Optional\) Select a different language to view your session in or request a language translation for the content you're creating. For more information, see [Multilingual support in the Content Library](ec-switch-language.md).
6.  Make the content available to users via a publish plan: [Create a publish plan for your content](../task/ec-content-library-publish2.md)

    Alternatively, you can build out a more robust publishing configuration using campaigns: [Creating campaigns](ecpro-campaigns.md)


## Rich Content Editor interface

The Rich Content Editor interface is comprised of a canvas where you assemble the content, content components that you drag into the canvas, and menu bar icons to modify the canvas.

**Note:** If the Edit Source code icon does not appear, ask an admin to enable the **Edit code** property. See [Properties installed with Content Publishing](../reference/properties-with-content-delivery.md)

![Rich Content Editor components](../images/ec-rce-components.png)

When you select a component, a toolbar appears at its top-left corner, allowing you to manipulate the component directly. Each component offers a variety of customization options that are accessed from the **Settings** tab.

![Rich Content Editor - Settings](../images/ec-rce-settings.png)

## Keyboard shortcuts for accessibility

You can assemble microsites and news articles in the Rich Content Editor using a keyboard for improved accessibility.

The Rich Content Editor supports many operating system and text formatting shortcuts, including Save, Bold, and Undo. In Content Publishing versions 33.0.9 and later, users can navigate the top toolbar and style manager using the right, left, up, and down arrow keys. You can use these additional keyboard shortcuts to support your content creation:

|Action|Mac keyboard shortcut|Windows keyboard shortcut|
|------|---------------------|-------------------------|
|Paste and match style of selected text box|Shift+Option+Command+V|Shift+Alt+Windows+V|

**Tip:**

With the **Rich Content Editor**, you can easily use your **keyboard** to select individual canvas components. You can add text and columns, create text sections within those columns, and update headings within each section to adjust the styling and fonts to your liking; it helps you customize your content in a simple and convenient way.

See [Next Experience keyboard shortcuts](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/next-experience-keyboard-shortcuts.md) for additional information.

## Searching for Rich content

When employees enter a keyword in the global search bar, Employee Center uses AI Search to return published pages containing that keyword in the content name or body.

![Searching for by keyword "employee" returns pages created with the rich content editor containing the term](../images/ec-rich-content-search.png)

AI Search returns additional results based on user roles:

-   Users with either the system admin or content admin role can see unpublished content.
-   For users with the content manager, content admin, or content approver roles, search results include content for which they are not the audience. However, they cannot view the content unless they are part of the configured audience.

**Related topics**  


[Editing source code in the Rich Content Editor](rce-editing-source-code.md)

[Content versioning](ec-content-versioning.md)

[Multilingual support in the Content Library](ec-switch-language.md)

