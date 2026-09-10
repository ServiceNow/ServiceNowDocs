---
title: Spend analytics
description: The Spend analytics page gives you visibility of your cloud spending data across multiple report types, including cloud spend, Kubernetes spend, and shared cost. Use saved views to store and reload your preferred filter configurations, including cost type, time range, and group-by selections.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/cloud-cost-management/spend-anaytics.html
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Spend view, Cloud Cost Management Workspace, Explore, Cloud Cost Management, IT Asset Management]
---

# Spend analytics

The Spend analytics page gives you visibility of your cloud spending data across multiple report types, including cloud spend, Kubernetes spend, and shared cost. Use saved views to store and reload your preferred filter configurations, including cost type, time range, and group-by selections.

**Important:** If you have the Insights owner \(insights\_owner\) role, only the accounts that are assigned to you appear in the filters and data.

Selecting any bar on the spend report navigates you to the list view of the corresponding report. The following roles can perform actions on spend views:

-   Spend admin \(spend\_admin\) and Spend owner \(spend\_owner\): can create, update, share, favorite, and delete views. These roles can also modify the system property sn\_cld\_spend\_core.favourite\_views\_limit.
-   Spend user \(spend\_user\): can create, update, favorite, and delete their own views. This role can read but not modify the system property sn\_cld\_spend\_core.favourite\_views\_limit.

Access the Spend analytics page by navigating to **Workspaces** &gt; **Cloud Cost Management Workspace** &gt; **Spend** &gt; **Spend analytics**.

\[Omitted image "spend-analytic.png"\] Alt text: Spend analytics page on Cloud Cost Management Workspace

Perform the following actions on the Spend analytics page.

<table id="table_i5b_qsv_zjc"><thead><tr><th>

Button or icon

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Star \(outline\)

</td><td>

Marks a spend view as a favorite. The star \(outline\) icon \[Omitted image "star-outline.png"\] appears next to each saved view on the Spend Analytics page.

</td></tr><tr><td>

Star \(solid\)

</td><td>

Indicates that the current view is marked as a favorite. Select the Star \(solid\) icon \[Omitted image "solid-star.png"\] again to remove it from your favorites list.

</td></tr><tr><td>

Spend report type

</td><td>

Displays the available spend report types:-   Cloud spend
-   Kubernetes spend
-   Shared cost

</td></tr><tr><td>

Favorite views

</td><td>

Shows the list of views that are marked as favorite by selecting the star icon. The list shows the view names based on the report type selected from the spend report type drop-down list. If cloud spend is selected only for Cloud spend, the favorites will show up in the list.

</td></tr><tr><td>

Set as default

</td><td>

Sets a spend report as your default view on the Spend analytics page.

</td></tr><tr><td>

Rename

</td><td>

Renames the spend report.

</td></tr><tr><td>

Delete

</td><td>

Deletes the spend report.

</td></tr><tr><td>

Save

</td><td>

Saves a spend report with a preferred view name and lets you choose who can view the report. Available values are:-   Public: The view is visible to all users.
-   Me: The view is visible only to you. This is the default selection.
-   Group: The view is visible to members of the groups you select in the **Groups** field.

</td></tr><tr><td>

Save as

</td><td>

Creates a new spend view based on the selected filters. Use this action to duplicate and rename an existing view without overwriting it.

</td></tr></tbody>
</table>Apply any of the following filters to a spend report to view precise results. The filters that you apply on the Spend analytics page also get applied to the list view of the report.

<table id="table_cmv_bzv_zjc"><thead><tr><th>

Filter

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Group by

</td><td>

Groups the spend report by the following available options:-   Provider
-   Purchase option
-   Region
-   Service account
-   Service category
-   Cloud service
-   Resource group
-   Tag category

</td></tr><tr><td>

Cost type

</td><td>

-   **Actual cost**: Each billing period, your organization pays for direct cloud services.
-   **Amortized cost**: Your organization pays the effective cost of the upfront and monthly reservation fees spread across the billing period. The amortized cost type is described in detail on the provider site.

</td></tr><tr><td>

Time range

</td><td>

Sorts your spend results by the current month or a time range such as 3, 6, 9, or 12 months.

</td></tr><tr><td>

Additional filters

</td><td>

Narrows down spend data using the following specific scopes:-   Provider
-   Master Service Account
-   Service account
-   Region
-   Service category
-   Cloud service
-   Purchase option
-   Resource group
-   Tag category

**Note:** For more information about tag categories and the list of default tag categories, see [Cost usage tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/tags-overview.md) and [List of default tag categories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/default-tag-categories.md).

-   Tag values
-   Tag categories selected

</td></tr></tbody>
</table>**Related topics**  


[Cloud service categories in Cloud Cost Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/cloud-ser-categories.md)

[Cost usage tags](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/tags-overview.md)

[Create and update a tag category](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/tag-category-crud-cloudin.md)

[Create or update a shared cost allocation policy](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/cloud-cost-management/create-shared-cost-policy.md)

