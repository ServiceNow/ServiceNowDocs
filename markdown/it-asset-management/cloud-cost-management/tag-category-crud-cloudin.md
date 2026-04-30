---
title: Create and update a tag category
description: Create a tag category to enable multiple tag names for representing costs against a single business entity. For example, multiple users might independently have created the tag names "App", "AppService", and "appl" to indicate applications. With a tag category of "Application", any costs for items tagged App, AppService, or appl are correctly assigned as costs against an application.
locale: en-US
release: zurich
product: Cloud Cost Management
classification: cloud-cost-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Use, Cloud Cost Management, IT Asset Management]
---

# Create and update a tag category

Create a tag category to enable multiple tag names for representing costs against a single business entity. For example, multiple users might independently have created the tag names "App", "AppService", and "appl" to indicate applications. With a tag category of "Application", any costs for items tagged App, AppService, or appl are correctly assigned as costs against an application.

Watch this short video to learn how to create and update a tag category.

Demonstrates how to create and update a tag category in Cloud Cost Management. 

## Before you begin

Role required: insights\_admin \[sn\_clin\_core.insights\_admin\]

## About this task

This procedure describes the process as performed from the user interface. Alternatively, to speed the process, you can edit the affected tables directly.

-   Tag Category \[sn\_cld\_intg\_core\_tag\_category\]
-   Tag Name-Category \[sn\_cld\_intg\_core\_tag\_name\_category\]

**Note:** Each successful execution of a Billing Download job updates tagged costs. Recent updates that you make to tag category definitions might not reflect ton the cost reports. To apply the latest tag category definitions to cost data without running a Billing Download job, select **Reapply categories** by navigating to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Cost usage tags** &gt; **Tag categories**.

## Procedure

1.  Navigate to **Cloud Cost Management Workspace** &gt; **Operations** &gt; **Cost usage tags** &gt; **Tag categories**.

2.  On the Tag Categories list, select **New**.

    For the list of default tag categories, see [List of default tag categories](../reference/default-tag-categories.md).

    **Note:** In this step, you add a single tag name to the category to create the initial category record. You can add any number of tag names to the category later.

3.  On the form, fill in the fields.

<table id="table_rlq_pzf_h4b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

A unique and meaningful name for the category.

</td></tr><tr><td>

Active

</td><td>

The option to add the category to the **Tag Category** filter list on spend reports.

</td></tr><tr><td>

Enable grouping

</td><td>

Option to add a **category:value** option for this category to the list of **Group by** choices on spend reports. **Note:** A category must be active to appear in the **Group by** list.

</td></tr><tr><td>

Tag names

</td><td>

The list of tag names that you can add to the category.1.  Select the Lookup icon ![Search icon.](../../software-asset-management2/image/search-icon.png) to open the list of tag names that came with the latest Billing Download Job. All tag names appear on the Tag Names list.
2.  Select tag names from the drop-down list.


</td></tr></tbody>
</table>4.  Select **Save** to create the category.

    The new category appears in the Tag Categories list.

5.  In the Tag Categories list, select the category that you just added.

    The Tag Category form reopens and the tag name that you added appears in the **Tag names** list.

6.  On the **Tag names** list, select the Lookup icon ![Search icon.](../../software-asset-management2/image/search-icon.png) to add multiple tag names.


**Parent Topic:**[Using Cloud Cost Management](../concept/using-cloud-insights.md)

**Related topics**  


[Tags and tag categories](../reference/tags-overview.md)

