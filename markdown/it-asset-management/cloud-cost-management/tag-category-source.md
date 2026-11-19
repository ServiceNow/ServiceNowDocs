---
title: Tag category source
description: The Tag category source setting controls how the Cloud Cost Management application maps cloud resource tags to business entities for cost attribution and reporting.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/cloud-cost-management/tag-category-source.html
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-08-13"
reading_time_minutes: 2
breadcrumb: [Cost usage tags, Explore, Cloud Cost Management, IT Asset Management]
---

# Tag category source

The Tag category source setting controls how the Cloud Cost Management application maps cloud resource tags to business entities for cost attribution and reporting.

The Cloud Cost Management application compares billing data with tag categories to calculate and report cloud spend by business entity. By default, tag categories are defined independently in the Cloud Cost Management application. With the tag category source setting, cloud admins can align cost attribution with the CMDB-driven cloud mapping taxonomy already maintained in their ServiceNow instance. This eliminates the need to duplicate business tagging in each cloud provider.

When you select a tag category source, that selection determines how spend tags are derived during each billing download. It also determines how costs are grouped in analytics, forecasting, and recommendations.

## Tag category source options

The Cloud Cost Management application provides the following tag category source options:

-   **Cloud provider resource tags**

    This is the default selection. The Cloud Cost Management application uses the tag names and values that your cloud provider attaches to each billing line item. Tag categories are defined and managed in the Cloud Cost Management application.

-   **CMDB-driven cloud mapping**

    Maps billing data to CMDB CI entities for cost attribution. This option requires that the selected tag names are present on billing line items from your cloud provider.

-   **ServiceNow-managed dimensions**

    Uses the CI-to-application service mapping already defined in the CMDB. This option requires that CI-to-application service relationships are populated in your CMDB before you select it.


**Related topics**  


[Select a tag category source](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/select-tag-category-source.md)

[Create and update a tag category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/tag-category-crud-cloudin.md)

[Cost usage tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/tags-overview.md)

[List of default tag categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/default-tag-categories.md)

