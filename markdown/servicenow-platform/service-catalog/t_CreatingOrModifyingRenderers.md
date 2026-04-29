---
title: Create a renderer
description: Create or modify renderers using UI macros to provide the rendering instructions. Renderers define a specific look and feel for a catalog or category.Select a renderer and apply them to a catalog to change its appearance.Select a renderer scheme for your categories.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service catalog home page configuration, Service Catalog customization, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create a renderer

Create or modify renderers using UI macros to provide the rendering instructions. Renderers define a specific look and feel for a catalog or category.

## Before you begin

Role required: catalog\_admin or admin

## About this task

Use renderers to specify the following formats:

-   How catalogs appear on the multi-catalog homepage.
-   How categories appear on a catalog homepage.

For example, you can create a renderer showing the category homepage image, the description, and the first two catalog items in a category.

## Procedure

1.  Create a UI macro to define specific rendering instructions.

2.  Navigate to **Service Catalog** &gt; **Catalog Definition** &gt; **Renderers**.

3.  Click **New**.

4.  Select to create a catalog or category renderer.

5.  Enter the renderer details.

<table id="table_ykt_32d_jp"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A name for the renderer.

</td></tr><tr><td>

Macro

</td><td>

The UI Macro to use.

</td></tr><tr><td>

Render catalog title

</td><td>

Appears for catalogs renderers. A check box to display the catalog title bar on the multi-catalog homepage.

</td></tr><tr><td>

Render title

</td><td>

Appears for category renderers. A check box to display the category title bar on the catalog homepage.**Note:** The **admin** and **catalog\_admin** roles can view the **Render title** even when the check box is not selected.

</td></tr></tbody>
</table>    ![Screenshot for catalog renderers](../image/ServiceCatalogRenderers.png "Service Catalog Renderers")

6.  Click **Submit**.

    **Note:** To modify a default catalog or category renderer, follow a similar process, by selecting one of the default renderers listed.

    This new renderer is added to the list of available choices when applying a renderer.


**Parent Topic:**[Service catalog home page configuration](../concept/c_ManagingTheHomepageForACatalog.md)

## Select a renderer for a catalog

Select a renderer and apply them to a catalog to change its appearance.

### Before you begin

Role required: catalog\_admin or admin

### About this task

The following default catalog renderer schemes are available:

-   **All Details**: shows desktop image, title, and categories.
-   **Image Only**: shows desktop image only.
-   **Title and Image**: shows title and desktop image.
-   **Title Only**: shows title only.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalogs**.

2.  Click the add content icon \(+\) on the upper right.

3.  Select a catalog in the middle panel of the pop-up window.

    ![](../image/ServiceCatalogMultiCatalogHomePageArrange.png "Service Catalog home page layout")

4.  Select a renderer from the list displayed in the right-hand panel, for example **Title Only**.

5.  Click **Close** to save the catalog with the renderer settings you defined.


## Select a renderer for a category

Select a renderer scheme for your categories.

### Before you begin

Role required: catalog\_admin or admin

### About this task

The following default category renderer schemes are available:

-   **Category Items**: shows desktop image, title, and description.
-   **Category Items No Title**: shows desktop Image and description.
-   **Category Details**: shows the subcategories and items in that category.

### Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog**.

2.  Click the add content icon \(+\) on the upper right.

3.  Select a category in the middle panel of the pop-up window.

4.  Select a renderer from the list displayed in the right-hand panel, for example **Category Items**.

5.  Click the close icon \(x\) to save the catalog with the selected renderer.


