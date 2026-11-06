---
title: Configure web components
description: Understand how to configure ServiceNow web components on your instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/config-web-componts.html
release: australia
product: Customer Self-service and Omnichannel Engagement
classification: customer-self-service-and-omnichannel-engagement
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure Web Embeddables, Set up self-service, Configure, Customer Service Management]
---

# Configure web components

Understand how to configure ServiceNow web components on your instance.

## Components you can configure

Each component displays a different part of your ServiceNow data on your external website. Use the following table to choose the components that fit your use case.

|Component|What it shows|
|---------|-------------|
|[Case list component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/case-list-component.md)|A list of cases with key details such as number, short description, and status.|
|[Case view component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/case-view-web-component.md)|The details of one case, with activity and attachments.|
|[Case create component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/case-create-component.md)|A form to submit a case.|
|[Catalog item component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/catalog-item-web-component.md)|A form to request an item or service.|
|[Catalog browse component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-catalog-browse-comp.md)|Catalog items that you can browse by catalog or category, or search by keyword.|
|[Knowledge article view component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-know-article-view-comp-overview.md)|A knowledge article with its title, author, and read time.|
|[Playbook intake component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-playbook-intake-comp-overview.md)|A guided experience for submitting a case, with the stages involved in resolving it.|
|[Data visualization component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-data-viz-comp-overview.md)|Data from any table as a score, pie, donut, or semi-donut chart.|
|[Object list component](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-object-list-comp.md)|Records from any table in a list, with bulk and inline actions.|

## How you configure a component

Every component follows the same workflow:

1.  Create a module. See [Create a module](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/create-we-module.md).
2.  Add a group to the module, then add a component instance to the group. See [Create a group and add a component instance](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/we-create-group-and-add-comp-instance.md).
3.  Set the component properties for the instance.
4.  Configure CORS rules so your website can call your instance. See [Configure CORS \(Cross-Origin Resource Sharing\) rules before embedding ServiceNow components](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/configure-cors-for-web-components.md).
5.  Copy the embed code for the instance and add it to your website. See [Embed ServiceNow components instance on the third-party website](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/customer-service-management/customer-self-service-and-omnichannel-engagement/embed-web-components-third-party-website.md).

Then follow the topics for the component to see its properties and sample code.

