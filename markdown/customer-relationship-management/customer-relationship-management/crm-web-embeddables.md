---
title: Web embeddables
description: Web  embeddables  are a set of self-service components that you can embed directly into external websites to give customers access to ServiceNow  self-service  capabilities without leaving your site. Customers can  search for  knowledge articles,  submit  requests, and create and track cases  from any web page where the components are deployed. 
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 5
---

# Web embeddables

Web  embeddables  are a set of self-service components that you can embed directly into external websites to give customers access to ServiceNow  self-service  capabilities without leaving your site. Customers can  search for  knowledge articles,  submit  requests, and create and track cases  from any web page where the components are deployed. 

## Web embeddables overview

Web  embeddables  offer  pre-built,  configurable components that organizations embed directly into external websites to  give customer access to  ServiceNow self-service capabilities  without leaving the site or being redirected to a separate portal.

Administrators manage web  embeddables  through a dedicated experience in the ServiceNow instance. Each external website is represented as a module. Within a module, administrators add components and configure each  component  instance to control its behavior, appearance, and data access. The same  component  type can be configured differently across multiple external sites, all managed from a single ServiceNow instance.

Web  embeddables  include  default  components that address common self-service use cases, including knowledge search, case creation and tracking, and service catalog browsing.  Organizations that need capabilities beyond the default  components can create custom components.  Custom components follow the same deployment model as  default  components and are managed within the same admin experience, allowing organizations to extend web  embeddables  without  maintaining  a separate integration layer.

![End to end workflow for web embeddables](../image/we-end-to-end-workflow.png "High level end-to-end workflow of web  embeddables")

## Web embeddables benefits

Web embeddables provide benefits to customers and administrators across an organization

-   **For customers and end users:** Web  embeddables  enable  users  to access ServiceNow self-service capabilities from within the organization's main website using their existing authentication. Customers can search for knowledge articles,  submit  service requests, create cases, and track case progress without leaving the site or signing in to a separate portal.
-   **For administrators:** Web  embeddables  reduce the effort  required  to create and  maintain  the components needed to extend ServiceNow self-service capabilities to external websites. The  default  components are configurable, themeable, and  Non-functional  requirements  \(NFR\)  compliant.

## Web embeddables components

Web  embeddables  include nine components that cover knowledge, catalog, case management, and data presentation use cases.

-   **Knowledge Article View**

    Displays a specific knowledge article inline on an external page. Organizations  use this  component  to surface resolution content, product documentation, or policy information at the point where customers are most likely to need it. The  component  renders  article content from the ServiceNow knowledge base and supports article feedback.

-   **Catalog Browse**

    Shows  service catalog categories and items on an external page, allowing customers to explore available services and navigate to specific items. Organizations  use this component to expose a curated service catalog on intranets, employee portals, or customer-facing sites without requiring access to the ServiceNow portal.

-   **Catalog Item/Service Request**

    It  surfaces with  a specific catalog item form on an external page, allowing customers to  submit  a service request directly from the site. Organizations use this  component  to make high-demand services available at the point of need, such as embedding a hardware request form on an IT intranet page or a returns request form on a product support page.

-   **Case Create**

    Provides a case submission form on an external page. Customers complete the  form  and  submit  a case to ServiceNow without leaving the site. Organizations  use this  component  on support pages and contact pages to capture structured case data and route it directly into ServiceNow case management workflows.

-   **Case View**

    Shows the details of a specific case on an external page. Customers can review case status, activity, and  resolution  information from the external site  where the  component  is embedded. Organizations  use this  component  to give customers visibility into their cases without requiring access to a full self-service portal.

-   **Case List**

    Displays a list of cases associated with the authenticated user on an external page. Customers can review open and resolved cases and navigate to individual case details. Organizations  use this  component  on account pages and support dashboards to give customers a  consolidated  view of their service history.

-   **Object List**

    Displays a configurable list of ServiceNow records on an external  page. The component supports a range of record types and can be configured to display fields, filters, and actions relevant to the use case. Organizations  use this  component  to surface data that does not fit a standard case or catalog pattern, such as order records, incident queues, or asset inventories.

-   **Data Visualization**

    Renders  charts and data summaries from ServiceNow on an external page. Organizations  use this  component  to surface operational metrics, service performance data, or analytics relevant to the audience of the external site, such as SLA summaries on a customer account page or request volume trends on an operations dashboard.

-   **Playbook Intake**

    Enables you to  submit  a case using the playbook guided experience, which systematically captures case details and displays the stages and activities involved in resolving the case. You can use prefilled fields or choose from various playbook experiences, and customize the display of stages, such as the number of visible stages and their horizontal or vertical orientation.


## Use cases

-   **Technology: product support site**

    A software company embeds Knowledge Search and Case Create on its product support site. Customers searching for help see relevant knowledge articles inline before deciding whether to submit a case. Customers who do not find a resolution complete the Case Create form without leaving the support site.

    After  submitting a case, the customer accesses Case View on their account page to  monitor  status and review agent responses. The company reduces inbound case volume from customers who resolve issues through knowledge search and provides a consistent support experience without building a separate portal.

-   **Financial services: customer account portal**

    A financial services organization embeds Catalog Item on its customer account portal to allow customers to submit  account service requests, such as address changes and statement requests, directly from the portal page. Case List gives customers a view of all open and resolved cases from the same page.

    Because the components connect to the existing ServiceNow instance, submitted requests enter the same fulfillment workflows as requests  submitted  through other channels. The organization extends self-service to the account portal without duplicating workflow configuration or case management infrastructure.

-   **Telecommunications: device and plan support**

    A telecommunications provider embeds Knowledge Search and Case Create on device-specific support pages. Customers troubleshooting a device  see k knowledge articles relevant to that device model before  submitting  a support case. The Case Create  component  is pre-configured with the device  context,  so customers do not need to reenter information already captured by the page.

    The provider also embeds Data Visualization on an internal operations dashboard to surface case volume and SLA performance metrics for service managers reviewing daily operations.

-   **Manufacturing: dealer and partner portal**

    A manufacturer embeds Catalog Browse and Catalog Item on a dealer portal to give authorized partners access to  parts  ordering, warranty claim submission, and service documentation requests. Partners complete catalog requests from the portal without requiring access to the full ServiceNow instance.

    Object List surfaces open order records on the  portal  so dealers can  monitor  fulfillment status for  submitted  requests without contacting the manufacturer directly.


**Related topics**  


[bundle-csm.using-web-embeddables]

