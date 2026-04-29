---
title: General guidelines for developing widgets
description: When developing custom widgets, keep these general guidelines in mind for optimal performance, scalable development, and a good user experience.
locale: en-US
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# General guidelines for developing widgets

When developing custom widgets, keep these general guidelines in mind for optimal performance, scalable development, and a good user experience.

-   **Create a default state that provides an example to the end user**

    A widget does not have instance options defined when initially added to a page. A widget in this empty state can appear blank and cause confusion. In situations where a widget requires some initial configuration, ensure that your widget has a default state that communicates to the admin what configuration is necessary.

    Widgets can also be created with demo data. Demo data can also be used to:

    -   Clearly demonstrate the widget functionality to the user.
    -   Provide data when previewing the widget in the widget editor. \(Demo data is not visible in the designer\).
    Learn more: [Tutorial: Build a custom widget](adv-widget-tutorial.md#).

-   **Embed a widget rather than clone when possible**

    Embedding an existing widget into your custom widget takes advantage of pre-existing functionality without cloning or duplicating code. You can still pass parameters into the embedded widget to control its behavior.

    Learn more: [Embed an existing widget](adv-widget-tutorial.md#)

-   **Avoid using large data sets to improve performance**

    Querying data, evaluating ACLs, running business rules, and data processing take time and can slow performance. Determine how much data portal users need and then apply the appropriate limits and filters to your scripts and queries. Isolate widgets that require significant data or processing to their own separate pages in the portal. Avoid implementing the following items that use large data sets:

    -   Scripted menu items that load large amounts of data, which can cause every page in the portal to load slowly.
    -   Large files and attachments, such as high-definition media files or fonts from the Attachments \[sys\_attachment\] table.
    -   Auto-refreshing widgets. Every time a widget's client controller calls server.update\(\), spUtil.update\(\), server.refresh\(\), or spUtil.refresh\(\), the application runs the widget's server script and sends a data object back to the client.
    -   Unfiltered record watchers. The recordWatch\(\) function watches for updates to a table or filter and returns the value from the callback function. Adding filters for specific fields to watch reduces the number of calls a widget makes to the server. Specifying when to refresh widgets in response to a record producer notifying the client that there is an update in the callback function can also improve performance.
    -   Server-side scripts with GlideRecord queries without the `setLimit` function. Using the `setLimit` function can restrict the number of records returned and improve response time on queries. For added flexibility, you can tie this limit to an instance option rather than assigning a hard-coded value \(for example: `gr.setLimit(options.limit || 100)`\).
    Learn more:

    -   [Six common performance pitfalls in Service Portal and how to avoid them \[KB0634588\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0634588)
    -   [spUtil - recordWatch](https://www.servicenow.com/docs/access?context=spUtilAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
    -   [GlideRecord setLimit Function](https://www.servicenow.com/docs/access?context=c_GlideRecordAPI&version=australia&pubname=australia-api-reference&ft:locale=en-US)
-   **Create a directive instead of embedding a complex widget**

    When an embedded widget is called from the server, all the scripts associated with that widget are returned. If you only need a subsection of a widget, embedding the entire widget creates unnecessary overhead. Instead, use directives to share lightweight code between widgets. Directives are useful, for example, when building UI components. Complex components with server-side and client-side functionality are best left as widgets. Use a directive instead of an embedded widget to:

    -   Share scope or custom scope behavior with multiple widgets.
    -   Share a reusable, lightweight subsection of a widget.
    -   Share a common UI feature, such as a list or an avatar.
    -   Augment widget behavior.
    Learn more: [Reuse components with Angular Providers](../task/angular-providers.md).

-   **Use a service or factory to share data and persist state**

    Data services and factories maintain and persist state in a widget without requiring multiple calls to the server, enabling you to:

    -   Keep widgets synchronized when changing records or filters.
    -   Share data between widgets.
    -   Develop more performant widgets.
    Learn more: [Reuse components with Angular Providers](../task/angular-providers.md).

-   **Handle events with a publish/subscribe service**

    Avoid using [$broadcast](https://docs.angularjs.org/api/ng/type/$rootScope.Scope#$broadcast) in the DOM. $broadcast dispatches the event name to all child scopes notifying registered listeners, which can be an expensive call that requires the use of the $rootScope global object.

    Instead, use a publish/subscribe service to handle events. When using a publish/subscribe service, a clear relationship forms between your widgets through callback handlers. In this model, you can better control the state of your events.

-   **Use REST calls or `server.get` to fetch data from the server**

    When you call `server.update()`, the entire widget is returned from the server. If your widget includes divergent code paths, multiple calls to update the server can affect performance. As a rule, use your server script to set up the initial state of your widget. For subsequent updates, use scripted REST APIs that call script includes on your instance. This practice:

    -   Separates business logic from UI elements.
    -   Centralizes your code, allowing changes to be made in one place.
    You can also use `server.get` to pass information to the server. Use this function along with `input.action` to execute specific parts of the server script.

-   **Develop with localization, accessibility, and UI in mind**

    To create the best experience for your users, follow these guidelines:

    -   Consider the impact of your widget in a mobile environment. For example, avoid using mouse-over and other events that do not translate to a mobile device.
    -   Use SCSS variables to reuse items. See [SCSS variables](scss-primer.md#).
    -   Use variable names when using colors.
    -   Wrap strings for translation in localization APIs. See [Internationalize a widget](c_WidgetLocalization.md).
-   **Remove unused Angular Providers from client script**

    For easier maintenance, remove any unused Angular Providers that were injected into the client script function statement.

-   **Avoid using &lt;script&gt; tags in HTML templates**

    To lessen the likelihood of production issues in Service Portal, avoid using inline templates using &lt;script&gt; tags in a widget's HTML template. Instead, create a related Angular ng-template record for the widget.


**Parent Topic:**[Developing custom widgets](widget-dev-guide.md)

