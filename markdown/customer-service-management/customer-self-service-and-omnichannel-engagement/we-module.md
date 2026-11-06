---
title: Configure module in Web Embeddables
description: A module is a collection of component instances tied to specific domains or deployment contexts.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-module.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure module in Web Embeddables

A module is a collection of component instances tied to specific domains or deployment contexts.

A module represents a website with a collection of pages or a section using groups and a collection of components instances embedded on the website. The theme for component instances, external domain URL for CORS, and custom ServiceNow domain for base URL are derived from module meta data.

\[Omitted image "we-module-1.png"\] Alt text: Web Embeddables homepage displaying demo module under Your modules section.

## How modules, groups, and component instances fit together

You model your website in Web Embeddables with three levels.

|Level|Represents|
|-----|----------|
|Module|Your website.|
|Group|A page or section of your website.|
|Component instance|A component on that page or section.|

## What a module controls

All component instances in a module share the module settings:

-   Theme. The theme applies to all components that you embed on your website.
-   External domain. The domain where you embed the components. Your CORS rules depend on this domain. If you change it, review the CORS rules and reconfigure them if necessary.
-   ServiceNow custom domain. The domain of the instance where you configure the components, used as the base URL. If you change it, copy the updated global code to your webpages.

## Start from a prebuilt module

You can create a module or use a prebuilt module, such as the demo module, and edit it to fit your website. When you create a module, a default group named Group 1 is created for it automatically.

For more information, see [Create a module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/create-we-module.md) and [Create a group and add a component instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-create-group-and-add-comp-instance.md).

