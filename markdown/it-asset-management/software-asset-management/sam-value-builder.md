---
title: Value builder
description: Maximize the usage of your Software Asset Management application capabilities by getting insights into integrations, playbooks, and other installations.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Success portal view in Software Asset Workspace, Software Asset Workspace, Explore, Software Asset Management, IT Asset Management]
---

# Value builder

Maximize the usage of your Software Asset Management application capabilities by getting insights into integrations, playbooks, and other installations.

## Overview of the Value builder

The sam\_user role can identify and prioritize functionalities that haven't yet been implemented or aren't being used.

The Value builder functionality enables you to perform the following actions:

-   Learn how close your instance is to maximizing the value of your Software Asset Management application.
-   Track Value builder tasks that are automatically generated when publisher packs aren't fully used and are identified as incomplete. You can also manually create Value builder tasks. For details see [Create a Value builder task](../task/create-valuebuilder-task.md).
-   Filter the data by domain or category or you can filter by both domain and category. The filter applies to the entire dashboard, and when selected, displays only the data that matches the specific filter.
-   Prioritize or increase visibility of certain tasks by marking tasks as favorites.
-   Stay up to date and get a glimpse of the new features available in the upcoming release.

You can view a maximum of 15 tasks in the Value builder section. To see additional tasks, click **View all**.

![Value builder in the Success Portal view.](../image/value-builder.png "Value builder dashboard")

## Use case for Value builder

The Value builder displays four donut chart widgets to the sam\_user role. Each widget shows you how far your instance is from fully using the Software Asset Management capabilities.

For example, the Publisher pack utilization widget shows five publisher packs but only four are being used in your instance. A Value builder task automatically gets created for the additional publisher pack that is not being used and appears in the New Value builder tasks section. You can prioritize this task and click the star icon to add this task to your Favorites list. If you decide not to work on this task, you can click **Dismiss** to remove it from the New Value builder tasks section.

## Value builder widgets

Select a donut chart widget to take you to the list view of records. For example, if you want to view the incomplete publisher pack records, select the incomplete part in the donut chart widget.

All the widgets get refreshed and the value builder tasks are created after the following two scheduled jobs run:

-   **SAM- Update value builder usage**
-   **SAM- Value builder content handler**

<table id="table_obc_4fc_kvb"><thead><tr><th>

Widget

</th><th>

Source

</th><th>

Description

</th></tr></thead><tbody><tr><td>

SAM apps and plugins

</td><td>

sam apps and plugins \[samp\_sp\_apps\_and\_plugins\]

</td><td>

All Software Asset Management plugins and store applications that are available to use and how many haven't been installed on your instance.

 **Complete** indicates the store applications and plugins that are installed. **Incomplete** indicates the store applications and plugins that haven't yet been installed.

</td></tr><tr><td>

Publisher pack utilization

</td><td>

SAM Publisher Pack Utilization \[samp\_sp\_publisher\_pack\_utilization\]

</td><td>

All publisher packs that are available for use and how many are actually being used.

 **Complete** indicates the publisher packs that are fully used. **Incomplete** indicates the publisher packs that aren't fully used.

 Utilization of a publisher pack depends on a criteria. If the value is true for all three details in the **Usage details** section of a publisher pack record, namely **Plugin enabled?**, **Usage found?**, and **Entitlements created?**, then the publisher pack is considered to be fully used and is set to be complete. If the value for even one of the three entities is false, then the publisher pack is considered to be not fully used and is set to be incomplete. Value builder tasks are automatically created for incomplete publisher packs.

 The criteria for **Usage found?** differs for each publisher pack. For details on the specific **Usage found?** criteria for each publisher pack, see [Usage criteria for publisher packs](../reference/publisher-pack-criteria-usage.md).

</td></tr><tr><td>

Usage under management

</td><td>

SAM usage under management \[samp\_usage\_under\_management\]

</td><td>

Usage of all licensable products.

 Usage of licensable products depends on a criteria. If the value is true for both **Usage found?** and **Entitlement created?**, the product is considered to be used.

 The criteria for **Usage found?** differs for each product. For **Usage Found?** to be considered complete, any one of the following entities should be detected in your instance for a product.

-   Discovery model
-   Client access record
-   Subscription

</td></tr><tr><td>

Value builder tasks by status

</td><td>

SAM Value Builder Task \[samp\_sp\_vb\_task\]

</td><td>

All value builder tasks that are in the following states:

-   **New**
-   **In progress**
-   **Pending review**
-   **Closed complete**

**Note:** Value builder tasks that are in the **Closed Skipped**state aren't displayed.

</td></tr><tr><td>

Value builder tasks \(In Progress\)

</td><td>

SAM Value Builder Task \[samp\_sp\_vb\_task\]

</td><td>

Value builder tasks that are currently in progress.

</td></tr><tr><td>

Value builder tasks \(Favorites\)

</td><td>

SAM Value Builder Task \[samp\_sp\_vb\_task\]

</td><td>

Value builder tasks that are marked as favorites.

 Click the star icon in front of a value builder task, in the Value builder task section to mark it as a favorite.

</td></tr><tr><td>

Value builder tasks \(Success Guides\)

</td><td>

SAM Value Builder Task \[samp\_sp\_vb\_task\]

</td><td>

Value builder tasks that would enable you in accessing the Success Guides.

</td></tr><tr><td>

New Value builder tasks

</td><td>

SAM Value Builder Task \[samp\_sp\_vb\_task\]

</td><td>

All value builder tasks that are still in the **New** state and aren't favorites.

</td></tr><tr><td>

New Updates

</td><td>

SAM Value Builder Task \[samp\_sp\_vb\_task\]

</td><td>

Preview of the features in the upcoming release.

</td></tr></tbody>
</table>