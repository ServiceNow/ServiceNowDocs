---
title: Create a custom work item type in EAP
description: Create a custom work item type to include in the Agile configurations for Enterprise Agile Planning.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/enterprise-agile-planning/create-custom-work-item-type-in-eap.html
release: australia
product: Enterprise Agile Planning
classification: enterprise-agile-planning
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Enterprise Agile Planning, Strategic Planning, Strategic Portfolio Management]
---

# Create a custom work item type in EAP

Create a custom work item type to include in the Agile configurations for Enterprise Agile Planning.

## Before you begin

Set the application scope in your instance to Portfolio Planning Core.

Role required: sn\_apw\_advanced.eap\_admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Select **New**.

3.  On the form, fill in the fields.

    For field information, see [Work item type form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/work-item-type-form-for-eap.md).

4.  Deselect the **Create module** check box.

5.  Select **Submit**.


## What to do next

For any new work item type tables, create relevant form views and list views. See [Create or update form views for EAP work items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/create-or-update-form-views-for-eap-work-items.md) and [Create or update list view for EAP work items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/create-or-update-list-views-for-eap-work-items.md).

If the work item type uses custom state choices as columns on the Planning board, map the custom states to state buckets so that cards display correctly after a page reload. For more information, see [Configure state bucket mapping for custom story states in EAP](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/enterprise-agile-planning/configure-state-buckets-for-custom-story-states-in-eap.md).

