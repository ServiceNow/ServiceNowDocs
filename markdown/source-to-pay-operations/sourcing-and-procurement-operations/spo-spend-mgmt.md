---
title: Spend and Savings Management
description: Category management is a strategic procurement approach that involves managing a group of related products or services to maximize value, optimize costs, and enhance supplier relationships. Essentially, it’s the structured management of category taxonomy, ensuring that goods and services are categorized, sourced, and managed efficiently to drive better decision-making and operational efficiency.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Spend and Savings Management

Category management is a strategic procurement approach that involves managing a group of related products or services to maximize value, optimize costs, and enhance supplier relationships. Essentially, it’s the structured management of category taxonomy, ensuring that goods and services are categorized, sourced, and managed efficiently to drive better decision-making and operational efficiency.

The Spend and Savings Management \(sn\_spend\_mgmt\) feature enables category managers to import and manage their organization's category taxonomy. By incorporating this taxonomy into the ServiceNow system, category managers can streamline procurement processes, track spending, and evaluate savings more effectively at the category level.

**Important:** Check your entitlements to determine whether you have access to Spend and Savings Management.

The Spend and Savings Management application offers the following key benefits:

-   **Cost optimization**: Analyze spending across categories to identify areas for cost reduction through better supplier negotiations, volume discounts, and contract optimization.
-   **Improved visibility**: Categorize spend to gain insights into where money is being spent, enabling better decision-making and control over expenses.
-   **Strategic sourcing**: Consolidate spend within specific categories to achieve better pricing and terms with suppliers.
-   **Risk management**: Identify potential supplier risks early on by closely monitoring spend within categories and ensuring compliance with regulatory requirements.
-   **Enhanced procurement efficiency**: Streamline the procurement process by focusing on key categories, reducing unnecessary administrative tasks.
-   **Data-driven decision making**: Use data analytics to identify trends and make informed procurement decisions based on category performance.

For more information about using Spend and Savings Management, see [Using Spend and Savings Management](using-spend-mgmt.md).

## Required role

Category manager admin \(sn\_spend\_mgmt.category\_manager\_admin\): Can import the category taxonomy and update the Spend Category and Spend Category Stage tables.

## Tables installed

<table id="table_blg_sm1_q2c"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Spend Category \(sn\_spend\_mgmt\_category\)

</td><td>

Stores data about spend categories.

</td></tr><tr><td>

Spend Category Stage \(sn\_spend\_mgmt\_category\_stage\)

</td><td>

Temporarily stores important data about spend categories before this data is sent to the Spend Category \(sn\_spend\_mgmt\_category\) primary table.

</td></tr><tr><td>

Spend to Product Category Mapping\(sn\_spend\_mgmt\_m2m\_spend\_product\)

</td><td>

Stores the mapping of spend categories to product categories.

</td></tr></tbody>
</table>-   **[Components installed with Spend and Savings Management](../reference/components-spend-savings.md)**  
Several types of components are installed with activation of the Spend and Savings Management \(sn\_spend\_mgmt\) plugin, including user roles and tables.
-   **[Category management tab](category-mgmt-tab.md)**  
The Category management tab provides an overview of spend, savings, and pipeline projects, highlights savings opportunities, and enables creating pipeline projects directly from filtered lists.
-   **[Category analytics](spo-category-analytics.md)**  
Within the Source-to-Pay Workspace, the Category analytics module includes the Savings dashboard that offers procurement teams a unified view of savings opportunities across the sourcing pipeline.

**Parent Topic:**[Explore Sourcing and Procurement Operations](exploring-spo.md)

**Related topics**  


[My purchases on Shopping Hub](my-purchases.md)

[Shopping Hub Mobile](shoppinghub-mobile.md)

[Performance Analytics for Sourcing and Procurement Operations](performance-analytics-for-spo.md)

[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

[Procurement Case Management](psd-overview.md)

[Source-to-Pay Workspace](procurement-specialist-workspace.md)

[Sourcing Pipeline Management](spo-sourcing-pipeline-mgmt.md)

[Understanding Punchout](punchout-overview.md)

[AI Search for Sourcing and Procurement Operations](ai-search-sourcing-procurement-operations.md)

