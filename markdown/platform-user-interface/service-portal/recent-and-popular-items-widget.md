---
title: Recent &amp; Popular Items widget
description: Allow a user to browse recent and popular catalog items. You can use this base system widget as-is in your portal or clone it to suit your own business needs.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/platform-user-interface/service-portal/recent-and-popular-items-widget.html
release: australia
product: Service Portal
classification: service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Service Catalog widgets, Widget library, Using portal widgets, Configuring Service Portal, Service Portal, Configure UIs and portals, Configure user experiences]
---

# Recent &amp; Popular Items widget

Allow a user to browse recent and popular catalog items. You can use this base system widget as-is in your portal or clone it to suit your own business needs.

## Using the widget

The Recent &amp; Popular Items widget includes two tabs: **My Recent Items** and **Popular Items**.

A user opens the My Recent Items tab to see catalog items that they recently viewed or requested.

\[Omitted image "my-recent-items.png"\] Alt text: My Recent Items tab

A user opens the Popular Items tab to see catalog items that have been widely requested by other users.

\[Omitted image "popular-items.png"\] Alt text: Popular Items tab

Each item card displays basic information about the catalog item, such as the item name, image, and price.

To navigate to the item listing, the user selects **View Details**.

## Instance options

Use the instance options to configure the Recent &amp; Popular Items widget for a portal page.

<table id="table_sgd_y3w_bkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Data

</td></tr><tr><td>

Popular Items used in

</td><td>

Time span over which users have requested the popular items. You select one of the following options:-   **-- None --**: Display popular catalog items with no time span specified. This is the default option.
-   **Last 3 Months**: Display the most requested catalog items in the past three months.
-   **Last 6 Months**: Display the most requested catalog items in the past six months.
-   **Last 12 Months**: Display the most requested catalog items in the past year.
-   **Life time \(Has performance implications\)**: Display the most requested catalog items of all time. Selecting this option may decrease system performance.

</td></tr><tr><td class="sub-head" colspan="2">

Presentation

</td></tr><tr><td>

Number of Items

</td><td>

Maximum number of catalog items to display in each tab. The value is 8 by default.

</td></tr><tr><td class="sub-head" colspan="2">

Behavior

</td></tr><tr><td>

My Recent Items By

</td><td>

Criteria to qualify which catalog items are displayed in the My Recent Items tab. You can select one of the following options:-   **-- None --**: Display recent items with no criteria specified. This is the default option.
-   **View**: Display the catalog items that the user viewed most recently.
-   **Request**: Display the catalog items that the user requested most recently.

</td></tr></tbody>
</table>**Parent Topic:**[Service Catalog widgets](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/service-portal/sc-widgets.md)

**Related topics**  


[Catalog Content widget]()

[Catalog Homepage Search widget]()

[Request Fields widget]()

[Requested Items widget]()

[Requests and Approvals widget]()

[SC Catalog Item widget]()

[SC Categories widget]()

[SC Category Page widget]()

[SC Order Guide widget]()

[SC Popular Items widget]()

[SC Save Bundles widget]()

[SC Saved Carts widget]()

[SC Scroll to top widget]()

[SC Shopping Cart widget]()

[SP Variable Editor widget]()

[SC Wish List Cart widget]()

[Create and edit a page using the Service Portal Designer]()

[Configure widget instances]()

[Clone a widget]()

