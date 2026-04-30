---
title: Dynamically expose data in UI Builder pages \(advanced feature\)
description: Sync data between ServiceNow tables and data with the pages you build with UI Builder. Pages display synced data in real time and update data/tables when a user inputs information.
locale: en-US
release: xanadu
product: UI Builder
classification: ui-builder
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Advanced UI Builder, UI Builder, Builder library, Developing your application, Building applications]
---

# Dynamically expose data in UI Builder pages \(advanced feature\)

Sync data between ServiceNow tables and data with the pages you build with UI Builder. Pages display synced data in real time and update data/tables when a user inputs information.

## Learning about data resources in UI Builder

UI Builder syncs ServiceNow tables/data using [data resources](ui-builder-glossary.md#). A data resource fetches the data that UI Builder uses to display information in a [component](ui-builder-glossary.md#). UI Builder components use data resources to sync data across different experiences. Data resources make the data in components dynamic, which means that you don't have to recreate data for every page.

![Data resource stack distributing data to multiple pages.](../image/data-resource-graphic.png)

Data resources are found in the data resource drawer. The data resource drawer is where you can add and configure a data resource for your page. After you configure the data resource, you can sync the data between components on your page and ServiceNow tables/data.

![Arrow pointing to the data resource drawer in UI Builder.](../image/data-resource-shelf.png "Data Resource Drawer")

The data resource drawer contains three sections:

-   Data resources: The data resources that are part of the experience
-   Configuration/Events: Configured data resources and events for the experience
-   Preview: JSON for the information returned by the data resource

You can bind the configuration properties for components, other data resources, client scripts, client state, and events to these data resources.

Set conditions for a filter in your data resource. For more information, see [Connect data to your components](../task/connect-data.md).

## How data resources work in UI Builder

Data resources fetch data from Glide, GraphQL, and REST APIs, then transform it for use in a component on a UI Builder page.

Components use both inherited and local data resource instances. Inherited data resources are automatically loaded into a UI Builder page, and local data resource instances can be added and configured. Data resources are evaluated based on specified input values to make sure the right data is retrieved. For more information about inherited and local data resources, see [Inherited versus local data resources in UI Builder](data-resources.md#inherited_versus_local).

## Local data resources in UI Builder

You can select local data resources, such as server data, operations, transforms, or client data, like the gForm API, to bring data to the UI Builder page.

**Note:** Only one GlideForm is supported per page in UI Builder. For more information about GlideForm, see the [ServiceNow Developer site](https://developer.servicenow.com/dev.do#!/reference/api/vancouver/client/c_GlideFormAPI).

Data resources are organized by application in the data resource drawer. They are then further categorized by the data resource type like Server data or Transform. For example, the Global application has several data resources, but the Customer Service Management \(CSM\) Workspace application has only a few data resources.

![Data resources select modal.](../image/data-resources-local.png "Data resources")

You see different data resources depending on the application that you are in. If you select the Global application, you will see different data resources under Server data than if you select the CSM Configurable Workspace application.

## Using data binding in UI Builder

Data binding enables you to create dynamic pages by syncing pages and components to data resources. You can bind data to a component to retrieve data from the back end, and use field parameters to get properties from the URL. Changing the URL parameters enables you to create dynamic pages that show different data depending on the parameters.

You can bind data to a component in the following ways:

-   **Context binding**

    Use URL parameters to connect parts of the URL with your page's properties. For example, you can link the table name from the URL to your component by using the @context syntax, like this: `@context.props.table`.

    Imagine you have a UI Builder page with a required field named `table`. The URL for your page might look like /demo/page/&lt;table-name&gt;. The &lt;table-name&gt; could be something like `incident`. The data can also come from parent data resources or be local properties specific to the page.

    To link your component properties, other data resource properties, or event details to the page property, you use a `@context.props.table` binding. Be sure to either provide a test value in the URL or set a fixed value for that property in your page's configuration if you are using context binding.

-   **Data resource binding**

    Use data resources to fetch data from the back end of your instance, such as Client state, GraphQL, or a REST API. These data sources have properties that can be linked to elements on a UI Builder page.

    For instance, if you are using the Lookup Record data resource, you can utilize it in a button component. You might use a data expression in the "label" property like this: `@data.lookup_record_1.result.number.displayValue`.

-   **Component binding**

    Use component binding to connect one component to another. Let's say that you have a List Menu component on the UI Builder page. The List Menu reveals the currently chosen list to other components on the same page. These other components can access the data by linking to it using an expression such as `@elements.list_menu_1.selectedListId`.

-   **Client state parameter binding**

    Use client state parameter binding to connect and synchronize data between a client-side application and UI Builder components. Parameter binding allows the client state to automatically update data in components, and vice versa. Use `@state` syntax to bind a state property to a client state parameter.


## Types of data sources available in UI Builder

You can use the following data resource types that are shown in the table.

|Data resource type|Description|
|------------------|-----------|
|Controller|Encapsulates data and event logic and enables presets for components.|
|GraphQL|GraphQL queries and mutations that are executed.|
|Transform|Script that transforms the input data into another format.|
|Client state|Client-side data resources that include the client information, domain-specific states or logic, user preferences, and so on.|
|Composite|Single reusable data resource that contains multiple data resources.|
|REST|Data resources that are made through REST API requests.|

## Inherited versus local data resources in UI Builder

Inherited data resources share information from the surrounding parts of a UI Builder page such as an application. Imagine your page is in a large frame, and it gets some information from the frame or other parts around it. You can use this info by connecting it to your page's properties, kind of like linking puzzle pieces together. If you get this information from the frame, you don't have to get it again yourself.

![Diagram showing the difference between inherited and local data resources.](../image/data-resources-inherit-local.png)

Local data resources are items you add to a UI Builder page yourself. Imagine you're making a page for travel requests. You can sync employee data to a list component so employees can request trips linked to their own info.

To use these data resources, either bring them in from an app or create them in the ServiceNow platform. Then, in UI Builder, make these resources available for your components. Next, tie the data to your component, so it can work with it. For instance, you could have a set of records, expose it in UI Builder, and link it to a component. From there, configure the component to do things with the data, like saving new records.

Once your page is syncing data, you connect it to the part of the page that needs it such as a component. It's like making sure the right puzzle piece fits in the right spot. Then you can tell that part of the page what to do with the data. For example, you might use it to add new travel plans for employees.

## UI Builder Data resource properties

When you add a data resource in UI Builder, it's like adding a tool that knows where to get information from. Data resource properties are the instructions that tell a data resource how to bring data into UI Builder pages. These properties tell a data resource which data to get, how to organize it, and what conditions to follow. For instance, you can use these properties to specify which tables to look in, how to sort the data, and more. These properties are what make the data resource work correctly and give you the data you need.

## UI Builder Data resource scripts

Data resource scripts are special instructions you give UI Builder to return specific pieces of data. For example, if you're dealing with a list of products, a script could tell a data resource to show only products that are available in stock or to arrange them in a particular order. Data resource scripts enable you to customize how UI Builder treats the information, such as adding extra rules or actions.

-   **[Add and configure data resources to a page](../task/add-data-resources.md)**  
Add data resources to dynamically expose data from tables, records, or other elements on your page in UI Builder.
-   **[Bind data to UI Builder pages using controllers \(advanced feature\)](controllers.md#)**  
Controllers simplify the linking of data and event logic to enable component presets in UI Builder.
-   **[Connect data components](connect-data-components.md)**  
Use the data binding modal to associate data exposed by local data resources to components on your UI Builder page.
-   **[Client state parameters](client-state-parameters.md)**  
Use client state parameters to bind values to component configurations. When the client state parameter's value changes, the component updates to use the new value.
-   **[Define and bind client scripts to components](../task/define-client-scripts.md)**  
Add and edit client scripts in UI Builder so that you can update the client state through events. You can bind these scripts to any component by using an event handler.
-   **[Multi-table data configuration](multi-source-data-configuration.md)**  
Present data from multiple tables using components and control the layout and styling.
-   **[Work with the Entity View Action Mapper for UI Builder](evam-ui-builder.md)**  
With UI Builder, you can use the Entity View Action Mapper \(EVAM\) application to standardize how the data sources in your components are displayed in your cards and lists.

**Parent Topic:**[Advanced UI Builder](advanced-uib.md)

