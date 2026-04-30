---
title: UI Builder glossary
description: Learn about the terms and concepts used in UI Builder \(UIB\).
locale: en-US
release: zurich
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Exploring UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# UI Builder glossary

Learn about the terms and concepts used in UI Builder \(UIB\).

**Parent Topic:**[Exploring UI Builder](create-custom-experience.md)

## action

Actions in UI Builder are specifically activity on a page or within a page component. Events and event handlers are used to add actions. For example, add a button component to a page and then add an event handler to apply an action for the button, such as opening a web page.

## app shell

App shells are the static elements of a web experience \(for example, the header, footer, and menu navigation\) that stays with the end user as they navigate throughout the experience. App shells are primarily used and supported in Workspace and Portal experiences.

## binding

See data binding.

## client script

Client-side JavaScript that interact with components and client state parameters on a page. Client scripts are mapped to events as event handlers in UI Builder.

## client state parameter

Page variables that are defined for a page to store a piece of data \(a client state\) only for that page. For example, create three client state parameters to store the input needed to create a record and specify when to refresh the list. Page variables can be updated using client scripts and events to make a page dynamic.

## component \(UI Builder\)

Components are used in the UI Builder to build pages. Components have an interface that an end user can view and interact with. Components can talk to each other through events and properties. Commonly used components include Heading, Image, List, Form, and Button.

## component id

Used to reference a component when adding a script or binding data to the component. A component ID is automatically created \(based on the component label\) when you add a component to a page, but the component ID can be edited.

## component preset

Presets apply predefined configuration values and event mappings to components. Presets apply prebuilt configurations to component properties and events handlers. Presets are only available for certain components.

## component properties

Available in the Configuration panel and used to configure a component. Each component has unique properties. Component properties are specified within each tab on the Configuration panel: Config, Style, and Event. Some components have presets available. Use the component presets to set component properties automatically.

## controller

A type of data resource that includes data and event logic and enables component presets. Controllers are added automatically when using a page template. There are two types of controllers:

-   Data controllers contain data resources and can be manually added to a page
-   UI controllers are added to pages when using page templates and can't be added manually. Creating controllers isn't supported currently.

## data binding

The process of associating data with a UI element that displays the information.

## data resource

A dynamic, reusable way of defining what data to fetch for a page's components.

## entity view action mapper

Also known as EVAM. Standardizes the format for displaying data in cards and lists.

## event \(UI Builder\)

Action a user takes \(such as selecting a button\) or an occurrence that happens on a page. Most UI Builder components, pages, and data resources have default-associated events. Use event handlers with the events to add additional actions to pages.

## event handler

An action performed when an event occurs.

## event mapping

The process of identifying an event handler to run when an event occurs.

## macroponent

A core data structure that drives UI Builder pages. Its fields contain JSON data that builds the page.

## modal

A user experience window that overlays another content window and takes control of the user experience.

## now code editor

A rich-text editor that supports CSS, HTML, JavaScript, XML, and JSON. Use Now Code Editor to change UI configuration, data resource configuration, styles, events, client-side scripts, and server-side scripts in Next Experience UI Builder components.

## page

Collection of column layouts, columns, and components. Create or customize multiple UI Builder pages for workspace and portal experiences.

## page collection

Group of pages that can be reused in experiences within tabs or modals.

## popover

A page overlay that enables users to continue using the rest of the page. Popovers can be configured just like UI Builder pages with text, components, images, fields, and menu items.

## repeater

In UI Builder, a repeater is a component that acts as a basic loop that repeats the data you provide in multiple components. Repeaters use an array or an array of objects. Repeaters bind values to a data array property. For example, \[\{"task": "A"\},\{"task": "B"\}\], repeats the content inside it two times.

## UI Builder \(UIB\)

A WYSIWYG web user interface builder. UI Builder enables developers to build new pages or customize existing pages for Agent Workspace and portals using Now Experience UI Framework components.

## variant

The version of a UI Builder page with access controlled by role or condition. Create variants of pages to target experiences for different audiences. For example, create a home page for agents and a variant for managers at the same URL. Alternatively, create a page variant that users see under different conditions.

