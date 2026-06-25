---
title: Configuring a custom API to dynamically fetch supplier news
description: By default, News Integration for Supplier Lifecycle Operations retrieves the supplier news and activities using the Microsoft Bing News Search API.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/source-to-pay-operations/supplier-lifecycle-operations/config-supplier-news-api.html
release: australia
product: Supplier Lifecycle Operations
classification: supplier-lifecycle-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [News Integration, Integrate, Supplier Lifecycle Operations, Finance and Supply Chain]
---

# Configuring a custom API to dynamically fetch supplier news

By default, News Integration for Supplier Lifecycle Operations retrieves the supplier news and activities using the Microsoft Bing News Search API.

However, you have the flexibility to use any API of your choice to dynamically retrieve the supplier news and activities.

The process for configuring a custom news API includes the following tasks:

1.  [Create a REST message for a custom API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-custom-api-rest.md).
2.  [Add and configure the Get News data resource in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-config-news-data-resource.md).
3.  [Update the field names in the UX client script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/update-client-script.md).

1.  [Create a REST message for a custom API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-custom-api-rest.md)  
Create a REST message request and send it to a custom API endpoint to fetch the latest supplier news.
2.  [Add and configure the Get News data resource in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-config-news-data-resource.md)  
Add and configure the Get News - Composite data resource in UI Builder to dynamically retrieve supplier news in the News and Activity section of the Source-to-Pay Workspace.
3.  [Update the field names in the UX client script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/update-client-script.md)  
Update the field names in the UX client script to match the custom field names in the custom API response.

**Parent Topic:**[News Integration for Supplier Lifecycle Operations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/supp-news-integration.md)

**Related topics**  


[Create a REST message for a custom API](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/create-custom-api-rest.md)

[Add and configure the Get News data resource in UI Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/add-config-news-data-resource.md)

[Update the field names in the UX client script](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/source-to-pay-operations/supplier-lifecycle-operations/update-client-script.md)

