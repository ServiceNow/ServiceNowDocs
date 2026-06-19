---
title: Review existing planning item types in Strategic Planning
description: Before you create a portfolio plan using lenses, start with verifying that the default planning item types in Strategic Planning suit your company's planning needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/scenario-planning-in-spw/review-existing-planning-org-planning-item-types.html
release: australia
product: Scenario Planning in SPW
classification: scenario-planning-in-spw
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Planning item configuration for lenses and portfolio plans, Configure, Portfolio Planning in Strategic Planning Workspace, Strategic Planning, Strategic Portfolio Management]
---

# Review existing planning item types in Strategic Planning

Before you create a portfolio plan using lenses, start with verifying that the default planning item types in Strategic Planning suit your company's planning needs.

## Before you begin

Ensure you have the details of your company's planning needs.

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  Filter the list of tables by using **sn\_align\_core** in the Name column.

    \[Omitted image "table-filter-apw.png"\] Alt text: Review existing planning organizations and planning item types

3.  Review the tables that have **Planning Item** in the Extends table column.

    Confirm if those are all the tables that you would require to set up lens required for portfolio plans.


## What to do next

If you need a planning item type other than those available, use one of the five pre-defined custom planning item tables or you can create your own.

-   [Enable pre-defined custom planning item tables.](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/planning-items-for-lenses-and-portfolio-plans.md)
-   [Define a new planning item type in Strategic Planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/scenario-planning-in-spw/create-planning-organization-and-planning-item-type.md)

