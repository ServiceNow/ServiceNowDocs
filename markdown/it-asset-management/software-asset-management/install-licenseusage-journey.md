---
title: License usage analysis
description: Gain visibility into the end-to-end journey from installing software to consuming licenses.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Exploring Software Asset Management, Software Asset Management, IT Asset Management]
---

# License usage analysis

Gain visibility into the end-to-end journey from installing software to consuming licenses.

## Overview of license usage analysis

Enable SAM managers to map the entire process from software installation to license utilization. This process includes identifying licenses used for each installation and differentiating between installations that have been used and those installations that haven't.

To gain further insights into your installations, use node maps for a detailed numerical breakdown. For each product, explore the installation layer to see the product versions and editions, examine the consumption status layer to determine if the installations are licensed, unlicensed, ignored, or require action. Finally, review the licensing layer that displays the software model results.

The nodes of a node map are stored in the Install Consumption Nodes \[samp\_install\_consumption\_nodes\] table and the nodes are generated during reconciliation. You can view the node map in the License operations view in the Products with installs list. For details on node maps, see [View license usage for your installations](../task/view-install-usage.md).

## Benefits to the SAM manager

-   Verify that the total number of installations for a product aligns with the sum of used and not used installations.
-   Determine the licensing status of the installations: licensed, unlicensed, requiring action, and ignored.
-   Determine all issues related to installations in one view.
-   Determine all key licensing concepts applied such as downgrades and inference.
-   Track usage statistics by viewing the consumption percentage and installation status count.

## Considerations for node maps

Here are some special considerations to keep in mind for node maps:

-   Grouping: Reconciliation can be run with a group and a subgroup. The node map displays each group and subgroup as nodes.
-   Domain separation: Reconciliation can be executed for a specific domain level, displaying domain-separated information based on the user's domain. If a product spans multiple domains, a separate node map gets generated for each domain. Consequently, you can view each node map within its respective domain, resulting in a single product having multiple node maps in the same reconciliation run.

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

**Related topics**  


[View license usage for your installations](../task/view-install-usage.md)

