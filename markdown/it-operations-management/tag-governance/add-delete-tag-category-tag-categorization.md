---
title: Add or delete a tag category for Tag Categorization
description: Add or delete a tag category for improved tagging of your organization's configuration items \(CIs\) and cloud assets.
locale: en-US
release: zurich
product: Tag Governance
classification: tag-governance
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using Tag Governance, Tag Governance, ITOM Visibility, IT Operations Management]
---

# Add or delete a tag category for Tag Categorization

Add or delete a tag category for improved tagging of your organization's configuration items \(CIs\) and cloud assets.

## Before you begin

Verify that you have installed version 1.16.3 of Service Mapping Plus to access to the CI tag category and CI tag key tables. For more information, see [Install Service Mapping Plus](../../service-mapping/task/install-service-mapping-plus.md).

Role required: tag\_governance\_admin

## Procedure

1.  Navigate to **All** &gt; **Tag Governance** &gt; **Tag Categories**.

2.  Verify that you are in the leaf domain.

    1.  In the page header, select the globe icon ![](../image/globe-icon.png).

    2.  Select **Domain scope**, and choose the appropriate leaf domain.

3.  Add or delete a tag category.

<table id="choicetable_eks_y2x_yfc"><thead><tr><th align="left" id="d591722e127">

Action

</th><th align="left" id="d591722e130">

Description

</th></tr></thead><tbody><tr><td id="d591722e136">

**Add a tag category**

</td><td>

1.  Select **New**.
2.  Enter the category name in the **Tag category name** field.
3.  Select the Lookup using list icon ![](../../../administer/field-administration/image/SearchIconHeisenberg.png).
4.  Select **New** in the Tag Category Definitions window.
5.  Enter the value for the category definition in the **Regex** field.

**Note:** The regex identifies the tag values that are included in the category. Separate multiple values with a vertical slash \(\|\).

6.  Update the priority value.
7.  Select **Submit**.
8.  Select **Submit** on the CI tag category - New Record page.


</td></tr><tr><td id="d591722e198">

**Delete a tag category**

</td><td>

1.  Select the check box next to the tag category.
2.  In the **Actions on selected rows** menu, select **Delete**.


</td></tr></tbody>
</table>4.  If you want to apply your changes immediately rather than waiting for the automatic update within 24 hours, select the **Re-Categorize Tags** button.


