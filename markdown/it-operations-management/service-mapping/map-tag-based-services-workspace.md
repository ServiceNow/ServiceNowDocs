---
title: Map your application services using tags in the Service Mapping Workspace
description: Categorize and organize organization's configuration items and map them into application services using the Tag-based dashboard in the Service Mapping workspace.
locale: en-US
release: yokohama
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-06-08"
reading_time_minutes: 2
breadcrumb: [Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Map your application services using tags in the Service Mapping Workspace

Categorize and organize organization's configuration items and map them into application services using the Tag-based dashboard in the Service Mapping workspace.

## Before you begin

-   Verify that you have installed Service Mapping Plus version 1.16.3, which is required to access tag-based mapping in the Service Mapping workspace. For more information, see [Install Service Mapping Plus](install-service-mapping-plus.md).
-   Review and analyze your organization’s tag usage, making a list of all tags and their purposes. Use the Key Value \[cmdb\_key\_value\] table to see the tags in the Configuration Management Database \(CMDB\).
-   Use Tag Governance to optimize tag application in your organization. See [Tag Governance](../../it-operations-management/concept/exploring-tag-governance.md) for more information.
-   Assign tags to configuration items \(CIs\) that you want to include in application services.
-   Run Discovery to horizontally discover CIs. Discovery populates the CMDB with the CI data, including tags. For more information about discovery tag-based discovery for the Service Mapping workspace, see [Tag-based discovery for the Service Mapping Workspace](../concept/tag-discovery-service-mapping-workspace.md).

Role required: service\_mapping\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Mapping**, then select the Tag-based Service Mapping icon ![](../../../reuse/icons/product-icons/tag-outline-24.svg) from the navigation pane.

2.  Select **Create service maps**.

3.  Either select an existing tag category or create a new tag category.

<table id="choicetable_mmz_qlx_1gc"><thead><tr><th align="left" id="d562261e181">

Tag category option

</th><th align="left" id="d562261e184">

Action

</th></tr></thead><tbody><tr><td id="d562261e190">

**Select an existing tag category**

</td><td>

1.  Start entering the category name in the search field.
2.  Select the tag category from the list.
3.  Select **Define the tag values** and enter values for the selected category.


</td></tr><tr><td id="d562261e214">

**Create a new tag category**

</td><td>

1.  Create a new tag category by selecting **Create a new tag category**.
2.  Enter the tag category name.
3.  Enter values for the tag keys in the **Tags** field.


</td></tr></tbody>
</table>4.  Save the tag category and values by selecting **Save**.

    **Note:** To save the tag categories in a service family so you can return later to complete the mapping process, select **Save and exit** at any time.

5.  Search for potential services matching the tag categories by selecting **Find candidates**.

6.  Review the list of tag-based service candidates by selecting **Map selected candidates** when you have chosen your preferred candidates.

7.  When prompted, enter a unique name for the tag-based service family.

8.  Select **Save and map**.


## Result

A tag-based application service and tag-based service family have been created.

**Parent Topic:**[Using Service Mapping](../concept/using-service-mapping.md)

