---
title: Rich Content Editor
description: Rich Content Editor enables content managers and admins to create HTML-based content for the Employee Center Pro topic and portal pages using a visual drag-and-drop interface.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/employee-service-management/employee-experience-foundation/ec-rich-content.html
release: xanadu
product: Employee Experience Foundation
classification: employee-experience-foundation
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Content Library, Creating employee communications with Content Publishing, Manage, Employee Center, Employee Service Management]
---

# Rich Content Editor

Rich Content Editor enables content managers and admins to create HTML-based content for the Employee Center Pro topic and portal pages using a visual drag-and-drop interface.

You can create a layout, add components \(such as containers, images, videos, and links\), and adjust the settings of the components with little or no HTML or CSS \(cascading style sheets\) knowledge. The Rich Content Editor allows non-technical users to build sections of pages without the help of IT or technical users.

The Rich Content Editor provides a library of components and a canvas area, where you use drag-and-drop method to create your content. The components can be edited individually and you can preview what you are creating on a desktop, tablet, or mobile device before you make your content available to your audience.

Creating content does not interfere with your portal theme or color. Published content that does not use custom style changes uses the theme of the underlying portal page.

**Note:** By default, the **Rich Content Editor** uses the **sn\_cd.preview.portal\_url\_suffix** sys property to determine the portal theme to use for the content you create. Using the preview portal when creating rich content reflects the portal theme to provide an example of how the content will appear. For more information, see [Properties installed with Content Publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/properties-with-content-delivery.md).

## Rich Content Editor interface

The Rich Content Editor interface is comprised of a canvas where you assemble the content, content components that you drag-and-drop into the canvas, and menu bar icons to modify the canvas.

**Note:** If the Edit Source code icon does not appear, ask an admin to enable the **Edit code** property. See [Properties installed with Content Publishing](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/properties-with-content-delivery.md)

\[Omitted image "ec-rce-components.png"\] Alt text: Rich Content Editor components

When you select a component, a toolbar appears at its top-left corner, allowing you to manipulate the component directly. Each component offers a variety of customization options that are accessed from the **Settings** tab.

\[Omitted image "ec-rce-settings.png"\] Alt text: Rich Content Editor - Settings

## Using the Rich Content Editor

The Rich Content Editor makes it possible to build HTML content with little or no HTML or CSS \(cascading style sheets\) knowledge, using the following process:

1.  Create the Rich Content type record: [Create rich content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/ec-content-library-portal-rich-content.md)
2.  Create the page layout.
    -   Modules are predefined content layouts comprised of header, paragraph text, and images. See [Add predefined content layouts with the Rich Content Editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/add-modules-rich-content-editor.md)
    -   Columns are containers that enable you to define a custom layout. See [Add columns with the Rich Content Editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/ec-rich-content-canvas.md)
3.  Add components such as images, videos, text boxes, and buttons.
4.  Change the canvas size to create content for tablet and mobile.

    **Note:** For best results when creating content for all three platforms, first create your content for desktop, then tablet and mobile.

5.  \(Optional\) Select a different language to view your session in or request a language translation for the content you are creating. For more information, see [Configuring translation for Content Publishing after upgrade](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/ec-multiple-language-support.md).

    **Note:** Only translate content after you have completed creating and formatting the content. To create content with format that varies across translations, duplicate the content for each language and format it, then perform the translation.

6.  Make the content available to users via a publish plan: [Create a publish plan for your content](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/ec-content-library-publish2.md)

    Alternatively, you can build out a more robust publishing configuration using [Creating campaigns with Content Experiences](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/employee-service-management/employee-experience-foundation/ecpro-campaigns.md)


## Keyboard shortcuts

You can assemble rich content and news articles in the Rich Content Editor using a keyboard for improved accessibility.

The Rich Content Editor supports many operating system and text formatting shortcuts, including Save, Bold, and Undo. You can use these additional keyboard shortcuts to support your content creation.

|Action|Mac keyboard shortcut|Windows keyboard shortcut|
|------|---------------------|-------------------------|
|Paste and match style of selected text box|Shift+Option+Command+V|Shift+Alt+Windows+V|

**Tip:**

With the Rich Content Editor, you can easily use your keyboard to select individual canvas components. You can add text and columns, create text sections within those columns, and update headings within each section to adjust the styling and fonts to your liking; It helps you customize your content in a simple and convenient way.

## Rich content in portal search

When employees enter a keyword in the global search bar, Employee Center uses AI Search to return published pages containing that keyword in the content name or body.

\[Omitted image "ec-rich-content-search.png"\] Alt text: Searching for by keyword "employee" returns pages created with the rich content editor containing the term

If the user with the system admin or content admin role uses the global search bar, the results include unpublished pages.

