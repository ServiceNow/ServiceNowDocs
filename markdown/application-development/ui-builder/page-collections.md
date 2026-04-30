---
title: Page collections
description: Page Collections are groups of pages that can be used across multiple experiences.
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Customize UI Builder pages using components, Working in UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Page collections

Page Collections are groups of pages that can be used across multiple experiences.

## What is a page collection

Page Collections \(sys\_ux\_extension\_point\) are groups of pages that are meant to be re-used across multiple experiences. These sets of pages can be used in a modal viewport or in a tabs component. These pages are sandboxed and do not have access to things like URL params or data resources from the page that is calling them. All they have access to is the Controller record that is specified on the Page Collection record and that is passed down by the calling page in runtime.

Page collections are sandboxed inside of the pages they are within, this means that they do not have direct access to change the parent page. However, because of the way seismic works, your page collection page can dispatch an event that the calling page can listen for to take action. This is the only way to achieve a change in the calling page.

!['List page modals' page collection with several variants displayed.](../image/page-collection-example.png)

## Why should you use page collections

Page collections allow you to reuse custom pages across experiences. This will save you time if you need to replicate a page for multiple experiences and help pass information to different groups of users.

You can also use page collections to provide additional information within an existing topic by using a viewport modal. A viewport modal will allow your audience to view pages outside of their experience to make changes without leaving the parent page.

Create collection of tabs that can be shared across experiences. Each tab is an individual page in a page collection.

## Where can you use page collections

You can access a page collection from the UI Builder home screen. The list of page collections details which component and type each page collection is.

You can create a page collection from the UI Builder home screen, or from a component that uses page collections.

Page collections can be used with the following components:

-   Viewports
-   Viewport Modals
-   Tabs

## Things to consider

The page collection creation screen requires a component and controller selection.

Data resources need to be selected to pass information to a page collection. Need to bind data from the parent page.

Need to route to the page in a page collection you want to display in a viewport.

Add a link to creating a page collection.

## Page collection on the platform

You create a page collection within the ServiceNow platform. At this time, only the Tab and Viewport component can be used when creating a page collection. You can select a controller or pass controller dependencies using JSON.

![New record for page collection on the platform.](../image/page-collection-platform-form.png)

-   **[Create a page collection across multiple UI pages](../task/create-page-collection.md)**  
Create a page collection to accommodate tabbed content that can be used across experiences.

**Parent Topic:**[Customize UI Builder pages using components](work-components.md)

