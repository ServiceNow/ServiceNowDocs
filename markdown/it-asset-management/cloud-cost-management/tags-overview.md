---
title: Cost usage tags
description: Cost usage tags in the Cloud Cost Management application are the tag key-value pairs that cloud providers attach to billing line items when resources are deployed.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/cloud-cost-management/tags-overview.html
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Explore, Cloud Cost Management, IT Asset Management]
---

# Cost usage tags

Cost usage tags in the Cloud Cost Management application are the tag key-value pairs that cloud providers attach to billing line items when resources are deployed.

## Overview of Cost usage tags

Cost usage tags represent the metadata that your teams define in AWS, Azure, or Google Cloud to identify who owns a resource, what it's for, or which business entity it belongs to. For example, a tag key of `App` with a value of `Payments-Service`.

On their own, raw providers tags might be inconsistent across teams and providers. Cloud Cost Management solves this with tag categories, which group multiple tag names under a single normalized label. This enable cost reports to accurately reflect business entities regardless of possible tagging inconsistencies across your cloud environment.

**Related topics**  


[Create and update a tag category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/tag-category-crud-cloudin.md)

[List of default tag categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/default-tag-categories.md)

