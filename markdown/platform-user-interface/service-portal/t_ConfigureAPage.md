---
title: Create and edit a page using the Service Portal Designer
description: Create or edit a page and use layouts to organize the columns that house the widgets.Select a container record to serve as a page subheader. A subheader sticks to the page header and does not scroll.Include font icons on a page so that all the widgets on the page have access to the font-icon set.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: task
last_updated: "2026-04-22"
reading_time_minutes: 8
breadcrumb: [Creating portal pages, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Create and edit a page using the Service Portal Designer

Create or edit a page and use layouts to organize the columns that house the widgets.

## Before you begin

Role required: sp\_admin or admin

## About this task

These steps are intended for users with little to no coding experience. The Service Portal Designer includes several layers of customization from simply adding widgets in a particular configuration on a page, to adding CSS classes.

## Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  Switch to the portal you want to design pages for by selecting the portal name in the header.

    ![Service Portal Designer header with the portal name SP highlighted](../image/DesignerSwitchPortal.png)

4.  From the Service Portal Designer, select a page to customize or select **Add a new page**.

5.  Under Layouts, select **Container** and drag it onto the page.

6.  Drag one of the other layouts and drop it in the container.

    This layout defines the structure of your page and the space available to drop widgets. The structure of the layout aligns with the Bootstrap grid template and adds up to 12.

7.  Use the filter to search for a widget, then drag the widget to the layout.

    ![Gif showing how to drag containers, layouts, then widgets onto a page](../image/ConfigurePage.gif "Drag containers, layouts, then widgets onto a page")

    For widgets that do not contain any information by default, you must configure the options for their widget instances before they will appear on a portal page. For more information about configuring widget instance options, see [Configure widget instances](../concept/c_ConfigureWidgetInstances.md).

8.  Edit page properties.

    1.  Select **Edit Page Properties**.

        The page record from the Pages table \[sp\_page\] opens.

    2.  Edit the form.

<table id="table_ygl_qdt_3z"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Internal name of the page. Use the title to search for a page in the Service Portal Designer.

</td></tr><tr><td>

ID

</td><td>

A unique ID for the page. The ID is what you use to assign a page to a portal. It also determines the URL for the page, for example `https://instance name.service-now.com/doc_portal/?id=doc_page`, where doc\_page is the page ID.

</td></tr><tr><td>

Application

</td><td>

The application scope.

</td></tr><tr><td>

Public

</td><td>

Enables the page to be accessed without the need for authentication. If **Public** is selected, all users can view the page no matter the roles listed.

</td></tr><tr><td>

Draft

</td><td>

Mark a page as draft to limit user ability to view the page while you’re still creating it. Only users with the admin role can view a page in draft, all other users see a 404 page.

</td></tr><tr><td>

Roles

</td><td>

Limit user access to a page by role.

</td></tr><tr><td>

Short description

</td><td>

Describes the portal page. This field isn’t public facing.

</td></tr><tr><td>

Page Specific CSS

</td><td>

Unless a page has Page Specific CSS, the page inherits CSS from the Theme and Branding. If you need a page to look different, the Page Specific CSS overrides the inheritance from the Theme and Branding.

</td></tr><tr><td>

Dynamic page title

</td><td>

Create variables to generate descriptive titles depending on the content loaded into a page.

 For more information, see [Add dynamic titles to a page](add-page-title.md).

</td></tr><tr><td>

Clone Page

</td><td>

Enables you to make a copy of a page that can be modified. If you copy a base system page, a new widget instance is created for each widget on the page.

</td></tr><tr><td>

Use SEO script

</td><td>

Option to enable a script include that adds SEO tags for canonical URLs and hreflang tags.

 For more information, see [Enable SEO for localized versions of a portal page](seo-header-tags.md).

</td></tr><tr><td>

SEO script

</td><td>

Script include to apply to the page. By default, the system uses the SPSEOHeaderTags script include, which includes the default implementation for the canonical URL and hreflang tags for Service Portal Analytics pages.

</td></tr><tr><td>

Human readable URL structure

</td><td>

Add human readable keywords to the page URL to improve search engine optimization \(SEO\) and click-through rates for public pages. Human readable URLs also help users understand what to expect on a page for public and non-public pages. For example, `https://<instance>/kb/en/faq/what-is-a-cookie?id=kb_article_view&sysparm_article=KB0000007`.

 For more information, see [Add human readable keywords to page URLs](add-human-readable-keywords-page-urls.md).

</td></tr></tbody>
</table>9.  Edit container properties.

    1.  Select within the container you would like to edit, or select **Container** in the breadcrumbs.

    2.  Select the edit icon \[![Edit icon](../image/IconEditOption.png)\].

        The container record from the Containers table \[sp\_container\] opens.

    3.  Edit the form.

<table id="table_evm_ng4_qbb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Internal name of the container.

</td></tr><tr><td>

Order

</td><td>

The order in which the containers appear on a page. To set a container to appear above all other containers, give the container the lowest number in the **Order** field.

</td></tr><tr><td>

Page

</td><td>

The page that includes the container.

</td></tr><tr><td>

Screen reader title

</td><td>

The title used by a screen reader.

</td></tr><tr><td>

Semantic tag

</td><td>

The semantic HTML tag that includes the container. Options include:-   None: All content on the page between the header and footer is included in the **&lt;main&gt;** tag.
-   Main: The **&lt;main&gt;** tag includes only the container and its contents. The **&lt;main&gt;** tag is a semantic HTML element that contains the main content of the page. It should be applied to content that is unique to the page and should be configured for only one element on the page.

**Note:** The **&lt;main&gt;** tag can be applied to a container, row, or column. For more information, see [Configure the main tag on a page](configure-main-tag-on-page.md).

-   Header: The &lt;header&gt; tag is used as introductory content. It can be used multiple times per page, including inside an &lt;article&gt; tag.
-   Nav: The &lt;nav&gt; tag is used in page-level navigation. It can be used multiple times in each page.
-   Section: The &lt;section&gt; tag groups related content under a common heading or theme.
-   Article: The &lt;article&gt; tag is self-contained content that can stand alone or be reused.
-   Details: The &lt;details&gt; tag can be used in expand/collapse sections, and intended for FAQs.
-   Summary: &lt;summary&gt; tag is the first child of &lt;details&gt; and acts as the clickable label.
-   Time: &lt;time&gt; tag is for dates, times, and durations. Add for machine-readable values.
-   Fig caption: &lt;figcaption&gt; tag is only valid as a child of &lt;figure&gt; and provides the caption for a figure.


</td></tr><tr><td>

Application

</td><td>

The application scope.

</td></tr><tr><td>

Width

</td><td>

Width of the container. Options include: -   Fixed
-   Fluid


</td></tr><tr><td>

Parent class

</td><td>

Parent CSS class for the container.

</td></tr><tr><td>

CSS class

</td><td>

The CSS classes for the container. Overwrites page-specific CSS.

</td></tr><tr><td>

Background color

</td><td>

The background color of the container.

</td></tr><tr><td>

Background image

</td><td>

Background image for the container.

</td></tr><tr><td>

Background style

</td><td>

The display style of a background image. Options include: -   Default
-   Cover
-   Contain
-   Repeating


</td></tr><tr><td>

Bootstrap alternative

</td><td>

Selecting this field removes the standard Bootstrap grid classes and disables the Bootstrap grid system in the container. If selected, the following aren’t applied: -   The **Width** field in the container record.
-   Standard Bootstrap class in the row record within the container.
-   The **Size - xs**, **Size - sm**, **Size - md**, and **Size - lg** fields in column records within the container.
 Only select this field if you plan to provide custom CSS classes and CSS for the container, row, and column records.

</td></tr><tr><td>

Move to header

</td><td>

When selected, the container sticks to the header and doesn’t scroll. Use this option to create a subheader.

</td></tr></tbody>
</table>10. To switch to a different page, select the **Pages** tab in the left pane, then select the next page you want to configure.

11. Use the Preview button in the header to view your page as you design it.

    You can also use **Preview** to view your page in mobile or tablet mode through the controls presented in the header.

    ![Page preview with the iPad view mode selected.](../image/DesignerIPadView.png "Designer tablet view")


**Parent Topic:**[Creating portal pages](../concept/c_Pages.md)

## Add a subheader to a page

Select a container record to serve as a page subheader. A subheader sticks to the page header and does not scroll.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Service Portal Configuration**.

2.  Select **Designer**.

3.  Select a page.

4.  Switch to the portal you want to design pages for by selecting the portal name in the header.

    ![Service Portal Designer header with the portal name SP highlighted](../image/DesignerSwitchPortal.png)

5.  Select the container that you would like to use as a subheader, or select the container using the breadcrumbs.

6.  Select the edit icon \(![Edit icon](../image/IconEditOption.png)\).

7.  Select **Move to header**.


### Result

As a subheader, the container sticks to the header and does not scroll.

## Include font icons on a page

Include font icons on a page so that all the widgets on the page have access to the font-icon set.

### Before you begin

Role required: sp\_admin or admin

### Procedure

1.  Navigate to **All** &gt; **Service Portal** &gt; **Pages** and click the page you want to add font icons to.

2.  Attach the font-icon file to the page record.

3.  In the Page Specific CSS field for the page, add the CSS for the font-icon definition.

    Use the sys\_id of the attachment as the src in the CSS. For example:

    ```
    /* fallback */
    @font-face {
      font-family: 'Material Icons';
      font-style: normal;
      font-weight: 400;
      src: url('/828b8ca8b7033010897725cbde11a9f7.iix') format('woff2');
    }
    
    .material-icons {
      font-family: 'Material Icons';
      font-weight: normal;
      font-style: normal;
      font-size: 24px;  /* Preferred icon size */
      display: inline-block;
      line-height: 1;
      text-transform: none;
      letter-spacing: normal;
      word-wrap: normal;
      white-space: nowrap;
      direction: ltr;
    
      /* Support for all WebKit browsers. */
      -webkit-font-smoothing: antialiased;
      /* Support for Safari and Chrome. */
      text-rendering: optimizeLegibility;
    
      /* Support for Firefox. */
      -moz-osx-font-smoothing: grayscale;
    
      /* Support for IE. */
      font-feature-settings: 'liga';
    }
    ```


### Result

You can select an icon from the icon set for any widget on this page. For example, in the HTML widget you can use the **Source Code** option to use an icon. For example:

`<p style="text-align: center;"><em class="material-icons">flight_land</em></p>`

