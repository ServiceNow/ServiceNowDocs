---
title: AI portfolio overview
description: Act on the AI governance work that matters most, review the state of your AI portfolio, and track the value your AI assets deliver on the Home page in AI Control Tower.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/intelligent-experiences/aict-ai-portfolio-overview.html
release: zurich
topic_type: concept
last_updated: "2026-07-22"
reading_time_minutes: 4
keywords: [Now Assist, AI Agents, generative AI, agentic AI]
breadcrumb: [Explore, AI Control Tower, Enable AI experiences]
---

# AI portfolio overview

Act on the AI governance work that matters most, review the state of your AI portfolio, and track the value your AI assets deliver on the **Home** page in AI Control Tower.

## Key benefits

-   Identify the highest-priority recommendations and lifecycle tasks that need your attention today.
-   Review the size and composition of your AI asset inventory and the split between managed and unmanaged assets.
-   Check the governance posture of your managed AI assets across quality, safety, security, compliance, and residual risk avoidance.
-   Track the total value your managed AI assets deliver and the trend over time.

The **Home** page provides a portfolio-level view of all AI assets across your organization. For a detailed view scoped to a single AI asset, see [Working with AI asset records](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/disc-managing-ai-assets.md).

**Note:** If you have the AI Asset Owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, the **Home** page displays details only for the AI assets that you're assigned to manage.

\[Omitted image "aict-home.png"\] Alt text: Access an overview of your AI portfolio on the Home tab in AI Control Tower.

## Required roles

The AI steward \[sn\_ai\_governance.ai\_steward\] or AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role is required to access the **Home** page in AI Control Tower.

## Accessing the overview

Access an overview of your AI portfolio on the **Home** page in AI Control Tower by navigating to **All** &gt; **AI Control Tower** &gt; **Home**.

## Use cases

-   Act on the recommendations AI Control Tower has surfaced for you from the **Your top recommendations** widget.
    -   Review each recommendation and resolve it using the primary action on the card.
    -   Select **See all Recommendations in Activity Center** to open the full list of recommendations for your portfolio. For more information, see [Recommendations and AI insights](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-recommendations-ai-insights.md).
-   Check how much work is waiting for you across AI Control Tower from the **Pending work items** widget.
    -   Review the total count of work items assigned to you or created by you, spanning recommendations, lifecycle tasks, and the other work types tracked in Activity Center.
    -   Select the widget to open **Activity Center** and work through the underlying items. For more information, see [Addressing your AI action items](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/intelligent-experiences/aict-addressing-ai-action-items.md).
-   Review the size and composition of your AI inventory.
    -   If you have the AI steward \[sn\_ai\_governance.ai\_steward\] role, you can view the total number of AI assets in the **Inventory** widget. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, you can view the total number of assets you own in the **Your inventory** widget.
    -   Break down your inventory by **By type**, **By status**, **By department**, or **By management status**, and identify where your assets are concentrated.
    -   Select the widget to open the **Inventory** page, where you can search, filter, and take action on individual assets.
-   Assess the governance health of your managed AI assets from the **Governance posture summary** widget.
    -   Review the distribution of managed AI assets across five dimensions: **Quality**, **Safety**, **Security**, **Compliance**, and **Residual risk**.
    -   Identify the dimensions where your portfolio has the most assets in the **Low** or **NA** category, and use those findings to prioritize governance work.
    -   If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this widget reflects only the assets you own. The **Quality** and **Safety** dimensions remain interactive, but **Security**, **Compliance**, and **Residual risk** are summary-only.
-   Monitor the regulatory risk of your AI assets from the **Regulatory risk classification** widget.
    -   Review the number of AI assets classified as **Unacceptable**, **High**, **Medium**, or **Low** risk.
    -   Focus remediation efforts on assets in the higher-risk tiers, where misclassification or inadequate controls have the most significant consequences.
    -   If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this widget reflects only the assets you own, and does not link out to the full **Regulatory risk classification** page.
-   Track the value your AI assets deliver from the **AI Value** widget.
    -   Check the total return for all managed AI assets and the percentage change over the previous period. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this reflects only the assets you own.
    -   If you have the AI steward \[sn\_ai\_governance.ai\_steward\] role, select the widget to open the full Value page, where you can see per-asset contribution and filter the view by time period, team, or AI system.
-   Review your governance workload in the **Lifecycle tasks needing attention** table.
    -   Select **By inventory** to view a list of AI assets with the most pending tasks. Use this view to identify the assets that are consuming the most governance capacity. If you have the AI asset owner \[sn\_ai\_asset\_mgmt.ai\_asset\_owner\] role, this view is scoped to the assets you own.
    -   If you have the AI steward \[sn\_ai\_governance.ai\_steward\] role, select **By team** to view a list of tasks for team members. Use this view to identify team members who are overloaded or falling behind.
-   If you have the AI steward \[sn\_ai\_governance.ai\_steward\] role, use the **Get started with AI Control Tower** widget to launch a guided setup experience that helps you configure AI Control Tower.
    -   Track your overall setup progress and see the milestone you're currently working on.
    -   Select **Set up now** to open guided setup, or select **Continue** to pick up where you left off.

