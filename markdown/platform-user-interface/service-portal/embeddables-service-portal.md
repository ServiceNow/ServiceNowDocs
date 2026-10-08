---
title: Embeddables in Service Portal
description: Embeddables are UI Builder components that you can embed into Service Portal pages, external websites, and other web interfaces. Using embeddables, you can reuse existing components across multiple platforms without requiring an AngularJS rebuild. Embeddables enable low-code configuration of components, reducing development time and improving integration flexibility across your ServiceNow ecosystem.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/platform-user-interface/service-portal/embeddables-service-portal.html
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-09-23"
reading_time_minutes: 1
keywords: [embeddables, service portal, UI Builder, component reuse]
breadcrumb: [Developing custom widgets, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Embeddables in Service Portal

Embeddables are UI Builder components that you can embed into Service Portal pages, external websites, and other web interfaces. Using embeddables, you can reuse existing components across multiple platforms without requiring an AngularJS rebuild. Embeddables enable low-code configuration of components, reducing development time and improving integration flexibility across your ServiceNow® ecosystem.

## Key benefits

-   Reuse existing components across platforms. Deploy the same UI Builder component on Service Portal pages, external websites, and other web interfaces.

-   Reduce development time. Low-code configuration means faster deployment and fewer engineering hours required for component integration.

-   Improve portal performance with preloading. Service Portal can preload selected embeddable components during the initial page load, reducing runtime delays and improving the user experience.


## When to use Embeddables

Consider using embeddables when you want to:

-   Display the same UI Builder component in multiple Service Portal pages.
-   Embed Service Portal components in external websites or web applications.
-   Leverage existing components without rebuilding them for a new platform.
-   Improve portal responsiveness by preloading frequently used components.

## How embeddables work

When you enable embeddables in a portal, the Seismic framework and embeddable APIs automatically load. Service Portal widgets can then call the `spEmbeddables` AngularJS service to interact with embedded components at runtime.

You can:

-   Initialize embeddables with a specific UI Builder theme.
-   Retrieve component data and properties.
-   Register event handlers to respond to user actions.
-   Update component properties dynamically.

-   **[Enable embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-user-interface/service-portal/enable-embeddables.md)**  
Before you can use embeddables in Service Portal, you must install the required plugins and enable the feature on your portal record.
-   **[Configure theme mapping for embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-user-interface/service-portal/configure-theme-mapping-embeddables.md)**  
Apply a custom UI Builder theme that matches your ServiceNow® NOW experience.
-   **[Embeddable APIs](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-user-interface/service-portal/embeddable-apis.md)**  
Service Portal automatically loads the Seismic framework and embeddable APIs when you enable embeddables. To access these APIs in your Service Portal widget scripts, call the `spEmbeddables` AngularJS service.
-   **[Create a Service Portal widget with embeddables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-user-interface/service-portal/create-service-portal-widget-embeddables.md)**  
Create a Service Portal widget that displays an embeddable component. Add the component to the widget HTML and then call the embeddable APIs in a widget client script.

**Parent Topic:**[Developing custom widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/platform-user-interface/service-portal/widget-dev-guide.md)

