---
title: Multi-tier structure \(nested tiers\)
description: Create complex, multi-tier layouts in ServiceNow CPQ by nesting tiers in other tiers using a layout CSV file. Define tier display types—such as tabs, expandable sections, and basic containers—to organize fields and achieve flexible, structured, and visually clear configuration interfaces.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2025-10-08"
reading_time_minutes: 2
breadcrumb: [Set up layouts, ServiceNow CPQ app, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Multi-tier structure \(nested tiers\)

Create complex, multi-tier layouts in ServiceNow CPQ by nesting tiers in other tiers using a layout CSV file. Define tier display types—such as tabs, expandable sections, and basic containers—to organize fields and achieve flexible, structured, and visually clear configuration interfaces.

In ServiceNow CPQ, there are two basic container types: tiers and column sets. This article focuses on the top-level container \(tiers\) and how to achieve more complex layouts by nesting different types of tiers.

**Note:** As of May 23, 2023, nesting tiers is not supported in the Layout Wizard or in the layout editor. However, you can change the display type of existing tiers, including nested tiers.

The basic CSV format for a single-tier structure looks like this:

![CSV file](../images/cpq-layout-nested-tiers-1-tier.png)

The tier definition defines the visual display of a level of tier, not just one particular tier. So in this case, all three tiers \(tab1, tab2, and tab3\) are defined as the Tab display type. This creates a simple structure where each tier in the CSV file appears as a tab.

However, different types of tier display types may sometimes be nested in another tier. The simplest example is a two-tier structure. Letʼs build off of our first example and nest some expandable sections in one of our tabs.

![CSV file](../images/cpq-layout-nested-tiers-2-tiers.png)

Notice how the nested tier is defined. The tier definition row path is “layout/tiers/tiers”, indicating that a tier that is below another tier in the path should be defined as an expandable section. You can then see that on rows 3 and 4, the tier “exsect1” is placed below the tier “tab1” in the path. This displays for the end-user like so:

![Multi-tier structure (nested tiers)](../images/cpq-layout-nested-tiers-end-user-display.png)

You can extrapolate this pattern to create deeper tier structures, declaring more and more nested definitions. However, note that you cannot have multiple tier definitions at the same level. For example, the tiers in the first image shown below are valid, but the tiers in the second image are not valid, because the component display type for /layout/tiers/tiers is both ExpandableSection and VerticalTab.

Valid tiers:

![CSV file](../images/cpq-layout-nested-tiers-valid-tiers.png)

Invalid tiers:

![CSV file](../images/cpq-layout-nested-tiers-invalid-tiers.png)

## Displaying fields outside the bottom tier

A common use case of nested tiers may be to have a bottom layer nested inside a top layer tier, with some general fields displayed outside the bottom tier. This can be achieved by using an intermediary tier of the BasicContainer display type. This structure might look like this for the end user:

![Multi-tier structure (nested tiers)](../images/cpq-layout-nested-tiers-fields-ouside-bottom-tier.png)

The layout CSV file is structured like so:

![CSV file](../images/cpq-layout-nested-tiers-fields-outside-bottom-tier-csv.png)

