---
title: Tag categories
description: Tag categories in the Cloud Cost Management application enable grouping multiple tag names under a single category, making it simpler to track costs against specific business entities. In the provider portal, you can define cost tags to associate resource usage with specific business entities. For example, the Application, Test, and QA tags represent cost centers.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/cloud-cost-management/tag-categories.html
release: australia
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-08-14"
reading_time_minutes: 1
breadcrumb: [Cost usage tags, Explore, Cloud Cost Management, IT Asset Management, Asset Management]
---

# Tag categories

Tag categories in the Cloud Cost Management application enable grouping multiple tag names under a single category, making it simpler to track costs against specific business entities. In the provider portal, you can define cost tags to associate resource usage with specific business entities. For example, the `Application`, `Test`, and `QA` tags represent cost centers.

## Overview of tag categories

The Cloud Cost Management application enables you to enhance your cost management capabilities and ensure that the cost reports accurately reflect the business entities. For example, different users might create multiple tag names like "App", "AppService", and "appl" to represent applications. By creating a tag category named "Application", you ensure that costs associated with these different tag names are correctly assigned to the "Application" category. You can add multiple tag names to a category during or after its creation. For more information, see [Create and update a tag category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/cloud-cost-management/tag-category-crud-cloudin.md).

## Key points and considerations

-   Tag categories help in organizing and consolidating cost data from different sources.
-   Tag categories also enable more accurate cost reporting by grouping related tags together.
-   Cost categories are updated with new cost tag values each time billing data is downloaded through a Billing Download job.
-   Recent updates to tag category definitions might not be immediately reflected in cost reports.
-   To apply the latest tag category definitions to cost data without waiting for the next Billing Download job, you can manually reapply the categories. Reapply tag categories by navigating to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Cost usage tags** &gt; **Tag categories** &gt; **Reapply tag categories**.

