---
title: Sourcing Pipeline Management
description: Sourcing Pipeline Management \(sn\_spend\_pipeline\) provides a centralized framework for creating, tracking, and executing sourcing initiatives through pipeline projects. It enhances efficiency through automated workflows, improves visibility into project progress, and simplifies savings tracking and forecasting.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing Pipeline Management

Sourcing Pipeline Management \(sn\_spend\_pipeline\) provides a centralized framework for creating, tracking, and executing sourcing initiatives through pipeline projects. It enhances efficiency through automated workflows, improves visibility into project progress, and simplifies savings tracking and forecasting.

Sourcing Managers gain access to a unified pipeline project workspace that consolidates sourcing events, negotiations, and contract management. Each pipeline project includes dedicated tabs for these components, along with UI actions to initiate them directly. All related work, including sourcing requests, is consolidated within the pipeline, providing complete, end-to-end visibility into sourcing activities.

**Important:** Check your entitlements to determine whether you have access to Sourcing Pipeline Management.

With the pipeline\_management\_admin role, you can configure the Pipeline project creation rule decision table to automate the creation of pipeline projects. The default pipeline project creation rule automatically creates a pipeline project when the total price of the products being sourced exceeds $250,000. When a sourcing intake request is submitted, a pipeline project is automatically created in the Draft state when the rule conditions are met. The pipeline project is associated with the sourcing request.

For more information about using Sourcing Pipeline Management, see [Using Sourcing Pipeline Management](use-pipeline-sourcing-mgmt.md).

## Plugin dependencies

The following are the plugin dependencies that are required to use Sourcing Pipeline Management \(sn\_spend\_pipeline\).

-   Source-to-Pay Common Architecture \(sn\_shop\)
-   Sourcing and Purchasing Automation \(sn\_pr\)
-   Spend and Savings Management \(sn\_spend\_mgmt\)

## Viewing pipeline projects in the Source-to-Pay Workspace

You can view pipeline projects by navigating to the **Lists** tab in the Source-to-Pay Workspace. Within this tab, pipeline projects are accessible through the **Pipeline projects** sub-module under both the My work and All work modules. Additionally, you can access them via the **Sourcing pipeline: new request** submodule under the Review needed module.

Fulfillers can view their assigned pipeline projects directly in the Work to review panel on the Source-to-Pay Workspace landing page. Each pipeline project appears in a dedicated tile.

To filter and locate specific pipeline projects, fulfillers can use the All work types filter and select **Pipeline project** from the drop-down list.

Fulfillers can view tasks related to pipeline projects in the Distribution of Work section of the Summary panel on the Source-to-Pay Workspace workspace landing page. Pipeline projects also appear in the Recently updated section.

-   **[Components installed with Sourcing Pipeline Management](../reference/components-pipeline-mgmt.md)**  
Several types of components are installed with activation of the Sourcing Pipeline Management \(sn\_spend\_pipeline\) plugin, including user roles and tables.
-   **[Pipeline project creation rule for high-value sourcing requests](pipeline-project-creation-rule.md)**  
By default, the Pipeline project creation rule decision table is used to create pipeline projects automtatically in Sourcing Pipeline Management.
-   **[Automatic pipeline project creation via Shopping Hub or Employee Center intake requests](automatic-pipeline-creation.md)**  
When a shopper submits sourcing requests for products, pipeline projects are automatically created, provided the product price meets the budget conditions defined in the decision table.
-   **[Email notifications for pipeline projects](pipeline-email-notifications.md)**  
Sourcing managers receive email notifications when a pipeline project is created automatically, and before its estimated start and end dates.
-   **[Pipeline management tab](pipeline-mgmt-tab.md)**  
The Pipeline management tab enables you to get insights into savings and pipeline projects, improving visibility, tracking, and collaboration across teams.

**Parent Topic:**[Explore Sourcing and Procurement Operations](exploring-spo.md)

**Related topics**  


[My purchases on Shopping Hub](my-purchases.md)

[Shopping Hub Mobile](shoppinghub-mobile.md)

[Performance Analytics for Sourcing and Procurement Operations](performance-analytics-for-spo.md)

[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

[Procurement Case Management](psd-overview.md)

[Source-to-Pay Workspace](procurement-specialist-workspace.md)

[Spend and Savings Management](spo-spend-mgmt.md)

[Understanding Punchout](punchout-overview.md)

[AI Search for Sourcing and Procurement Operations](ai-search-sourcing-procurement-operations.md)

