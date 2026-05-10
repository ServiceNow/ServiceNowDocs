---
title: Knowledge blocks for HR knowledge management
description: You can use knowledge blocks with HR Service Delivery to simplify knowledge authoring for writers and knowledge consumption for readers.
locale: en-US
release: australia
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [HR Knowledge Management, HR Administration, Configure, Case and Knowledge Management, HR Service Delivery, Employee Service Management]
---

# Knowledge blocks for HR knowledge management

You can use knowledge blocks with HR Service Delivery to simplify knowledge authoring for writers and knowledge consumption for readers.

Knowledge blocks are reusable pieces of content secured by user criteria that you can add to knowledge articles in a knowledge base. The user criteria controls which users can read or not read the block content in an article or search, enabling users to more easily view content that is relevant to them.

## How to use knowledge blocks

To use knowledge blocks, a knowledge administrator or manager must enable the knowledge blocks feature for each knowledge base in which the blocks will be used.

[Enable knowledge blocks for each knowledge base](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/enable-knowledge-blocks-for-knowledge-base.md)

Knowledge contributors can create knowledge blocks and insert them into articles in a knowledge base:

**Note:** Knowledge blocks are not supported in articles of type wiki. By default, knowledge block doesn't show files attached to it. However, you can see images and text are visible on KB's created from block files.

-   [Create a knowledge block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/create-modify-knowledge-block.md)
-   [Add knowledge blocks to a knowledge article](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/add-knowledge-block-to-knowledge-article.md)
-   [Preview a knowledge article with knowledge blocks by user or date](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/preview-knowledge-article-with-knowledge-blocks.md)

Knowledge block content can be read or not read in an article or search based on user criteria set at the knowledge base and knowledge block level. See [Select user criteria for a knowledge block](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/select-user-criteria-for-knowledge-block.md) for more information.

## Holiday calendar with location-specific knowledge block content

You are part of an enterprise HR organization that maintains a company knowledge base. You want to create a holiday calendar so that employees know which days of the year are company holidays. Since the company has multiple locations and holiday dates vary based on where the employee is located, there are several ways that you could create the knowledge article.

One way is that you could create a knowledge article for each location, with an article for Location A, Location B, and so on.

-   Pros: simplified consumption. Employees have a single article to search for and read.
-   Cons: more work for HR. HR has multiple articles to manage and update for each location where the company has employees.

Another way is that you could create a single knowledge article that includes sections for each location.

-   Pros: simplified authoring. HR has a single article to manage and update.
-   Cons: more work for employees. Employee must scroll through and disregard extraneous content to find the section in the article that pertains to them.

With knowledge blocks, you can create a single knowledge article with location-specific block content secured by user criteria. This approach helps to reduce the workload for both HR and employees. As an HR agent, you have a single article to manage and update. Employees have a single article to search for and read, with the user criteria ensuring that they only view content that is relevant to them.

## If you are using a custom search or knowledge article viewer

If you are using a custom search or knowledge article viewer with your application, you should integrate it with the appropriate knowledge or knowledge blocks API. \(Integration is only necessary if you are using a custom search or knowledge article viewer.\)

[Integrating a custom search or knowledge article viewer with knowledge blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/integrating-with-custom-search-or-knowledge-article-viewer.md)

## Activation information

To use knowledge blocks in your application, you must [activate knowledge blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/activate-knowledge-blocks.md). For information on what components are installed with the feature, see [Components installed with knowledge blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/components-installed-with-knowledge-blocks.md).

**Note:** Activating knowledge blocks automatically activates Knowledge Management Advanced, which enables advanced features such as article versioning. Knowledge blocks can be used with or without the article versioning feature. To disable the feature, see [Disable the article versioning feature](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/article-versioning-disable-property.md).

**Parent Topic:**[HR Knowledge Management](hr-knowledge-management.md)

**Related topics**  


[Knowledge blocks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/knowledge-management/knowledge-blocks.md)

